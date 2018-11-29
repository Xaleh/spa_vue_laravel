<template>

  <div class="card">
    <div class="card-content">
      <div class="row valign-wrapper">

        <grid-vue tamanho="1">
          <img src="http://materializecss.com/images/yuna.jpg" alt="" class="circle responsive-img">
        </grid-vue>
        <grid-vue tamanho="11">
          <span class="black-text">
            <strong>Maria Silva</strong> - <small>12/01/18 12:30</small>

          </span>
        </grid-vue>

      </div>

      <div class="card-image">
        <img src="http://materializecss.com/images/sample-1.jpg">
        <span class="card-title">Card Title</span>
      </div>

      <div class="card-content">
        <p>Teste de texto.</p>
      </div>

    </div>
    <div class="card-action">
      <p>
        <i class="material-icons">favorite_border</i>
        <i class="material-icons">insert_comment</i>
      </p>
    </div>
  </div>

</template>

<script>
import GridVue from '@/components/layouts/GridVue'

export default {
  name: 'CardConteudoVue',
  props:[],

  data () {
    return {

    }
  },
  components:{
    GridVue
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
