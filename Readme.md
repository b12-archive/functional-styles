<h1 align="center">
  <img
    alt="functional-styles"
    width="596"
    height="472"
    src="https://cdn.rawgit.com/studio-b12/functional-styles/0b7be24/logo.svg"
    id="/"
  />
</h1>

**The functional alternative to CSS**




&nbsp;

##                                                                 <a id="/tldr" >TL;DR                                                                      </a>

This is not a library or something. It’s just an idea that will change the world.

The idea is simple. Instead of one big fat CSS scope full of name conflicts and inheritance chains you compose your styles out of little functions.

As well as being super modular, composable, testable and isolated functions have one more advantage. They can take options.

So instead of this CSS:

```css
/*  • styles.css  */
.my-class {
  color: blue;
}

/*  • red-theme.css  */
.red-theme .my-class {
  color: red;
}
```

You write this beautiful, concise JS:

```js
//  • styles.js
export myClass = ({color: blue}) => ({  // Defaults are totally optional!
  color,
});

//  • red-thing.js
const theme = {color: red};

<h1 style={myClass(theme)}>
  I’m very red!
</h1>
```

Fair enough – that was nothing new to some of you. But here comes the exciting part:

[snare drum rolling…]

Thanks to [git.io/orthodox](http://github.com/studio-b12/orthodox) you can also render a CSS module with the same function!

```js
const restyle = require('restyle');

restyle({
  '.my-class': myClass(theme),
});
//» `.my-class {
//    color: red;
//  }`
```

In fact it’s even more flexible. Thanks to orthodox functional styles fit in seamlessly with [*Cycle.js*](https://github.com/cyclejs/cycle-core), [*virtual-dom*](https://github.com/Matt-Esch/virtual-dom), [*Free style*](https://github.com/blakeembrey/free-style) and every other hotness!




&nbsp;

##                                                                 <a id="/note" >Note                                                                       </a>

The idea is being tested out on a big production-ready style framework. It still needs some polishing – we’ll post concrete examples as soon as they are ready!

Meanwhile, don’t hestitate to [weigh in](https://github.com/studio-b12/functional-styles/issues)!




&nbsp;

##                                                              <a id="/license" >License                                                                    </a>

[MIT](./License.md) © [Studio B12 GmbH](http://github.com/studio-b12)
