<template>

  <site-template>
    <span slot="menusesquerdo">
      <div class="row valign-wrapper">
        <grid-vue tamanho="4">
          <img src="http://materializecss.com/images/yuna.jpg" alt="" class="circle responsive-img">
        </grid-vue>
        <grid-vue tamanho="8">
          <span class="black-text">
            <h5>Maria Silva</h5>
            This is a square image. Add the "circle" class to it to make it appear circular.
          </span>
        </grid-vue>
      </div>
    </span>

    <span slot="principal">
      <publicar-conteudo-vue />

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

  </site-template>

</template>

<script>
import SiteTemplate from '@/templates/SiteTemplate'
import CardConteudoVue from '@/components/social/CardConteudoVue'
import CardDetalheVue from '@/components/social/CardDetalheVue'
import PublicarConteudoVue from '@/components/social/PublicarConteudoVue'
import GridVue from '@/components/layouts/GridVue'

export default {
  name: 'Home',
  data () {
    return {

    }
  },
  components:{
    SiteTemplate,
    CardConteudoVue,
    CardDetalheVue,
    PublicarConteudoVue,
    GridVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
