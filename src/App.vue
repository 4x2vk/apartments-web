<template>

  <div class="menu">
    <a v-for="loop in menu" :key="loop"> {{ loop }}</a>
  </div>

  <div v-for="(a,i) in products" :key="i">
    <h4>{{ a }}</h4>
    <p>50만워</p>
    <button v-on:click="신고수++">허위매물신고</button> <span>신고수 : {{신고수}} </span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      신고수 : 0,
      price : [60, 70, 80],
      menu : ['Home', 'Shop', 'About'],
      products :  ['역삼동원룸', '천호동원룸', '마포구원룸'],
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
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}
</style>
