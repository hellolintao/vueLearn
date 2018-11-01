# 表单与`v-model`
## 6.1 基本用法
### 文本输入框
```
<div id="app">
	<input type="text" v-model="message"/>
	<h2>{{ message }}</h2>
</div>
<script>
	var app = new Vue({
		el:"#app",
		data:{
			message:""
		}
	});
	// 此时，实例中的message和input标签中的message已经绑定了，一个数据更新，另外一个数据也会更新，同时，h2元素中的message也会及时更新。
</script>
```
### 单选按钮
```
<!-- 单选模式可以直接使用数据绑定 -->
<div id="app">
	<input type="radio" :checked="picked">
</div>
<script type="text/javascript">
	var app = new Vue({
		el:"#app",
		data:{
			picked: true
		}	
	});
</script>

<!-- 互斥模式可以使用v-model -->
<div id="app">
	<input type="radio" value="js" v-model="picked"><label>js</label>
	<input type="radio" value="html" v-model="picked"><label>html</label>
	<input type="radio" value="css" v-model="picked"><label>css</label>

	<p>您选择的是：{{ picked }}</p>
</div>
<script type="text/javascript">
	var app = new Vue({
		el:"#app",
		data:{
			picked:"js"
		}	
	});
</script>
```
### 复选框
```
<!-- 可以单独使用 -->
<div id="app">
	<input type="checkbox" v-model="checked">
</div>
<script type="text/javascript">
	var app = new Vue({
		el:"#app",
		data:{
			checked:true
		}	
	});
</script>

<!-- 可以组合使用 -->
<div id="app">
	<input type="checkbox" value="js" v-model="picked"><label>js</label>
	<input type="checkbox" value="html" v-model="picked"><label>html</label>
	<input type="checkbox" value="css" v-model="picked"><label>css</label>

	<p>您选择的是：{{ picked }}</p>
</div>
<script type="text/javascript">
	var app = new Vue({
		el:"#app",
		data:{
			picked:["js","html"]
		}	
	});
</script>
```
### 选择列表
## 6.2 绑定值
## 6.3 修饰符