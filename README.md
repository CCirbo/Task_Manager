
## Rails Tutorial: Task Manager 


1. #### Define CRUD.
    They are four basic types of functionality or operations for creating and managing data elements in a database application. 
    - C: Create -- adds a new record to the database.
    - R: Read -- returns records or documents from a database table based on some criteria.
    - U: Update -- used to modify existing records in the database. Updates can be the whole record or lines of the record.
    - D: Delete -- allows the user to remove records from the database.
    
2. #### Define MVC 
    - Model-View-Controller, a framework design pattern that separates an application into three main componets. 
    - Models - Interact with the database. Holds other methods related to a particular resource (e.g. a task).The purpose of Models is to create objects based on records that exist in a database.
    - Views - Presents an application’s data to the user. In Task Manager, this was the JSON rendered in the controller with the use of Serializers. In other applications this might look like an HTML template.
    - Controllers - Coordinate the response to an HTTP request. In Task Manager, we just had one, but it is common to have multiple controllers.
    
3. #### What two files would you need to create/modify for a Rails application to respond to a GET request to /api/v1/tasks, assuming you have a Task model.
    - *route.rb* file and added code so that when we received an HTTP GET request, it should perform the index action with our tasks controller. We also added code for Show, Create, Update and Delete routes. These routes allow for a full set of CRUD operations on the tasks resource via an API.
    - *tasks_controller.rb* file. Each of the routes added corresponds to a specific action (written in ruby methods) in the task_controller file, making sure the API can handle requests to create, read, update and delete tasks.
    
4. #### What are params? Where do they come from? 
    - *params* is a parameter object/hash (query) that contains the parameters sent by a client in the request. You can see paramenters in the URL after the ? and allow the client to pass data to the API.  The parameters are populated based on the route definition.
    
5. #### What is the purpose of a serializer?
    - Serializers are used to generate custom JSON so we can control exactly what the controller sends back to our user. In our case, we removed from the user's view the id, and both date stamps as the user doen't want them however they are still used in our database.
