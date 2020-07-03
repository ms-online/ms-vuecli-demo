# vuecli-demo

## lesson10 生命周期钩子函数

beforeCreate():这时实例还没有被创建，所以无法知道 data，也不能用 watch 监听；

created()：这时实例已经创建，可以得到 data，调用 watch，但是页面显示空白

beforeMount()：页面挂载前，此时页面显示空白，但是 render 函数被首次调用；

mounted()：页面挂载了，这时可以看到内容，也可以访问 dom；

beforeUpdate()：数据更新前，也就是虚拟 DOM 打补丁前；这时访问到的还是原有的 DOM；

updated()：数据已经更新完毕，重新渲染页面。

beforeDestroy()：离开页面之前被调用，清除定时器，或第三方的一些 DOM 结构；

destryed()：实例已经完全被销毁。
