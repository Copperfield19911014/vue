# vue加载时初始化
## 一、初始化方法：
	1.initMixin(Vue)
	2.stateMixin(Vue)
	3.eventsMixin(Vue)
	4.lifecycleMixin(Vue)
	5.renderMixin(Vue)
### 初始化方法解析
	>>>initMixin(Vue)
	...
	initLifecycle(vm); //初始化生命周期
    initEvents(vm); //初始化事件
    initRender(vm); //初始化渲染
    

