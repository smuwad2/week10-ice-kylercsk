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
<div class="card" style="width: 18rem;">
    <div class="card-body">
    <h5 class="card-title fw-bold"><span>Deadline:</span>{{ task.deadline }}</h5>
    <p class="card-text"> {{ task.desc }} </p>
    <button class="btn btn-primary" @click="$emit('rdelete',idx)">Done</button>

  </div>
</div>
   
</template>


