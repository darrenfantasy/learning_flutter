# Json转Dart Model类

官方推荐的**[json_serializable package (opens new window)](https://pub.dartlang.org/packages/json_serializable)**包。 它是一个自动化的源代码生成器，可以在开发阶段为我们生成 JSON 序列化模板，这样一来，由于序列化代码不再由我们手写和维护，我们将运行时产生 JSON 序列化异常的风险降至最低。

借助 [https://caijinglong.github.io/json2dart/index.html](https://caijinglong.github.io/json2dart/index.html) 这个网站，来生成你需要的

copy过去之后， 会报错，先不用处理

命令行执行

```jsx
flutter packages pub run build_runner build
```

这触发了一次性构建，我们可以在需要时为我们的 Model 生成 json 序列化代码，它通过我们的源文件，找出需要生成 Model 类的源文件（包含@JsonSerializable 标注的）来生成对应的 .g.dart 文件。一个好的建议是将所有 Model 类放在一个单独的目录下，然后在该目录下执行命令。

虽然这非常方便，但如果我们不需要每次在Model类中进行更改时都要手动运行构建命令的话会更好。

参考 [https://book.flutterchina.club/chapter11/json_model.html#自动化生成模板](https://book.flutterchina.club/chapter11/json_model.html#%E8%87%AA%E5%8A%A8%E5%8C%96%E7%94%9F%E6%88%90%E6%A8%A1%E6%9D%BF)

[https://blog.csdn.net/xudailong_blog/article/details/95168949](https://blog.csdn.net/xudailong_blog/article/details/95168949)