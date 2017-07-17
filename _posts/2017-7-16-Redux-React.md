# React Redux

Middleware design which groups asychronous behavior, thus obviating duplicate code and simplifying testing.  Extracts redundant logic using the [Chain of Responsibility Pattern](https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern).  

Some tutorial videos:

[Getting Started With Redux](https://egghead.io/courses/getting-started-with-redux)

[Hot Reloading With Time Travel](https://www.youtube.com/watch?v=xsSnOQynTHs)

```javascript
{
  todos: [{
    text: 'Eat food',
    completed: true
  }, {
    text: 'Exercise',
    completed: false
  }],
  visibilityFilter: 'SHOW_COMPLETED'
}
```

Reducers allow us to manage the complete state of the app for calling the reducer for each corresponding state key:

```javascript
function todoApp(state = {}, action) {
  return {
    todos: todos(state.todos, action),
    visibilityFilter: visibilityFilter(state.visibilityFilter, action)
  }
}
```