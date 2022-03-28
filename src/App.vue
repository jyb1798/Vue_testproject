<template>
<div class="menu">
  <a v-for="item in list" :key="item">{{item}}</a>
</div>

   <div>
      <h4>{{products[0]}}</h4>
      <p>50만원</p>
      <button @click="increase">허위매물신고</button> 
      <span>신고수 : {{신고수[0]}} </span>
   </div>
   <div>
    <h4>{{products[1]}}</h4>
    <p>60만원</p>
    <button @click="increase">허위매물신고</button> 
    <span>신고수 : {{신고수[1]}} </span>
 </div>
 <div>
  <h4>{{products[2]}}</h4>
  <p>70만원</p>
  <button @click="increase">허위매물신고</button> 
  <span>신고수 : {{신고수[2]}} </span>
</div>
</template>

<script>

export default {
  name : 'App',
  data(){
    return {
     신고수 : [0, 0, 0],
     list : ['Home', 'Shop', 'About'], 
     products: ['역삼동원룸', '천호동원름', '마포구원룸'],
     price : ['50만원', '70만원', '80만원'],
    }
  },
  method : {
    increase(){
      this.신고수 += 1
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
