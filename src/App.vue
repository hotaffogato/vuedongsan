<template>

  <div class="black-bg" v-if="modal" @click="modalToggle">
    <div class="white-bg">
      <img :src="rooms[modalId].image">
      <h4>{{rooms[modalId].title}}</h4>
      <p>{{ rooms[modalId].content }}</p>
      <p>{{ rooms[modalId].price }}원</p>
    </div>
  </div>


  <div class="menu">
      <a v-for="item in menus" :key="item">{{item}}</a>
  </div>

  <DiscountTag />

  <!-- <CardTag /> -->


</template>

<script>



export default {
  name: 'App',
  data(){
    return{

    }
  },
  methods:{

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
  background: darkslateblue;
  padding:15px;
  border-radius: 5px;
}
.menu a {
  color : white;
  padding:10px;
}
.room-img{
  width:80%;
  margin-top: 40px;
}

.black-bg{
  width:100%;
  height:100%;
  background: #000;
  position:fixed;
  padding:20px;
}
.white-bg{
  background: #fff;
  width:100%;
  border-radius: 10px;
  padding:20px;
}
.discount{
  background: #eee;
  padding:10px;
  margin:10px;
  border-radius: 10px;
}
</style>
