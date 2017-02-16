html和css知识笔记
======  

###基本标签
显示单行代码：`<code></code>`  
显示大段代码：`<pre></pre>`  &ensp;&ensp;  
换行：`<br>`   
空格： `&nbsp`  &ensp; 
  
在新窗口打开超链接：`<a  href="目标网址"  title="鼠标滑过显示的文本" target="_blank">链接显示的文本</a>` 

表单标签：  
```javascript  
<form>
    method="传送方式(post/get)" action="服务器存储文件(save.php)"
      <label for="username">用户名:</label>
      <input type="text"  name="username" id="username" value="" />
      <label for="pass">密码:</label>
      <input type="password"  name="pass" id="pass" value="" />    
      <input type="submit" value="确定"  name="submit" />
      <input type="reset" value="重置" name="reset" />
</form>    
```  







```javascript  

$(document).ready(function () {
    alert('hello world');
});  

```