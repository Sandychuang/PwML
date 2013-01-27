PwML
====

**open source Programming with Mother Language**

**开源母语编程**

前一阵子看代码看得双眼干涩、头脑发烫，尤其是英文自定义函数名，太短了不清楚意思，想清楚表达意思就要忍受长长的名字，而且类似的函数还不只一个，所有的自定义函数为了清楚表达含义，都很长、很长，看得人只想吐，于是萌发了用中文做函数名的念头，再进一步，用中文、标点符号、数字来写代码。

首先介绍一下背景知识，英文是一种拼音语言，中文是一种拼义语言，拼义语言这个概念是由香港中文大学心理学教授 [张学新] [1] 根据其对汉字的研究结果提炼出的一个概念，大概的理解就是英语是基于不同语音的组合，而中文则是基于不同含义的组合，详细的理论可以参考他的2012年发表在[《科学通报》](#http://csb.scichina.com:8080/kxtb/CN/volumn/volumn_6364.shtml) 的论
文
[《汉字拼义理论》](#http://www.kuaipan.cn/index.php?ac=file&oid=6054104296062993) 和
[《顶中区N200: 一个中文视觉词汇识别特有的脑电反应》](#http://csb.scichina.com:8080/kxtb/CN/abstract/abstract506586.shtml#)

[1]: http://blog.sina.com.cn/s/articlelist_1787161060_0_1.html

  前面提到英文程序中的函数名称过长的问题，事实上用中文做函数名有先天优势，两个英文字母对应一个中文字符，两个中文字符组成的词语可以很清晰地表达一个概念。但是对应存储大小的四个英文字母却基本不可能表达清楚同样概念。

  所以甚至如果你精通古代文言文，你还可以把函数名称简化为一个汉字字符--只要你自己能读懂，再举个例子，比如 **define** 这个关键字，直译为现代中文是 **定义** ，原来要6个字节，现在变成了4个字节，那么把它翻译为一个字节的古文言文单字该怎么翻？就是 **名** ，《道德经》的第一句大家肯定都很熟悉：“道可道，非常道，名可名，非常名”，这里的“名”就是命名、定义的意思，看看下面列出的这三种形式的代码的比较：

    英文代码：
    > define function1()
    
    现代中文代码：
    > 定义 函数1()
    
    文言文代码：
    > 名 函数1()

除了函数名称，关键字以及语法也可以以文言文的简约方式来定义，这样你写的程序就是文言文程序了，这样一想是不是觉得很有趣？

  就像上面提到的“函数”这个概念，中文两个字符很清楚，只占4个比特的存储空间，但是英文的“ function”就需要用到两倍个数的英文字符，要占8个比特的存储空间。

  英语这种基于语音的特点，使得英文天生只能是一种一维线性文字，也就是说英文适合于听觉处理，而不适合视觉处理，而中文则恰恰相反，中文是一种基于视觉的二维文字，中文不需要那么多单独的读音去区分，因为它是各种基本概念的组合，中文的同音字特别多，就是因为中文主要依赖于视觉的识别。就像现在比较流行的二维条形码，因为设计者受拼音文字影响，所以设计成只适合机器识别的方式，人却无法直接看懂，其实后续的二维条形码可以设计为中文的样式，这样机器和人都可以阅读，这其实是中文的一种巨大优势。

  因为程序员不可能依靠耳朵去听代码，只能是依靠视觉去看代码，所以在这种使用场景下，用中文作为程序语言要优于英文。

  根据上面的分析，我们发现使用中文编程可以有效缩小源代码的规模，而且项目越大，这种效果越明显，如果使用现代中文的方式进行写作，源码体积可缩小 1/3 到 1/2，如果使用文言文的方式进行编程，源码体积可在现代中文的基础上再次缩小 1/3 到 1/2（当然这个只是粗略的估计，具体的数据等我完成源代码翻译器再进行精确的统计）。

有人可能会担心输入的工作量会增加，现在的开发环境一般都会有非常完善的自动完成功能，经过我的试验，使用 Emacs 编辑环境中的自动完成插件，输入的工作量跟使用英文基本持平，所以不必担心这一点。

目前中国国内有两种中文程序语言，一种是易语言，一种就是中文化的PYTHON，前者属于商业化软件，不适合进行探索性试验，后者则受限于 Python 语言本身的能力，也不太适合，在了解了 Common Lisp 的一些特性后，忽然发现 LISP 是最适合做开源母语开发的基础平台，首先是 Lisp 语言强大到逆天的宏能力，具备自定义一种新语言的能力，其次是全部开源的开发平台环境，再加上 Lisp 本身的迭代开发模式，非常适合我们用它来进行母语编程的探索。

初步计划是这样：先尝试搞一个中文编程的环境出来，然后再选择几种其他非英文类型的语言进行试验，这样每个国家的程序员都可以使用自己的母语编程了，程序员写的程序也可以。
