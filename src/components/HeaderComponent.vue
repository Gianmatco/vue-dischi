<template>
<header class="nav g-3">
  <img src="../assets/images/logo-small.svg" alt=""> 
</header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.nav{
  height: 60px;
  width: 100%;
  background-color: #2e3a46;
  color: white;
  img{
    width: 40px;
    margin: 10px;
  }

}

</style>
