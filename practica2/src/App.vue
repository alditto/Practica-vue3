<template>
  <div class="container">
    <nav>
      <div class="nav-wrapper">
        <a href="#!" class="brand-logo">MegaDron</a>
        <a href="#" data-target="mobile-demo" class="sidenav-trigger"><i class="material-icons">menu</i></a>
        <ul class="right hide-on-med-and-down">
          <li><router-link to="/">Menu1</router-link></li>
          <li><router-link to="/">Menu2</router-link></li>
          <li><router-link to="/product">Producto</router-link></li>
                 
        </ul>
      </div>
    </nav>

    <ul class="sidenav" id="mobile-demo">
      <li><router-link to="/">Menu1</router-link></li>
      <li><router-link to="/">Menu2</router-link></li>
      <li><router-link to="/product">Producto</router-link></li>
      
    </ul>
   
 
  </div>
  
  <router-view/>

  
</template>

<style lang="scss">


</style>

<script>

export default {
  name: 'AppView',
  data(){
    return {
      
    }
  },
 
  created() {
    document.addEventListener('DOMContentLoaded', function () {
      var elems = document.querySelectorAll('.sidenav');
      var instances = M.Sidenav.init(elems, {});

    });
  }
}
</script>

