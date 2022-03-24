_**像chrome的`<input type="number">`一样限制输入数字输入**_

能发现这个包，相信已经真实地遇到这个坑了吧～  
问题1：直接`<input type="number">`不行吗?  
不行，这个依赖于浏览器自己的实现

问题2：监听input，然后剔除掉非数字的输入，再赋值回去不行吗？  
行，但是有两个缺陷。第一个是直接重新赋值会移动光标。  
比如：当你输入了123，然后将光标移动到1后面，此时再输入一个字母 `a`，光标就定位到最后了  
第二个是mac下切换成中文输入，还是能输入非法内容，window没测过

其实这个包，虽然叫做NumberInput，可以拿来做其他限制用。demo.html里展示了几个例子  
没怎么测过，尤其是兼容性。有问题欢迎自己解决，或者告诉我