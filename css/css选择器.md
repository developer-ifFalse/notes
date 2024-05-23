#### 选择器
    id选择器（#box），选择id为box的元素
    类选择器（.one），选择类名为one的所有元素
    标签选择器（div），选择标签为div的所有元素
    后代选择器（#box div），选择id为box元素内部所有的div元素
    子选择器（.one>one_1），选择父元素为.one的所有.one_1的元素
    相邻同胞选择器（.one+.two），选择紧接在.one之后的所有.two元素
    群组选择器（div,p），选择div、p的所有元素

    伪类选择器
        :link ：选择未被访问的链接
        :visited：选取已被访问的链接
        :active：选择活动链接
        :hover ：鼠标指针浮动在上面的元素
        :focus ：选择具有焦点的
        :first-child：父元素的首个子元素
    
    伪元素选择器
        :first-letter ：用于选取指定选择器的首字母
        :first-line ：选取指定选择器的首行
        :before : 选择器在被选元素的内容前面插入内容
        :after : 选择器在被选元素的内容后面插入内容
    
    属性选择器
        [attribute] 选择带有attribute属性的元素
        [attribute=value] 选择所有使用attribute=value的元素
        [attribute~=value] 选择attribute属性包含value的元素
        [attribute|=value]：选择attribute属性以value开头的元素

#### 优先级
    !important > 内联 > ID选择器　> 类选择器　>　标签选择器

#### 继承属性
    可以继承的属性：
        1.字体属性
            font:组合字体
            font-family:规定元素的字体系列
            font-weight:设置字体的粗细
            font-size:设置字体的尺寸
            font-style:定义字体的风格
            font-variant:偏大或偏小的字体
        
        2.文本属性
            text-indent：文本缩进
            text-align：文本水平对刘
            line-height：行高
            word-spacing：增加或减少单词间的空白
            letter-spacing：增加或减少字符间的空白
            text-transform：控制文本大小写
            direction：规定文本的书写方向
            color：文本颜色
        
        3.列表属性
            list-style-type：文字前面的小点点样式
            list-style-position：小点点位置
            list-style：以上的属性可通过这属性集合