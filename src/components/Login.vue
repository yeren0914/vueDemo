

<template>
  <div class="hello">
   login
   <div class="div">
      <input type="text"  v-model="username"  />
       <input type="text"  v-model="userpwd"  />
       <button @click="plus">提交数据</button>
   </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      username: '',
      userpwd: ''
    }
  },
  methods:{
     plus: function () {
          this.$router.push('/detail');
          console.log(this.$router);
     }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped  lang="scss">
.hello{
  .div{
        width: 100px;
        height: 100px;
        background-color: #00d6b2;
        border:5px solid #ccc;
  }
}
</style>
