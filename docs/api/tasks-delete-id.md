# Delete task (ID)

Removes a [`task`](task.md) object specified by the `id` parameter.

## Request URL

**Method**: DELETE

**URL**: `{{base_url}}/tasks/{taskId}`

## Parameter(s)

| Name | Variable |
| ---- | ---------|
| base_url | string |
| tasks | string |
| taskId | integer |

## Header(s)

**Content-Type:** `application/json`

## Request Body

N/A

## Return Body

`
{}
`

## Responses
* 200: Successful
* 404: Task object not found
* ECONNREFUSED: To-do service is offline
