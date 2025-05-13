# Deleting Tasks

The to-do list API allows users to easily delete existing tasks. For example, this capability can delete tasks after completion
or remove tasks that are no longer relevant.

### Prerequisites

* An existing to-do list with tasks
* Access to a command line or Postman
  * This tutorial will use Postman, but can be completed with the command line to make the necessary REST API calls.

## Deleting an Existing Task

1. Confirm the local to-do service is running.
   * If the service is not running, run the following command:
     ```shell
     cd <your-github-workspace>/to-do-service/api
     json-server -w to-do-db-source.json
     ```
2. Open the Postman app on your computer.
3. Locate the task you want to delete. For a full list of the tasks currently available in the to-do list, create a new request
   with the following values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/tasks`
    * **Header**: `Content-Type: application/json` 
4. After locating the task to delete, create a new request with the following values:
    * **METHOD**: DELETE
    * **URL**: `{{base_url}}/tasks/{taskId}`
    * **Header**: `Content-Type: application/json` 
5. To confirm the task is deleted, create an additional request with the following values:
    * **METHOD**: GET
    * **URL**: `{{base_url}}/tasks/{previoustaskId}`
    * **Header**: `Content-Type: application/json`
6. Postman will return the following response if the deletion was successful: `{}`
    
### Result

You can now locate and delete existing tasks in the to-do list.
