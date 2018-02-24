# Extensions

Extensions allow you to extend an existing class or value type.

In an extension, you can declare and define everything you could when initially
declaring a class or value type, this includes methods, initializers, type
methods and protocol conformances.

>!N Adding instance varibales is deperecated as of 0.5.4 and will be
>!N removed in an upcoming version of Emojicode.

## Extending

The syntax is:

<pre class="syntax">
$extension$-> 🐋 $type-identifier$ $type-body$
</pre>

You can also extend classes from other packages. For example:

```
🏁 🍇
  😀 😈 🔤James Tiberius Kirk🔤
🍉

🐋 🔡 🍇
  🌮 Reverses a string 🌮
  🐖 😈 ➡️ 🔡 🍇
    🍮 out 🔤🔤

    🔂 i ⏩ ➖ 🐔 🐕 1 -1 🍇
      🍮 out 📝 out 🍺 🐽 🐕 i
    🍉

    🍎 out
  🍉
🍉
```

## Circumvent circular dependencies

Extension can also be used to circumvent circular dependencies. Imagine this
problem:

```
🐇 🌕 🍇
  🍰 belongingTo 🌍
🍉

🐇 🌍 🍇
  🍰 moon 🌕
🍉

```

No matter how you order the class definitions, this example will not compile.

This problem can be solved using extensions:

```
🐇 🌍 🍇🍉

🐇 🌕 🍇
  🍰 belongingTo 🌍
🍉

🐋 🌍 🍇
  🍰 moon 🌕
🍉
```

Although extensions to classes are practically cost free it is not considered
good style to always “forward declare” classes to extend them later.
