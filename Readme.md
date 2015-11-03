<h1 align="center">
  <img
    alt="functional-styles"
    width="404"
    height="472"
    src="https://cdn.rawgit.com/studio-b12/functional-styles/0b7be24/logo.svg"
    id="/"
  />
</h1>

**The functional alternative to CSS**




&nbsp;

##                                                                 <a id="/tldr" >TL;DR                                                                      </a>

This is not a library or something. It’s just an idea that will change the world.

The idea is simple. Instead of one big fat CSS scope full of name conflicts and inheritance chains (yuck!) you compose your styles out of little functions.

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
export myClass = ({color: blue}) => ({
  color,
});

//  • red-theme.js
import myClass from 'styles';

export default myClass({color: red});
```

The return value of each function can be [git.io/orthodox](http://github.com/studio-b12/orthodox) – this way you can use the styles with React, Cycle.js, virtual-dom and everything else!




&nbsp;

##                                                              <a id="/license" >License                                                                    </a>

[MIT](./License.md) © [Studio B12 GmbH](http://github.com/studio-b12)
