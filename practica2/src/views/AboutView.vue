<template>
  <div class="about">
    <h1>{{appName}}</h1>
  </div>
</template>
<script>
export default{
  name: 'About',
  data(){
    const appName= process.env.VUE_APP_NAME;
    return{
      appName
    }
  }
}
</script>