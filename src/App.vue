<template>
<div class="menu">
  <a v-for="item in list" :key="item">{{item}}</a>
</div>

   <div v-for="(a, i) in products" :key="i">
      <h4>{{a}}</h4>
      <p>50만원</p>
   </div>
</template>

<script>

export default {
  name : 'App',
  data(){
    return {
     list : ['Home', 'Shop', 'About'], 
      products: ['역삼동원룸', '천호동원름', '마포구원룸'],
      price : ['50만원', '70만원', '80만원'],
    }
  },
  components: {
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background-color : #F5dF4D;
  padding: 30px;
  border-radius: 5px;
}

.menu a{
  color: #939597;
  padding: 20px;
}


</style>
