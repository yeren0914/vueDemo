

<template>
  <div class="hello">
   msg
   <div class="div">
      详情信息
   </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
     plus: function () {
          console.log(11)
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
