# AWS SAM

Challenge to Implement: TASK MANAGEMENT PROJECT

    Create a New Task
        HTTP Method: POST
        Endpoint: /tasks
        Functionality:
            Accepts a JSON body with a taskName and description.
            Stores the task in a DynamoDB table with a unique taskId, a taskName, description, and status (default status: "pending").
            Returns the created task as a JSON response.

    Get All Tasks
        HTTP Method: GET
        Endpoint: /tasks
        Functionality:
            Retrieves all tasks from the DynamoDB table.
            Returns a JSON array of tasks.

    Get a Single Task by ID
        HTTP Method: GET
        Endpoint: /tasks/{taskId}
        Functionality:
            Retrieves a task by its taskId from DynamoDB.
            Returns the task as a JSON response if it exists, otherwise returns a 404 error.

    Update a Task
        HTTP Method: PUT
        Endpoint: /tasks/{taskId}
        Functionality:
            Accepts a JSON body with updated values (taskName, description, status).
            Updates the task in DynamoDB if it exists.
            Returns the updated task as a JSON response.

    Delete a Task
        HTTP Method: DELETE
        Endpoint: /tasks/{taskId}
        Functionality:
            Deletes a task from DynamoDB by taskId.
            Returns a success message or a 404 error if the task doesn't exist.