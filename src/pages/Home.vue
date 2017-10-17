<template>
  <div>
  	<home-header></home-header>
  	<list></list>
  </div>
</template>

<script>
import HomeHeader from '../components/HomeHeader'
import List from '../components/List'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created (){
  	var listUrl = '/api/goods';
//	this.$http.get(listUrl).then(function(res){
//		var thisData =res.body;
//		this.listData = thisData;
//	})
  },
  components: {
  	HomeHeader,
  	List
  }
}
</script>
