---
mode: 'agent'
tools: ['codebase', 'terminalLastCommand']
description: 'Combine frontend (Next.js) and backend (FastAPI) code for a Todo app'
---

You are working with a full-stack Todo application. The project is split into two folders:

- The frontend is located in the `frontend` directory and built with **Next.js**.
- The backend is located in the `backend` directory and built with **FastAPI**.

The backend exposes endpoints to:
- Get todos (`GET /todos`)
- Add a todo (`POST /todos`)
- Update a todo (`PUT /todos/{id}`)
- Delete a todo (`DELETE /todos/{id}`)

The frontend should:
- Fetch todos from the backend
- Display the list of todos
- Provide functionality to add, edit, and delete todos
- Handle loading and error states
- Have the ability to show the priority of a todo

Your task is to:
1. Analyze both frontend and backend code.
2. Identify where API requests are made in the frontend.
3. Verify that the frontend correctly maps to the FastAPI endpoints.
4. Fix any mismatches in route names, payload structure, or request methods.
5. Ensure CORS settings in FastAPI allow requests from the frontend's origin .
6. Add any missing functionality or pages necessary to complete the full-stack integration.

Additional checks:
- Ensure the environment variables or base URLs are correctly set in the frontend to point to the FastAPI server.
- Update the frontend UI to reflect real-time data from the backend after actions (create, update, delete).

You may suggest or make changes to improve the full-stack integration and ensure the system is working end-to-end.

If any part of the system is missing suggest or generate it.