## JS语法 {#vue-组件命名}

#### 请**尽量**使用ES6及其以上的语法

原因：ES6于2015年6月发布，距今已一年半时间，各大浏览器对其支持度已经越来越高。且本该项目还有webpack对其进行转换，所以不存在兼容性问题。ES6的某些特性解决了ES5的很多痛点，能更容易地解决某些复杂性高的问题，提高开发效率。

**（1） let 取代 var **原因：var存在变量提升

**（2） 使用箭头函数 **原因：使用箭头函数，函数里的this就是外层的this,无需用call/apply/bind/let self=this来改变this指向,传值时能少走弯路

**（3） 使用模板字符串  **使用 \`\` 将整个字符串包裹起来，而在其中使用 ${} 来包裹一个变量或者一个表达式，如：** **

    // es5
    var a = 20;
    var b = 30;
    var string = a + "+" + b + "=" + (a + b);

    // es6
    let a = 20;
    let b = 30;
    const string = `${a}+${b}=${a+b}`;

**（4） 判断时候相等时，请使用 ‘===’ 如： this.length === 0  原因：===保证值和类型的相等，减少不必要的校验**

**（5） 使用解析结构 **原因：代码简洁，减少不必要的代码量，如：

```
// es5
var loading = props.loading;
var clicked = props.clicked;

// es6
let { loading, clicked } = props;
// 给一个默认值，当props对象中找不到loading时，loading就等于该默认值
let { loading = false, clicked } = props;
```



