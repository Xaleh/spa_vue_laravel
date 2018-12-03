<template>

  <login-template>

    <span slot="menusesquerdo">
      <ul>
        <img src="http://www.inesting.org/ad2006/adminsc1/app/marketingtecnologico/uploads/redessociais_alternativas.jpg" class="responsive-img">
      </ul>
    </span>

    <span slot="principal">
      <h2>Login</h2>

      <input type="text" placeholder="E-mail" value="">
      <input type="text" placeholder="Senha" value="">
      <button type="button" class="btn">Entrar</button>
    </span>


  </login-template>

</template>

<script>
import LoginTemplate from '@/templates/LoginTemplate'
import CardConteudoVue from '@/components/social/CardConteudoVue'
import CardDetalheVue from '@/components/social/CardDetalheVue'
import PublicarConteudoVue from '@/components/social/PublicarConteudoVue'

export default {
  name: 'Login',
  data () {
    return {

    }
  },
  components:{
    LoginTemplate,
    CardConteudoVue,
    CardDetalheVue,
    PublicarConteudoVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
