## JavaScriptCore源码分析，这里是结构原理分析，源码注释在[code](https://github.com/luyigit/javascriptcore-analyse)里



## JavaScriptCore源码分析

### 编译器
```markdown
编译器包括：词法分析器，语法分析器，遍历器，转换器，代码生成器

词法分析器：递归下降和运算符优先级混合式；状态机处理递归下降。flex

语法分析器：上下文无关语法及分析；自顶向下分析（LL(1)）；自底向上分析（LR分析法）；bison
所谓的 LL(1) ，第一个 L 表示从左向右扫描输入流，第二个 L 表示每一步展开的时候取中间句子中左边第一个非终结符进行展开，括号里面的 1 表示每次只读入 1 个符号，每次只利用这 1 个符号的信息来挑选产生式。

遍历器：

转换器：

代码生成器：NASM（The Netwide Assembler）

```

下面分别分析上述过程在JavaScriptCore的实现
### 词法分析器
### 语法分析器

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/luyigit/javascriptcore-analyse/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
