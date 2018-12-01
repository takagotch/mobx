### mobx
---
https://github.com/mobxjs/mobx

```js
import { observable } from "mobx"
class Todo {
  id = Math.random();
  @observable title = "";
  @observable finished = false;
}

import {} from ""
class Todo {
  id = Math.random();
  title = "";
  finished = false;
}
decorate(Todo, {
  title: observable,
  finished: observable
})

class TodoList {
  @observable todos = [];
  @computed get unfinishedTodoCount() {
    return this.todos.filter(todo => !todo.finished).length;
  }
}

import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import {observer} from 'mobx-react';
@observer
class TodoListView extends Component {
  render() {
    return <div>
      <ul>
        {this.props.todoList.todos.map(todo =>
          <TodoView todo={todo} key={todo.id} />
        )}
      </ul>
      Tasks left: {this.props.todoList.unfinishedTodoCount}
    </div>
  }
}
const TodoView = observer(({todo}) =>
  <li>
    <input
      type="checkbox"
      checked={todo.finished}
      onClick={() => todo.finished = !todo.finished}
    />{todo.title}
  </li>
) 
const store = new TodoList();
ReactDOM.render(<>, document.getElementById('mount'));

autorun(() => {
  console.log("Tasks left: " + todos.unfinishedTodoCount)
})
store.todos.push(
  new Todo("Get Coffee"),
  new Todo("Write simpler code")
);
store.todos[0].finished = true;
```

```
```

```
```

