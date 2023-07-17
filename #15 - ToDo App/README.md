# _Index.js Explanation_

This code snippet implements a task management feature where users can add, edit, delete, and update the status of tasks. Here's an explanation of the code:

1.  The `const` keyword is used to declare constant variables `taskInput`, `filters`, `clearAll`, and `taskBox`, and assigns them with corresponding elements retrieved from the DOM using `querySelector` and `querySelectorAll`.

2.  An empty `todos` array is initialized by parsing the stored JSON data retrieved from the localStorage with the key "todo-list".

3.  The `forEach` loop iterates over each `btn` element in `filters` and adds a click event listener to it. When the event occurs (user clicks a filter button), the callback function is executed.

4.  Inside the callback function, the class "active" is removed from the currently active filter button by selecting the element with the class "active" and removing the class. Then, the class "active" is added to the clicked filter button (`btn`). The `showTodo` function is called with the `id` of the clicked button as the parameter.

5.  The `showTodo` function takes a `filter` parameter and generates HTML code for each task based on the `todos` array. The generated HTML code is stored in the `liTag` variable. The generated tasks are filtered based on the selected filter. The generated HTML code is then assigned to the `taskBox` element's `innerHTML`.

6.  The status of the tasks is updated based on the completion status of the checkboxes. If a checkbox is checked, the task is marked as "completed" and the class "checked" is added to the corresponding task name. If a checkbox is unchecked, the task is marked as "pending" and the class "checked" is removed.

7.  The `editTask` function is called when the edit button for a task is clicked. It sets the `editId` to the ID of the task and sets the `isEditTask` flag to `true`. The task name is then assigned to the `taskInput` value, and the input field is focused and marked as active.

8.  The `deleteTask` function is called when the delete button for a task is clicked. It removes the task with the corresponding `deleteId` from the `todos` array and updates the localStorage. The `showTodo` function is called with the `filter` parameter to update the task list.

9.  The `clearAll` button has a click event listener. When the button is clicked, the `todos` array is emptied, and the localStorage is updated. The `showTodo` function is called without any parameters to update the task list.

10. The `taskInput` element has a `keyup` event listener. When a key is released in the input field, the callback function is executed.

11. Inside the callback function, the user's input task is trimmed and stored in the `userTask` variable. If the Enter key is pressed (`e.key == "Enter"`) and the `userTask` is not empty, the code checks whether it is an edit task or a new task. If it is a new task, a task object is created and added to the `todos` array. If it is an edit task, the task name is updated in the `todos` array. The `taskInput` value is cleared, and the localStorage is updated. The `showTodo` function is called with the active filter button's `id` to update the task list.

Overall, this code allows users to manage tasks by adding, editing, deleting, and updating the status of tasks. The task data is stored in the localStorage, and the task list is dynamically updated based on the selected filter.