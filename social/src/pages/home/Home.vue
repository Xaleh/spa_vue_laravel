<template>

  <span>
    <div class="row">
      <div class="input-field col s12">
        <textarea id="textarea1" class="materialize-textarea"></textarea>
        <label for="textarea1">O que está acontecendo?</label>
      </div>
      <p>
        <button class="btn col s2 offset-s10">Publicar</button>
      </p>
    </div>

    <card-conteudo-vue
      perfil="http://materializecss.com/images/yuna.jpg"
      nome="Maria Silva"
      data="13/01/18 13:30">

      <card-detalhe-vue
      img="http://materializecss.com/images/sample-1.jpg"
      titulo=""
      texto="Texto que vai ficar debaixo da imagem." />

    </card-conteudo-vue>
  </span>

</template>

<script>
import CardConteudoVue from '@/components/social/CardConteudoVue'
import CardDetalheVue from '@/components/social/CardDetalheVue'

export default {
  name: 'Home',
  data () {
    return {

    }
  },
  components:{
    CardConteudoVue,
    CardDetalheVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
