###1.JQ-this和$(this)
    $(this)只是一个JQuery对象。用法：$(this).children()
    this才是代表一个元素，用法
    <li id="jq1" onclick="danji(this)">11</li>
    <li id="jq1" onclick="danji(this)">22</li>
    <li id="jq1" onclick="danji(this)">33</li>
    function danji(t){
    alert($(t).text());
    }
    ($(t).eq(0).offset().left);

    DOME:
    <a   id="lanmu"  onMouseOver="seover({$vo.id},this)" 
    --JS--
	function seover(id,t){
    var juli=parseFloat($(t).eq(0).offset().left);
###2.大型网站系统架构演化之路
     https://my.oschina.net/yuanxulong/blog/322626?p=1
     讲的是如何从一个小网站走向大型，自动化的网站的发展道路
     从开始的应用，文件，数据分离和数据库读写分离，到缓存，到负载均衡技术等。Docker技术
###3.了解新技术-CSDN学院
    http://edu.csdn.net/huiyiCourse/index/1/2#opencourse_area
    公开课，对于新技术的入门认识。
###4.图灵搜索，为程序员服务的搜索引擎

###5.web App 像素单位rem
    它就是一个相对单位   
    rem能等比例适配所有屏幕
    rem是通过根元素进行适配的，网页中的根元素指的是html我们通过设置html的字体大小就可以控制rem的大小。
    html{
        font-size:20px;
    }
	.btn {
	    width: 6rem;
	    height: 3rem;
	    line-height: 3rem;
	    font-size: 1.2rem;
	    display: inline-block;
	    background: #06c;
	    color: #fff;
	    border-radius: .5rem;
	    text-decoration: none;
	    text-align: center;    
	}
     .btn  120px*60px
    资料网址 http://isux.tencent.com/web-app-rem.html

###6.H5
     常用开发工具Hbuilder AND APICloud
     框架MUI AND AUI
###7.Vue.js初级认识
    1.数据绑定
    <div id="app">
    {{ message }}
    </div>
    --JS--
    new Vue({
    el:'#app',
    data: {
        message:'Hello World!'
    }
    });
    2.v-model--根据输入框 input 的改变而改变
     <p>{{ message }}</p>  {{* message }}
     <input v-model="message">
    3.列表
	<div id="app">
	  <ul>
	    <li v-for="todo in todos">
	      {{ todo.text }}
	    </li>
	  </ul>
	</div>
     --js--
	 new Vue({
	  el: '#app',
	  data: {
	    todos: [
	      { text: '菜鸟教程' },
	      { text: 'www.runoob.com' },
	      { text: 'www.w3cschool.cc' }
	    ]
	  }
	})
    4.数据连接
	 <li v-for="item in items">
	    {{ parentMessage }}  {{ $index }} - {{ item.message }}
	  </li>
     --JS--
     data: {
    parentMessage: '菜鸟教程官网',
    items: [
      { message: 'www.runoob.com' },
      { message: 'www.w3cschool.cc' }
    ]
    }
     {{ $index }}索引

    5.IF判断
	  <div v-if="Math.random() > 0.5">
		  随机数大于 0.5
		</div>
		<div v-else>
		  随机数不大于 0.5
		</div>
  		--js--
		new Vue({
		  el: '.app'
		})
