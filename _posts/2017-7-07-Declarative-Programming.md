## Some notes and quotes

### Declarative programming

Considering some of the more functional programming concepts/techniques,
starting with *.map*, *.reduce*, *.filter*.

> Declarative programming is "the act of programming in languages 
> that conform to the mental model of the developer rather than the 
> operational model of the machine".

> Declarative property is where there can exist only one possible set 
> of statements that can express each specific modular semantic.The 
> imperative property is the dual, where semantics are inconsistent 
> under composition and/or can be expressed with variations of sets 
> of statements.

> Declarative languages contrast with imperative languages which 
> specify explicit manipulation of the computer’s internal state; 
> or procedural languages which specify an explicit sequence of steps 
> to follow.

> In computer science, declarative programming is a programming paradigm 
> that expresses the logic of a computation without describing its 
> control flow.

### Webpack

> So where webpack really shines is you're able to tell it every transformation
> your code needs to make, and it will do them and output a bundle file for you
> full of those changes (and some other helpful things as well like minification
> if you desire).

```javascript
module.exports = {
  entry: './app/index.js',
  module: {
    rules: [
      { test: /\.coffee$/, use: "coffee-loader" }
    ]
  },
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: 'index_bundle.js'
  },
  plugins: [
    new HtmlWebpackPlugin({
      template: 'app/index.html'
    })
  ]
}
```
> Up until this point we haven’t really emphasized the importance of this new
> "virtual DOM" paradigm we’re jumping into. The reason the React team went with
> this approach is because, since the virtual DOM is a JavaScript representation
> of the actual DOM, React can keep track of the difference between the current
> virtual DOM (computed after some data changes), with the previous virtual DOM
> (computed befores some data changes). React then **isolates the changes between**
> **the old and new virtual DOM and then only updates the real DOM with the
> necessary changes.** (More advanced info here) In more layman’s terms, because
> manipulating the actual DOM can be complex, React is able to minimize
> manipulations to the actual DOM by keeping track of a virtual DOM and only
> updating the real DOM when necessary and with only the necessary changes.
> Typically UI’s have lots of state which makes managing state difficult. By
> re-rendering the virtual DOM every time any state change occurs, React makes it
>easier to think about what state your application is in.

**A component is a function or a Class which optionally accepts input and returns a React element.**

```javascript
function Button ({ onLogin }) {
  return React.createElement(
    'div',
    {id: 'login-btn', onClick: onLogin},
    'Login'
  )
}
```
[React Components, Elements, and Instances](https://facebook.github.io/react/blog/2015/12/18/react-components-elements-and-instances.html)

[^1]: (React Training by Tyler McGinnis)[https://learn.tylermcginnis.com/courses/50507/lectures/760301#/finished]
