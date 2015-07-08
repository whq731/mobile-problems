http://stackoverflow.com/questions/3508605/css-transition-height-0-to-height-auto/


类似这个的描述
在当当单品页和详情页 nav导航条 需要设置一个transition 动画
Height 0 -> 50px
展开和收起

某种情况下 进入页面 点击按钮加上class
safari debug发现 height不会计算变为新的高度
虽然会有重绘出现 但是高度不会展开

最后发现此种情况出现 都是有单品轮播图最后一个张左滑 跳转到单品详情造成的
当回退后 点击展开收起 js执行 class增加 但是动画不执行
当滑动下轮播图 或者轮播图自动计时滑动后 动画就出现
怀疑是跳转时 轮播图的滑动绘制任务并未结束 任务队列里无法执行后续动画
当将iscroll的useTransition 设为false时
此种情况不再出现
暂时只能确定是轮播也同样使用了transition 当传入gpu渲染时 页面跳转导致未清空任务队列 
