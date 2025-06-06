---
applyTo: "**"
---
# Todo App Language and Interaction Standards

## Domain Vocabulary

- **TodoItem**: A single unit of work. Must have a `title`, optional `description`, `isCompleted` status, and a unique `id`.
- **TaskList**: A collection of `TodoItem`s, optionally grouped under a user-defined category.
- **DueDate**: Optional date field specifying when a `TodoItem` is due.
- **PriorityLevel**: Enum representing urgency (`low`, `medium`, `high`).

## Common Actions

- `createTodo(title: string, description?: string): TodoItem`
- `completeTodo(id: string): void`
- `deleteTodo(id: string): void`

## Naming Conventions

- Use `PascalCase` for domain types (`TodoItem`, `TaskList`, `PriorityLevel`)
- Use `camelCase` for variables and functions
- Use verb-noun pairs for action functions (`createTodo`, `deleteTodo`)
- Prefix boolean properties with `is` or `has` (e.g., `isCompleted`, `hasDueDate`)

## Comments and Documentation

- Document purpose and side effects of each function
- When referring to a `TodoItem` in comments or prompts, use this structure:
  `"TodoItem(title: 'Buy milk', dueDate: '2025-06-10', isCompleted: false)"`
- Refer to filtering logic in functional terms:
  `"Filter todos with priority = 'high' and dueDate before '2025-06-15'"`

## Expected LLM Behavior

- Recognize and reason about domain terms like `TodoItem`, `completeTodo`, or `dueDate`
- When asked to "list high-priority todos," infer the intent to call `filterTodos({ priority: 'high' })`
- Understand that marking a task as done modifies `isCompleted` to `true`