<script>
import TaskTracker from './subcomponents/TaskTracker.vue';
    export default {
        data() {
            return {
                desc: '',
                deadline: '',
                taskList: []
            }
        },
        methods: {
            add() {
                this.taskList.push( { 'desc': this.desc, 'deadline': this.deadline } )
                this.desc = ''
                this.deadline = ''
            },
            // TODO: Add a new method, to delete a task completed
            rdelete(index){
                this.taskList.splice(index,1)
            }
            
        },
        components:{
            TaskTracker
        }
    }

</script>

<template>
    <div class="mb-3">
        <label for="desc" class="form-label">Task</label>
        <input type="text" class="form-control" id="desc" v-model='desc' placeholder="task">
    </div>
    <div class="mb-3">
        <label for="deadline" class="form-label">Deadline</label>
        <input type="date" class="form-control" id="deadline" v-model='deadline' placeholder="deadline">
    </div>

    <button type="button" @click="add" class="btn btn-primary">Add New Task</button>
    <hr>

    <!-- TODO: Modify following code -->
        <div class="container-fluid">
            <div class="row">
                <div v-for="(item,index) in taskList" class="col-4"
                :key=index>
                    <task-tracker 
                    :task="item"
                    :idx="index"
                    v-on:rdelete="rdelete"
                    >
                    </task-tracker>
                </div>
            </div>
        </div>

</template>

<style scoped>
   
</style>
