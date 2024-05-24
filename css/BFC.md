#### BFC
    BFC，块级格式化上下文，目的是形成一个相对于外界完全独立的空间，让内部的子元素不会影响到外部的元素

#### 触发条件
    - 根元素，html
    - 浮动元素：float值为left、right
    - overflow值不为visible，为auto、scroll、hidden
    - display的值为inline-block、inltable-cell、table-caption、table、inline-table、flex、inline-flex、grid、inline-grid
    - position的值为absolute或fixed

#### 应用场景
    - margin合并
    - 高度塌陷
    - 自适应多栏布局
