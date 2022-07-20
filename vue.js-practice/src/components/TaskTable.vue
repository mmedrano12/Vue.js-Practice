<template>
    <div>
         <!--Add a new task through form-->
            <div class="add-task">
                Add New Task
                <form v-on:submit="addTask">
                    <div class="input-form">
                        <div class="input">
                            <input type="text" v-model="tasks.name" />
                        </div>
                        
                        <div class="add-btn">
                            <input type="submit" value="Add"/>
                        </div>
                        
                    </div>
                </form>
            </div>
        
        <table class="table">

            
            <!--Display table with current tasks-->
            <thead>
                <th>Checked</th>
                <th>Task Name</th>
                <th>Remove</th>
            </thead>

            <!--each tasks comes with a completed box, task name, and a delete button-->
            <tbody class="table-body">
                <tr v-for="task in tasks" :key="task.id">
                    <td><input type="checkbox" v-model="task.completed"></td>
                        <td>
                            <span :class="{checked: task.completed}">
                                {{task.name}}
                            </span>
                        </td>
                    <td><button class="delete" v-on:click="deleteTask(task)">Delete</button></td>
                </tr>
                
            </tbody>

        </table>
    </div>
</template>

<script>

export default {
    name: 'Task-Table',
    data: function() {
        return{
            /**
             * task fields:
             * Name: name of the task
             * Completed: whether or not the task has been completed signaled by whether or not the checkbox is clicked
             */
            tasks: [
            {name: 'Buy Groceries', completed: false},
            {name: 'Feed the cat', completed: false},
            {name: 'Clean room', completed: false},
        ]
        }
        
    },
    methods: {
        //push the name of the new task to the tasks array
        addTask: function(e) {
            e.preventDefault(); //prevent default stops the page from instantly deleting the new task from the array
            this.tasks.push({
                name: this.tasks.name, 
                completed: false
            });
        },

        //delete task by task object clicked
        deleteTask: function(task){
            this.tasks.splice(this.tasks.indexOf(task), '1')
        },

        editText: function() {
            
        }
    }
}
</script>

<style scoped>

    .table{
        margin: auto;
        width: 50%;
        padding: 10px;
    }

    td{
        border-top: solid;
        border-width: 1px ;
        padding: 10px;;
    }

    .delete{
        background-color: red;
        color: white;
        border-color: red;
    }

    .add-task{
        border: solid;
        border-width: 2px;
        border-color: #aaa;
        width: 50%;
        margin: auto;
    }

    form{
        max-width: fit-content;
        margin: 30px auto;
        background: white;
        text-align: left;
        border-radius: 10px;
    }

    .input-form{
        display: flex;
        align-content: flex-start;
    }

    .checked{
        text-decoration: line-through;
    }

    




</style>
