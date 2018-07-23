## css
1. 盒子模型  
    css盒子模型有标准模型和怪异模型
    标准模型元素实际总用内容面积`(margin-left+padding-left+border-left-width)*2 + width`
    怪异模式的模型内容面积就是`width`
    模型的转换用`box-sizing`  `content-box`默认标准模式 （一般浏览器除ie低版本）`border-box`怪异模式
2. BFC概念	
	**BFC**	
		
	块格式化上下文（Block Formatting Context) 属于盒子模型布局的css渲染模式，指独立的渲染区域	
		
	**形成BFC条件**
	1. 浮动元素，float 除 none 以外的值； 
	2. 定位元素，position（absolute，fixed）； 
	3. display 为以下其中之一的值 inline-block，table-cell，table-caption； 
	4. overflow 除了 visible 以外的值（hidden，auto，scroll);		
	
	**BFC的特性**  
	
	1.  内部的Box会在垂直方向上一个接一个的放置
	2.  垂直方向上的距离由margin决定
	3.  bfc的区域不会与float的元素区域重叠。
	4.  计算bfc的高度时，浮动元素也参与计算
	5.  bfc就是页面上的一个独立容器，容器里面的子元素不会影响外面元素。
3. 布局(左边固定右边自适应或者左右固定中间自适应)
    1.  浮动定位 左边浮动宽度写死， 右边margin-left:固定宽度
    2.  绝对定位，左边绝对定位宽度写死，右边margin-left固定宽度
    3.  父元素display: flex，左边子宽度写死，右边flex:1,margin-left固定宽度
4. margin外陷的解决办法
    在父元素上加`:before{ content: ''; display: table/inline-block;  }`
5. 元素上下左右居中办法
    1. 绝对定位
    `margin: auto;
    top:0;width: 200px;
    left: 0;
    right:0;
    bottom: 0;
    position: absolute;`
    2. flex布局
    `display: flex;
    align-items: center;
    just-content:center;`
    3. 绝对定位+ margin
    `position: absolute;
     width:200px;
     top: 50%;
     left: 50%;
     margin-left: -100px;
     margin-top: -100px;`
6. css动画
 >       #ani{
 > 		    width: 200px;
 >		    height: 200px;
 >		    border-radius: 50%;
 >		    position: relative;
 >		    animation: gun 1s infinite alternate;
 >		    background-color: #f00;
 >		}
 >		@keyframes gun{
 >		    0%{
 >	            left:0;
 >		    }
 >	        100%{
 >		        left:100px;
 >		    }
 >		}