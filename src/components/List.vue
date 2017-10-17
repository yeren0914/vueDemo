<template>
  <yd-list theme="2"> 
        <yd-list-item v-for="item in list">
            <img slot="img" :src="item.img">
            <span slot="title">{{item.title}}</span>
            <yd-list-other slot="other ">
                <div>
                    <span  class="list-price">{{ item.price |price}}</span>
                </div>
            </yd-list-other>
        </yd-list-item>
    </yd-list>
</template>
<script>
import Vue from 'vue'
import {ListTheme, ListItem, ListOther} from 'vue-ydui/dist/lib.rem/list';
export default {
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      list:[]
    }
  },
  created (){
  	const listUrl = '/api/goods';
  	this.$http.get(listUrl).then(function(res){
  		this.list = res.body.data;
  	})
  }
}
Vue.filter('price', function(value){
	return '￥' + value +'元'
})

</script>
