<!-- YAML
added: v0.1.25
changes:
  - version: v6.0.0
    pr-url: https://github.com/nodejs/node/pull/5348
    description: 现在将非字符串作为 `path` 参数传入会抛出异常。
-->

* `path` {string}
* `ext` {string} 可选的文件扩展名。
* 返回: {string}

`path.basename()` 方法返回 `path` 的最后一部分，类似于 Unix 的 `basename` 命令。 
尾部的目录分隔符将被忽略，参阅 [`path.sep`]。


```js
path.basename('/foo/bar/baz/asdf/quux.html');
// 返回: 'quux.html'

path.basename('/foo/bar/baz/asdf/quux.html', '.html');
// 返回: 'quux'
```

如果 `path` 不是字符串、或给定了 `ext` 但不是字符串，则抛出 [`TypeError`]。

