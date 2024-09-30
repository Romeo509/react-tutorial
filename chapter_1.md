# Todo App - Chapter 1

## Overview

In this chapter, we set up the initial structure for our Todo application using React. The goal of this chapter was to create the foundational component that will allow us to display and manage our todo items effectively.

## Project Structure

After running `npx create-react-app todo-app`, we organized our project with a dedicated folder for components. This organization helps maintain a clean codebase as we continue to develop the application.

### Key Components Created

1. **TodoItem Component**:
   - Created a new file named `TodoItem.js` within the `src/components` folder.
   - This component receives a `todo` prop, which represents a single todo item, and displays it in a user-friendly manner.
   - It includes a checkbox to indicate whether the todo is completed and displays the text associated with the todo.

### Code Implementation

**TodoItem.js**
```javascript
import React from 'react';

const TodoItem = ({ todo }) => {
    return (
        <div>
            <input type="checkbox" checked={todo.completed} />
            {todo.text}
        </div>
    );
};

export default TodoItem;
```

**App.js**
- Updated `App.js` to import and use the `TodoItem` component.
- Created a sample state containing a list of todos to demonstrate how the `TodoItem` component would be rendered.

### Code Snippet for App.js
```javascript
import React, { useState } from 'react';
import TodoItem from './components/TodoItem';

const App = () => {
    const [todos, setTodos] = useState([
        { id: 1, text: 'Learn React', completed: false },
        { id: 2, text: 'Build a Todo App', completed: false },
    ]);

    return (
        <div>
            <h1>My Todo List</h1>
            {todos.map((todo) => (
                <TodoItem key={todo.id} todo={todo} />
            ))}
        </div>
    );
};

export default App;
```

## Conclusion

Chapter 1 provided a strong foundation for our Todo application by establishing the basic structure and the first component. This chapter set the stage for future enhancements, such as adding functionality to create, update, and delete todo items.

### Next Steps

In the upcoming chapters, we will focus on:
- Adding state management for creating and deleting todos.
- Styling the application to improve user experience.
- Implementing local storage to persist data.
