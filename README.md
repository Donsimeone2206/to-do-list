# Task List App

## Overview

This is a basic Task List App that allows users to add tasks and manage them using a simple user interface. Tasks can be marked as completed by clicking on them, and they can also be deleted. The tasks are saved locally in the browser's `localStorage`, ensuring that your tasks remain intact even after refreshing the page.

## Setup

1. **HTML Structure**: To integrate this JavaScript code, ensure you have an HTML structure similar to this:
   ```html
   <input type="text" id="input-box" placeholder="Enter a task...">
   <button onclick="addTask()">Add Task</button>
   <ul id="list-container"></ul>
   ```

2. **Styling**: Add some basic styles for better visualization. For instance, you can style the `.checked` class to represent completed tasks with a line-through.

3. **Local Storage**: The app uses the browser's `localStorage` to persist tasks. Ensure your browser supports `localStorage`.

## How to Use

1. **Adding Tasks**:
    - Type your task into the `input-box`.
    - Click the "Add Task" button to add the task to the list.
    - If you try adding an empty task, an alert will notify you to write something.

2. **Marking Tasks as Completed**:
    - Click on a task to mark it as completed. Clicking again will unmark it.
    - Completed tasks will have a visual indication (like a line-through) if styled accordingly.

3. **Deleting Tasks**:
    - Each task has a close button (`×`) on its right side.
    - Click on the close button to delete a task from the list.

4. **Persistence**:
    - Your tasks are automatically saved in the browser's `localStorage` after any changes.
    - When you revisit or refresh the page, your tasks will be loaded from `localStorage`.

## Code Structure

- **Add Task**: The `addTask` function is responsible for creating a new task element, appending it to the list, and saving the updated list to `localStorage`.

- **Manage Tasks**: An event listener on the `listContainer` detects clicks on tasks and their close buttons. Clicking on a task toggles its completion status, while clicking on a close button deletes the task.

- **Save and Load Data**: The `saveData` function saves the current list of tasks to `localStorage`. The `showTask` function loads the tasks from `localStorage` when the page is loaded.

## Note

While `localStorage` is a convenient way to store data locally in the browser, it has a limit (usually around 5MB). If you plan to expand this app or store a large number of tasks, consider other storage solutions or backend integration.

## Contributing

If you'd like to contribute to this project, enhance its features, or suggest improvements, please create an issue or submit a pull request.
