<template>
    <div v-for="task in tasks" :key="task.id">

    <TheTask :task="task" />
    </div>
</template>
<script>
import TheTask from './TheTask.vue'
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Tasks',
    props: {
        tasks: Array
    },
    components: {
        TheTask
    }
}
</script>