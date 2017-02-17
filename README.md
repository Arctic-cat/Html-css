html和css知识笔记

=====  




###基本标签

显示单行代码：`<code></code>`  

显示大段代码：`<pre></pre>`  &ensp;&ensp;  

换行：`<br>`   

空格： `&nbsp`  &ensp; 

  

在新窗口打开超链接：`<a  href="目标网址"  title="鼠标滑过显示的文本" target="_blank">链接显示的文本</a>` 




###表单标签  

```html  

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
<br>
####单选框和复选框：   

```html
<input   type="radio/checkbox"   value="值(1/2)"    name="名称"   checked="checked"/>  

```  

>**1.type:** 
>当 `type="radio"` 时，控件为**单选框 ** 
   
>当 `type="checkbox"` 时，控件**为复选框**  

>**2.value：**  
>提交数据到服务器的值（后台程序PHP使用） 

>**3.name：**  
>为控件命名，以备后台程序 ASP、PHP 使用

>**4.checked：**  
>当设置 checked="checked" 时，该选项被默认选中  

####下拉列表框：  
```html  
<select>
      <option value="看书">看书</option>
      <option value="旅游 selected="selected">旅游</option>
      <option value="运动">运动</option>
      <option value="购物">购物</option>
</select>  
```  
>**1.value：**
>提交值
>**2.selected="selected"：**
>设置selected="selected"属性，则该选项就被默认选中  

####label标签： 
```html  
<label for="控件id名称">  
```  
注意：标签的**for 属性中的值**应当与相关控件的**id 属性值**一定要相同。

###CSS样式  
**嵌入式**：直接写在现有的html标签中  
**内联式**：写在当前文件中  
**外联式**：写在单独的一个文件中  

####元素分类--**块级元素**  
在html中`<div>`、`<p>`、`<h1>`、`<dl>`、`<form>`、`<ul>` 和`<li>`就是块级元素。设置`display:block`就是将元素显示为块级元素。如:  
```css
a{display:block;}
```  
块级元素特点：  
1、很霸道，一个块级元素独占一行   
2、元素的高度、宽度、行高以及顶和底边距都可设置    
3、默认情况下，元素宽度是它本身父容器的100%  

####元素分类--**行级元素** 
在html中，`<span>`、`<a>`、`<label>`、`<strong>` 和`<em>`就是典型的行级(inline)元素。块状元素也可以通过代码`display:inline`将元素设置为内联元素。  
如:  
```css
div{
     display:inline;
 }
```  
  
####元素分类--**行级块级元素**  
同时具备行级元素、块级元素的特点，`display:inline-block`就是将元素设置为内联块状元素。`<img>`、`<input>`标签就是这种内联块状标签。 
inline-block元素特点：  
1、和其他元素都在一行上；  
2、元素的高度、宽度、行高以及顶和底边距都可设置  

####层模型--**绝对定位:**  
```css  
position:absolute;  
left:100px;  
top:50px;  
```  
原理：将元素从文档流中拖出来，然后使用left、right、top、bottom属性相对于**其最接近的具有定位属性的父包含块**进行绝对定位。如果不存在这样的包含块，则相对于body元素，即相对于**浏览器窗口**  



####层模型--**相对定位:** 
```css  
position:relative;  
left:100px;  
top:50px;  
```  
原理：通过left、right、top、bottom属性确定元素在正常文档流中的偏移位置。相对定位完成的过程是首先按static(float)方式生成一个元素(并且元素像层一样浮动了起来)，然后相对于以前的位置移动，移动的方向和幅度由left、right、top、bottom属性确定，**偏移前的位置保留不动**

####层模型--**固定定位**  
```css  
position:fixed;  
left:100px;  
top:50px;  
```  
它的相对移动的坐标是视图（屏幕内的网页窗口）本身。由于视图本身是固定的，它不会随浏览器窗口的滚动条滚动而变化，**右下角广告最爱**  

###网页布局基础  
####**自动居中1列布局**  
1.将要居中的页面元素用`<div>`包裹起来  
2.设置包裹层的样式(要点是margin左右间距设为auto)：`{width:1000px;margin:0 auto}`  

####**横向多列布局**  
设置了float的元素会对紧邻其后的元素造成影响，后者紧挨前者显示（经常造成布局乱七八糟，因此需要“**清除浮动**”）  
清除浮动的两种方法（对**受到浮动影响**的元素设置）：  
1.`clear both`
2.`width:100%`(或固定宽度)+`overflow:hidden`(多用于清除父包含块的浮动影响)  
  
横向多列布局基本方法：  
1.子元素使用float浮动，注意父包含块要清除浮动  
2.使用margin属性设置间距












