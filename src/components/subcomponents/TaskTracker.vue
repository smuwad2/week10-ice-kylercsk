<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        props:{
            task:Object,
            idx:Number
        },
        emits:['rdelete']
        // Hint: insert properties task (Object) and idx (Number)
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
<div class="card w-100 h-100">
    <div class="card-body">
    <h5 class="card-title fw-bold"><span>Deadline:</span>{{ task.desc }}</h5>
    <p class="card-text"> {{ task.deadline }} </p>
    <button class="btn btn-primary" @click="$emit('rdelete',idx)">Done</button>

  </div>
</div>
   
</template>


