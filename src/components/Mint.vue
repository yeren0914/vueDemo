<template>
	<div>
		<section class="page-demo">
			<div class="page-title">Mint UI组件</div>
			<button @click="test">点击提示信息</button>
	      	<button @click="getData">点击提示信息</button>
		</section>
	</div>
</template>

<script>

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      sheetVisible: false,
      actions: [{
        name: '展示 Toast',
        method: this.showToast
      }, {
        name: '展示 Message Box',
        method: this.showMsgbox
      }]
    }
  },
  methods:{
     plus: function () {
         console.log(11)
     },
     test: function () {
        Toast('提示信息')
     },
     getData: function () {
         var url='http://localhost:8080/api/goods';
         fetch(url).then(function(res){
         	console.log(res);
         	console.log(111)
         })
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
