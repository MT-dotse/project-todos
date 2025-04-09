# Project Todo ✅ 📝

The aim of the project was to build a TODO app using React, Redux, JSX and styled components. In this app the user should be able to add/remove tasks, list tasks and toggle when a task is completed or not.

## What have I learned 💡

- I started out by creating a **store** called todos.js with a **initial state** and reducers. In the addtodo reducer I included an object containing four properties: id, text, isComplete, CreatedAt.
- I then built a component called TodoList.js to show those tasks. This component accesses the store by using a **selector**, which returns an array containing all the tasks. It is then mapped over the array in order to show the different tasks on the browser.
- Moving on to **Add and Delete tasks functionality**: In order to add a task, an input form including a text field was created in the AddTodo.js component, allowing the user to add different tasks. Once the add button was clicked, an **action is dispatched**, which will then send the object with the four properties to our existing addTodo reducer. The addTodo reducer is then invoked and a new task is added to the current store.
- To remove a task I performed a filter in the deleteTodo reducer. When the Delete button is clicked an action is dispatched that sends the item.id (for the tasks we want to remove). The filter is then performed in the deleteTodo reducer and returns all the tasks except the item that was sent in.
- I then challenged myself to create **Complete and Remove All** features that enable the user to in one click mark all the tasks and on another click remove all tasks. In the completeAllTask reducer the tasks are mapped over and a isComplete property is set to true. Once the complete all button is clicked an action is dispatched, which invokes the completeAllTask reducer and sets all tasks to completed.
- In the removeAllTask reducer the items are set to an empty array. Once the remove all button is clicked an action is dispatched, and the reducer is invoked returning an empty array.
- For this project I mainly used **styled components**. I like this approach because it offers an organized and structure way to style.

## View it live

https://mt-dotse-todo.netlify.app/

![image](https://github.com/user-attachments/assets/d9eefc30-f81d-4b0c-aefd-744b8684f48e)
