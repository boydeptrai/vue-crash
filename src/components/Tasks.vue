<template>
    <div v-for="task in tasks" :key="task.id">

    <TheTask @toggle-reminder="$emit('toggle-reminder',task.id)" @delete-task="$emit('delete-task',task.id)" :task="task" />
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
    },
    emits: ['delete-task','toggle-reminder']
}
</script>