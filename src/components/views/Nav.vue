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

@media (max-width: 600px) {
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
        <div class="center-vertical">
          <a href="/#home" class="nav-item">Startseite</a>
          <a href="/#menu" class="nav-item">Leistungen</a>
          <a href="/#about" class="nav-item">Über uns</a>
          <a href="/#contact" class="nav-item">Projekte</a>
          <a href="/#contact" class="nav-item">Kontakt</a>
        </div>
      </div>
    </div>
    <div class="gradient max-width"></div>
  </div>

</template>


<script>

export default {
  name: "Nav",
  components: {},
  data() {
    return {
    };
  },

  props: {
  },

  created() {
  },

  mounted() {


  },


  methods: {


  }
}
</script>