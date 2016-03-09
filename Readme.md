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




<a                                                         id="/tldr">&nbsp;</a>

## TL;DR

This is a library and CLI tool that will cure CSS development.

The idea is simple. Instead of one big fat scope full of name conflicts and inheritance chains, you compose your styles out of little pure JS functions.

Functions are extremely modular, composable, testable and debug-friendly. And they can take options. All the things we’ve always wanted in CSS, LESS and SASS.




<a                                                 id="/installation"></a>&nbsp;

## INSTALLATION

```sh
# Globally for a user:
npm install --global functional-styles

# …or locally for a project:
npm install --save-dev functional-styles
```

Note that you need *node 4.0+* to run the tool natively. But if you’re stuck on an older version, don’t worry! [Rumour has it](https://github.com/tomekwi/elm-live/issues/2#issuecomment-156698732) that you can transpile the code to ES5!




<a                                                     id="/synopsis"></a>&nbsp;

## SYNOPSIS

```sh
functional-styles [--config=<config>] <style function> | (CSS goes out)
functional-styles --help
```




<a                                                  id="/description"></a>&nbsp;
## DESCRIPTION

`<config>` should be a JS or JSON file exporting a config object. If you omit it, we’ll assume an empty object.

`<style function>` should be a JS file exporting a function.

We’ll pass your config to the style function and translate the output object into a CSS stylesheet. Very simple, but very powerful.




<a                                                         id="/note"></a>&nbsp;

## NOTE

The idea is being tested out on a big production style framework. It still needs some polishing – we’ll post concrete examples as soon as they are ready!

Meanwhile, don’t hestitate to [weigh in](https://github.com/studio-b12/functional-styles/issues)!




<a                                                      id="/license"></a>&nbsp;

## LICENSE

[MIT](./License.md) © [Studio B12 GmbH](http://github.com/studio-b12)
