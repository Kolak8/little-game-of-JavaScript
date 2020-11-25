## 项目说明

---


### 游戏说明

    本游戏是经典的贪吃蛇游戏，通过点击开始游戏按钮可以开始游戏
    操作：通过 ↑ ↓ ← → 键来控制贪吃蛇的行走路线
    游戏规则: 1、撞到墙体或者自己身体则游戏结算，回到初始界面
             2、撞到苹果则会变长一个单位，苹果重新刷新
             3、游戏过程中点击游戏界面会出现三角启动按钮同时暂停游戏
             4、再次点击三角启动键可以继续开始游戏
             5、游戏过程会不断累积分数，吃到一个苹果加一分

---
### 对象

    1.Square: 这是食物和蛇的组成部件，可以看作是蛇的父一级构造函数
                <属性>
                    x：横坐标
                    y：纵坐标
                    class： 方块的CSS类
                    viewContent: 方块对应的Dom元素节点
                    parent:方块的父级Dom节点

                <方法>
                    create: 创建一个方块节点
                    remove: 清除一个方块节点
    2.Snake : 这个是蛇的整体，由多个Square对象组成

                <属性>
                    head: 存储蛇头的位置
                    tail: 存储蛇尾的信息
                    pos(数组): 存储蛇身上每一块的位置
                    directionNum: 存储蛇走的方向，用一个对象表示

                <方法>
                    init : 初始化蛇对象
                    getNextPos：用来获取蛇头的下一个位置对应的元素，要根据元素做不同的事情
                    strategies：处理碰撞后要做的事

    3.Food ：食物对象，由一个Square对象组成

                <属性>
                    include : 判断食物的位置是否在蛇身上

                <方法>
                    createFood: 随机生成一个食物
                    继承方法：
                    create: 创建一个食物方块节点;
                    remove:清除食物方块节点; 

    4.Game :  游戏对象，编写游戏规则

                <属性>

                        timer: 计时器
                        score: 得分

                <方法>

                        init: 初始化游戏
                        start: 开启游戏

                        over: 结算游戏

### 额外的函数/事件



