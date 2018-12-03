<template>
  <spam>

    <header>
      <nav-bar logo="Social" url="#" cor="green darken-1"/>
    </header>

    <main>
      <div class="container">

        <div class="row">
          <grid-vue tamanho="4">

            <card-menu-vue>
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
            </card-menu-vue>

          </grid-vue>
          <grid-vue tamanho="8">
            <slot />
          </grid-vue>
        </div>

      </div>
    </main>

    <footer-vue cor="green darken-1" logo="Social" descricao="Teste de descricao" ano="2018">

      <li><a class="grey-text text-lighten-3" href="#!">Link 1</a></li>
      <li><a class="grey-text text-lighten-3" href="#!">Link 2</a></li>
      <li><a class="grey-text text-lighten-3" href="#!">Link 3</a></li>
      <li><a class="grey-text text-lighten-3" href="#!">Link 4</a></li>

    </footer-vue>

  </spam>
</template>

<script>
import NavBar from '@/components/layouts/NavBar'
import FooterVue from '@/components/layouts/FooterVue'
import GridVue from '@/components/layouts/GridVue'
import CardMenuVue from '@/components/layouts/CardMenuVue'

export default {
  name: 'SiteTemplate',
  components:{
    NavBar,
    FooterVue,
    GridVue,
    CardMenuVue
  }
}
</script>

<style>

</style>
