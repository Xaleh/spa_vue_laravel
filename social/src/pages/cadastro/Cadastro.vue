<template>

  <login-template>

    <span slot="menusesquerdo">
      <ul>
        <img src="http://www.inesting.org/ad2006/adminsc1/app/marketingtecnologico/uploads/redessociais_alternativas.jpg" class="responsive-img">
      </ul>
    </span>

    <span slot="principal">

      <h2>Cadastro</h2>

      <input type="text" placeholder="Nome" value="">
      <input type="text" placeholder="E-mail" value="">
      <input type="password" placeholder="Senha" value="">
      <input type="password" placeholder="Confirme sua Senha" value="">
      <button type="button" class="btn">Enviar</button>
      <router-link class="btn orange" to="/login">Já tenho conta</router-link>

    </span>


  </login-template>

</template>

<script>
import LoginTemplate from '@/templates/LoginTemplate'

export default {
  name: 'Cadastro',
  data () {
    return {

    }
  },
  components:{
    LoginTemplate
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
