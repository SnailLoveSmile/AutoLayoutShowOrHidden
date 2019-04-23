###开篇看下动画前的图片显示
![](https://upload-images.jianshu.io/upload_images/913244-2a3dc34faf7764f8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
`在此基础上我们将做红色蓝色逐个删除(或者修改约束)达到黄色向左移动的
效果`

 ##`首先预览下整体约束的构建`
![总体约束预览图](https://upload-images.jianshu.io/upload_images/913244-5cf65b7fe79fc397.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* `首先我们暂且忽略那些虚线的约束`
`红色View`距左20下0,宽高比为1.0, 高度设为50
`蓝色View`和`黄色View`约束和`红色View`一样
  
* `现在我们做虚线的约束`
1. `蓝色View`的约束: 距离父视图左为20约束优先级设为750, 即为下图的那条虚线
![蓝色View的约束图](https://upload-images.jianshu.io/upload_images/913244-49db9609ec0fe656.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![蓝色View距离父视图的虚线视图](https://upload-images.jianshu.io/upload_images/913244-8cf86bd202815ba4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
2. 为`黄色View`同样添加距离父视图左侧为20 的虚线约束, 步骤和`蓝色View`一致约束优先级同样也为`250`
3. 再为`黄色View`设置距离`红色View`左侧为20 的虚线约束, 约束优先级设置为`750`
 ![黄色视图优先级设置](https://upload-images.jianshu.io/upload_images/913244-5016fbb5c11b9c47.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

`现在我们就达到了删除红色View或者蓝色View视图整体视图左移效果`

### 如何不删除View设置hidden属性做到左移效果呢?

其实很简单了就,![注意下这里](https://upload-images.jianshu.io/upload_images/913244-b50ac2ba70419df9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

将左侧20这个约束优先级设置为`250`
此时你就会发现蓝和黄左移了, 是不是很简单
<>


[DEMO 链接](https://github.com/SnailLoveSmile/AutoLayoutShowOrHidden)

















