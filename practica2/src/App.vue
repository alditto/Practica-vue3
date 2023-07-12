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

  <footer class="page-footer">
    <div class="container">
      <div class="row">
        <div class="col l6 s12">
          <h5 class="white-text">Pie de pagina</h5>
          <p class="grey-text text-lighten-4">Practica 2.</p>
        </div>
        <div class="col l4 offset-l2 s12">
          <h5 class="white-text">Links</h5>
          <ul>
            <li><a class="grey-text text-lighten-3" href="#!">Link 1</a></li>
            <li><a class="grey-text text-lighten-3" href="#!">Link 2</a></li>
            
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      <div class="container">© 2023 Copyright
      </div>
    </div>
  </footer> 
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

