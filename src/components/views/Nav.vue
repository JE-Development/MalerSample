<style scoped>

.nav{
  height: 60px;
  background: white;
}

.gradient{
  height: 15px;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.1), transparent);
}

.icon{
  width: 30px;
  height: 30px;
}

.logo-area{
  font-size: 20px;
  font-weight: bold;
}

.nav-item{
  margin-left: 30px;
  text-decoration: none;
  color: #5c5c5c;
  transition: color 0.1s linear;
}

.nav-item:hover{
  color: #2562e9;
}

.hide-nav{
  display: flex;
}

.show-mobile{
  display: none;
}

.mobile-nav{
  height: 0;
  width: 100%;
  background: white;
  overflow: hidden;
  transition: height 0.5s ease;
}

.mobile-nav-height{
  height: 140px;
}

.mobile-item{
  width: 100%;
}

.nav-p{
  height: 50px;
}

@media (max-width: 650px) {
  .nav-item{
    margin-left: 10px;
    text-decoration: none;
    color: #5c5c5c;
    transition: color 0.1s linear;
  }

  .logo-area{
    font-size: 15px;
    font-weight: bold;
  }

  .icon{
    width: 20px;
    height: 20px;
  }
}

@media (max-width: 500px) {
  .hide-nav{
    display: none;
  }

  .show-mobile{
    display: flex;
  }
}

</style>

<template>

  <div class="fixed max-width">
    <div class="nav center-horizontal">
      <div class="space-between max-height main-content-width center-vertical">
        <div class="logo-area center-vertical">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="icon prim-color"><path d="M18.37 2.63 14 7l-1.59-1.59a2 2 0 0 0-2.82 0L8 7l9 9 1.59-1.59a2 2 0 0 0 0-2.82L17 10l4.37-4.37a2.12 2.12 0 1 0-3-3Z"></path><path d="M9 8c-2 3-4 3.5-7 4l8 10c2-1 6-5 6-7"></path><path d="M14.5 17.5 4.5 15"></path></svg>
          <div style="width: 10px"></div>
          MalerPro
        </div>
        <div>
          <div class="center-vertical hide-nav">
            <a href="/#home" class="nav-item">Startseite</a>
            <a href="/#menu" class="nav-item">Leistungen</a>
            <a href="/#about" class="nav-item">Über uns</a>
            <a href="/#projects" class="nav-item">Projekte</a>
            <a href="/#contact" class="nav-item">Kontakt</a>
          </div>
          <div class="show-mobile">
            <Icon size="30" class="decent-color pointer" @click="onMobileMenu">
              <Menu2/>
            </Icon>
          </div>
        </div>
      </div>
    </div>
    <div class="mobile-nav" :class="showMobileMenu ? 'mobile-nav-height' : ''">
      <p class="reset-margin max-width center-text"><a href="/#home" class="nav-item" @click="hideMobileNav">Startseite</a></p>
      <div style="height: 10px"></div>
      <p class="reset-margin max-width center-text"><a href="/#menu" class="nav-item" @click="hideMobileNav">Leistungen</a></p>
      <div style="height: 10px"></div>
      <p class="reset-margin max-width center-text"><a href="/#about" class="nav-item" @click="hideMobileNav">Über uns</a></p>
      <div style="height: 10px"></div>
      <p class="reset-margin max-width center-text"><a href="/#projects" class="nav-item" @click="hideMobileNav">Projekte</a></p>
      <div style="height: 10px"></div>
      <p class="reset-margin max-width center-text"><a href="/#contact" class="nav-item" @click="hideMobileNav">Kontakt</a></p>
      <div style="height: 10px"></div>
    </div>
    <div class="gradient max-width"></div>
  </div>

</template>


<script>

import {Menu2} from "@vicons/tabler"
import {Icon} from "@vicons/utils"

export default {
  name: "Nav",
  components: {Icon, Menu2},
  data() {
    return {
      showMobileMenu: false,
    };
  },

  props: {
  },

  created() {
  },

  mounted() {

  },


  methods: {
    onMobileMenu() {
      this.showMobileMenu = !this.showMobileMenu
    },

    hideMobileNav() {
      this.showMobileMenu = false
    }
  }
}
</script>