<template>

  <site-template>

    <span slot="menusesquerdo">
      <ul>
        <img :src="usuario.imagem" class="responsive-img">
      </ul>
    </span>

    <span slot="principal">

      <h2>Perfil</h2>

      <input type="text" placeholder="Nome" v-model="name">
      <input type="text" placeholder="E-mail" v-model="email">

      <div class="file-field input-field">
        <div class="btn">
          <span>Imagem</span>
          <input type="file" v-on:change="salvaImagem">
        </div>
        <div class="file-path-wrapper">
          <input class="file-path validate" type="text">
        </div>
      </div>

      <input type="password" placeholder="Senha" v-model="password">
      <input type="password" placeholder="Confirme sua Senha" v-model="password_confirmation">
      <button type="button" class="btn" v-on:click="perfil()">Atualizar</button>

    </span>


  </site-template>

</template>

<script>
import SiteTemplate from '@/templates/SiteTemplate'
import axios from 'axios';

export default {
  name: 'Perfil',
  data () {
    return {
      usuario:false,
      name:'',
      email:'',
      password:'',
      password_confirmation:'',
      imagem:''
    }
  },
  created(){
    let usuarioAux = sessionStorage.getItem('usuario');
    if (usuarioAux) {
      this.usuario = JSON.parse(usuarioAux);
      this.name = this.usuario.name;
      this.email = this.usuario.email;
    }
  },
  components:{
    SiteTemplate
  },
  methods:{
    salvaImagem(e){
      let arquivo = e.target.files || e.dataTransfer.files; //Essa segunda opção é para quando alguem arrastar a imagem e soltar na opção de carregar imagem.
      if(!arquivo.length) {
        return;
      }
      let reader = new FileReader();
      reader.onloadend = (e) => {
        this.imagem = e.target.result;
      };
      reader.readAsDataURL(arquivo[0]);

      console.log(this.imagem);

    },
    perfil(){
      axios.put(`http://127.0.0.1:8000/api/perfil`, {
      name: this.name,
      email: this.email,
      imagem: this.imagem,
      password: this.password,
      password_confirmation: this.password_confirmation
    },{"headers":{"authorization":"Bearer "+this.usuario.token}})
      .then(response => {
        // console.log(response)
        if(response.data.token){
          //login com sucesso
          this.usuario = response.data;
          sessionStorage.setItem('usuario', JSON.stringify(this.usuario));
          alert('Perfil atualizado!');

        }else{
          //erros de validação
          console.log("erros de validação");
          let erros = '';
          for(let erro of Object.values(response.data)){
            erros += erro + " ";
          }
          alert(erros);
        }
      })
      .catch(e => {
      console.log(e)
      alert("Erro! Tente novamente mais tarde!")
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
