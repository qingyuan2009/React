#   React 特点

1.  不使用模板
2.  不是MVC框架
3.  响应式
4.  轻量级js库

#   原理：

*   虚拟DOM, React把DOM抽象成为一个JS对象，用diff算法操作JS对象，而不是直接操作DOM，增加performance。
    对界面真正发生变化的部分进行实际的DOM操作
*   逐层次的高效节点比较

#   开发环境

*   react.js    核心文件    
*   react-dom.js    渲染页面的DOM   
*   babel.js    翻译浏览器 ES6->ES5, JSX语法转换为javascript; 现今浏览器的兼容

下载：
    1.  npm i react --save
    2.  npm i react-dom --save
    3.  npm i babel-standalone --save

##  创建package
C:\Users\i035299\Documents\GitHub\React\demo001>npm init -y
##  下载react
C:\Users\i035299\Documents\GitHub\React\demo001>npm install react --save
完成后项目中会多出node-modules
##  下载react-dom
C:\Users\i035299\Documents\GitHub\React\demo001>npm install --save react-dom
##  下载babel
C:\Users\i035299\Documents\GitHub\React\demo001>npm i babel-standalone --save

# 注释

    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script src="node_modules/react/umd/react.development.js"></script>
    <script src="node_modules/react-dom/umd/react-dom.development.js"></script>
    <script src="node_modules/babel-standalone/babel.min.js"></script>
    </head>
    <body>	
        <!--创建 DOM Root, 一个页面需要一个root，这样可以被React进行管理-->
        <div id="demoReact">
        </div>
        <script type="text/babel">
            // jsx dom 注释 {/**/}
            let myDom=<div>
                        {/* jsx的注释 */}
                        Hello World
                      </div>;
            ReactDOM.render(myDom, document.getElementById("demoReact"));
        </script>
    </body>
    </html>

# 安装 marketplace live server
安装后，右击HTML页面，使用 Open with live server 打开

# 外部js文件
用Open with live server 执行jsxDocuments-> 005_jsxDemo.html

# 组件
高耦合，低内聚：把逻辑紧密的内容放在一个组件当中，把不同组件的依赖关系尽量弱化，每个组件尽可能的独立

组件中的内容：
1. 构建方式
2. 组件的属性
3. 生命周期

