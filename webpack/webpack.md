### webpack
1. 入口 entry  
可以是对象。也可以是直接一个入口
2. 出口 output  
filename对应改为[name]/[name].js
3. loader  
babel-loader,  css-loader, style-loader, postcss-loader      
html-loader, url-loader （处理图片）, file-loader 字体
4. 插件plugins  
html-webpack-plugin, clean-webpack-plugin, webpack的HotModuleReplacementPlugin
5. 模式mode. (开发和生产)  
mode: development , production