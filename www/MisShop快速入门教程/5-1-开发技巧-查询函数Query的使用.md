Query的函数说明

 Query的函数用法（以用户表(ds的泛型为用户)为例）：

 query.ds.id ------------通过用户id查找

 query.ds.名称  ------------------通过用户的名称查找

 query.ds.名称.like ----------------通过用的的名称进行模糊查询（例如：输入 李 查询所有名称中含有“李”的用户信息）

 query.ds.生日  ----------------通过用户的生日查找

 query.ds.生日.It -----------------通过用户的生日查找,查找出生日小于输入值的所有用户信息

 query.ds.生日.gt ---------------通过用户的生日查找,查找出生日大于输入值的所有用户信息

 query.ds.生日.equals -----------------通过用户的生日查找,查找出生日等于输入值的所有用户信息

 query.ds.生日.le -----------------通过用户的生日查找,查找出生日小于等于输入值的所有用户信息（query.ds.生日.小于等于 的用法和它一样）

 query.ds.生日.ge ------------------通过用户的生日查找,查找出生日大于等于输入值的所有用户信息（query.ds.生日.大于等于 的用法和它一样）

 query.ds.角色.in --------------------通过角色来查询对应用户，此方法的前提是这个 角色字段为多选 ，查询结果为满足多选角色中的一个或者多个的用户

 Query 的函数进阶

 Query.combo(判断条件,是非判断)；

  如下图：

![1.png](https://upload-images.jianshu.io/upload_images/12920178-b48e0b8d2015a4fc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


 B2,C2,D2均为标签式是非项按钮控件，点击后该单元格值为ture,再次点击变为false .初始值为flase;

当 多个query.combo（）函数在同一区域(组)中时，它所查询出来的为满足当前区域中任一函数的用户信息。

当点击B2 C2 D2 某个或者多个按钮时，点击查询 即可查出对应的用户信息。

在query,combo(判断条件，是非判断)中，除了可以以以上形式进行，还可以通过query.combo(ds.id>E2)来判断，E2为输入框。如下图：

![2.png](https://upload-images.jianshu.io/upload_images/12920178-03799b09d3f1a0bf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


当B3,C3,D3,E3一起用时需要给E3的是非判断项进行是否使用判断；

如下图：当多个 query.combo() 函数不在同一区域(组)时 。查询出的结果为同时满足两个区域中条件的用户信息。结果为：用户的性别为男，并且部门为财务部的用户信息。

![3.png](https://upload-images.jianshu.io/upload_images/12920178-45d7451d1fe82c8b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


当需要查询的内容为区间时可以选择上面的方法，还可以这样，如下图：
![4.png](https://upload-images.jianshu.io/upload_images/12920178-f99b979cc5695a2e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


就是将俩个需要查询的内容放入区域中，然后实现区间查询 这种的需要点击查询按钮 或者对当前区域绑定立即执行属性。
