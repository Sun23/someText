# react note

#### react 组件的生命周期 
- 生命周期三个状态
  - Mounting 插入真实Dom
  - Updating 正在被重新渲染
  - Unmounting 已移除真实Dom
  
- 状态处理函数
  - componentWillMount()  在渲染前调用
  - componentDidMount() 在第一次渲染后调用，只在客户端。之后组件已经生成了对应的DOM结构，可以通过this.getDOMNode()来进行        访问。 如果你想和其他JavaScript框架一起使用，可以在这个方法中调用setTimeout, setInterval或者发送AJAX请求等操作(防止异部        操作阻塞UI)。
  - componentWillUpdate(nextProps, nextState) 在组件接收到新的props或者state但还没有render时被调用。在初始化时不会被调        用。
  - componentDidUpdate(preProps, preState) 在组件完成更新后立即调用。在初始化时不会被调用。
