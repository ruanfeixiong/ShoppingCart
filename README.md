# ShoppingCart
##主题：仿淘宝的购物车
######个人网址：www.zerovoid.cc（主机暂未到位）
######版权：安卓编程吧，绯若虚无编写；（有问题可以到贴吧发帖）
######博客地址：http://blog.csdn.net/freegf
######安卓编程吧：http://tieba.baidu.com/f?kw=%E5%AE%89%E5%8D%93%E7%BC%96%E7%A8%8B


##一、购物车的通用元素；

###1、展示购物车列表的界面；

1）group显示商铺名称(StoreName)；

2）child的显示商品名称(GoodsName)、规格（Specification）、数量（Quantity-qty）;

3）商品详情和商铺详情，属于商品的内容，不放在购物车实现中，（未实现）；

4）结算按钮、选中的总价和数量、购物车商品的总数量；

5）清空购物车和编辑全部（暂未实现）；

6）失效列表（按需求定，需要服务端配合，所以暂时不加入）；

7）当商品为0时，显示购物车为空的界面；

8）当网络异常时，显示网络异常的界面（暂未实现）；

###2、界面的改变

1）全选、组选、单选；

2）删除商品，child、group；

3）商品数量的改变、商品规格的改变；（改变方式是变化的，比如使用新的编辑界面、底部弹出规格列表等，规格部分的界面未实现）；

###3、数据的改变

1）修改商品数量；

2）修改商品规格；

3）删除商品；

4）增加商品；（商品部分调用的接口）

5）获取选中商品的总价和数量；

6）获取购物车商品的总数量；

###4、逻辑部分；

1）选择的逻辑

2）增删改查的逻辑

3）联动部分，当选中、删除的操作的时候，选中的数量、总价都会发生变化；需要设置观察者来监视状态变化，及时作出改变；

4）结算的时候，可能需要将购物车中的数据传递给下一个订单界面（具体传递的是什么，是不确定的）；

###5、变化部分；

1）数据；

是否需要和服务端同步？如果不需要，则数据从本地获取；

如果和服务端同步，则数据从服务端获取；

无论是服务端返回的JSON格式，或者是购物车的数据结构，都是变化最大的；（还是通过更换适配完成，但是基本操作已经封装到BIZ中）

2）child

商品的参数（数量、规格、删除键）的展示方式肯定是不同的，可以通过更换适配器来解决；

3）无论怎么变，所有变量的非空判断都要做到位；




