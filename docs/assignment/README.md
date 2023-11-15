#### Task Overview:

You are tasked with building an advanced to-do list application using React, TypeScript, and any state management solution of your choice (e.g., Redux, MobX). The application should include features like task prioritization, due dates, and the ability to filter tasks based on different criteria. Additionally, implement asynchronous operations, such as fetching tasks from an API.

#### Requirements:

1. **Task Interface:**

   - Extend the `Task` interface to include additional properties like `priority` (string or number) and `dueDate` (Date or string).

2. **Task Component:**

   - Enhance the `Task` component to display the task's priority and due date. Allow users to update the task's completion status, priority, and due date directly from the component.
   - Utilize TypeScript for prop definitions and consider using React hooks for state management.

3. **Task List Component:**

   - Implement a `TaskList` component that can:
     - Display tasks based on different filters (e.g., all tasks, completed tasks, overdue tasks, high-priority tasks).
     - Allow sorting tasks based on priority or due date.
   - Use TypeScript to define props and state for the `TaskList` component.

4. **State Management:**

   - Use React Context and React's built in tools and integrate it into your application. Manage tasks and application state using this solution.
   - Use TypeScript to define actions, reducers, and the overall store structure.

5. **Asynchronous Operations:**

   - Implement the ability to fetch tasks from a mock API or a real one . Use asynchronous actions to handle the API requests.
   - Leverage TypeScript to define API response types.

6. **Editing and Deleting Tasks:**

   - Allow users to edit task details directly from the `Task` component. Implement a confirmation modal for deleting tasks.
   - Use TypeScript to define functions for editing and deleting tasks.

7. **Testing:**

   - Write unit tests for critical components and functions using Jest and React Testing Library.
   - Ensure TypeScript types are utilized in the test files.

8. **Responsive Design:**

   - Ensure your application is responsive and works well on both desktop and mobile devices.
   - Use media queries and CSS best practices.

9. **Quality of life improvements(Bonus)**

   - Implement a drag-and-drop feature to reorder tasks and allow users to drop tasks into different lists.

10. **Performance Optimization (Bonus):**

- Implement performance optimizations, such as memoization or virtualization, to handle a large number of tasks efficiently.

#### Submission Instructions:

- Set up a private repository.
- Create a new branch .
- Commit your changes regularly with meaningful commit messages.
- Provide clear instructions on how to run the application locally, including any setup or installation steps.

#### Evaluation Criteria:

- Effective use of advanced TypeScript features.
- Proper integration and use of a state management solution.
- Implementation of asynchronous operations and error handling.
- Well-structured and organized code with good architectural decisions.
- Thorough testing of critical components and functions.
- Responsive design and attention to user experience.
- Bonus points for performance optimizations and additional features.
