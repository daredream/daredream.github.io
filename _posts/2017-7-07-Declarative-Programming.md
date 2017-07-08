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

