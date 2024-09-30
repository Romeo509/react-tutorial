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
