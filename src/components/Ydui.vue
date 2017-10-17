<template>
	 <yd-layout>
	 	<yd-navbar slot="navbar" title="登录">
        </yd-navbar>
        <yd-cell-group title="必填内容" >
			<yd-cell-item>
				<span slot="left">手机号：</span>
				<input type="number" slot="right" placeholder="请输入手机号" v-model="username" />
			</yd-cell-item>
			<yd-cell-item>
				<span slot="left">密&nbsp;&nbsp;&nbsp;&nbsp;码：</span>
				<input type="password" slot="right" placeholder="请输入密码"  v-model="userpwd"/>
			</yd-cell-item>
		</yd-cell-group>
		<yd-cell-group title="可选内容">
			<yd-cell-item>
				<span slot="left">性别：</span>
				<select slot="right" v-model="usersex">
					<option value="0">保密</option>
					<option value="1">男</option>
					<option value="2">女</option>
				</select>
			</yd-cell-item>
			<yd-cell-item>
				<span slot="left">年龄：</span>
				<input slot="right" type="number" placeholder="请输入年龄" v-model="userage" />
			</yd-cell-item>
		</yd-cell-group>

		<yd-button size="large" type="primary" shape="square" @click="submitFun">提交信息</yd-button>
	 </yd-layout>
</template>

<script>
import {CellGroup, CellItem} from 'vue-ydui/dist/lib.rem/cell';
import {Button, ButtonGroup} from 'vue-ydui/dist/lib.rem/button';
import {  Alert, Toast, Notify, Loading } from 'vue-ydui/dist/lib.rem/dialog';

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      username: '',
      userpwd: '',
      userage: 0,
      usersex: 0
      
    }
  },
  created () {
  	this.$dialog.loading.open('页面加载中。。。');
  	setTimeout(()=> {
  		this.$dialog.loading.close()
  	},2000);
  },
  methods: {
  	submitFun () {
      console.log(333);
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
