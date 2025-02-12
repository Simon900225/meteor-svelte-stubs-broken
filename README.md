If you run this project, you will see that there are no logs to the browser console when inserting a new task, but there are in the server console.  
user: meteorite  
password:password  

if you however uncomment this line  
//import { TasksMethods } from '../api/tasksMethods';   
in TaskForm.svelte
the method will now run both in the server and on the client.

