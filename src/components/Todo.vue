<template>
    <div class="tile flex-centered" :class="{checked: todo.checked}">
        <div class="tile-icon">
        <div>
            <i class="icon" :class="todo.checked ? 'icon-check' : 'icon-time'"></i>
        </div>
        </div>
        <div class="tile-content">
            <div class="tile-subtitle">
                {{ todo.description }}
            </div>
        </div>
        <div class="tile-action">
            <button @click="$emit('toggle', todo)" class="btn btn-link">
                <span v-if="todo.checked">To Do</span>
                <span v-else>Done!</span>
            </button>
            <button @click="$emit('remove', todo)" class="btn btn-link">
                <span class="text-error">Remove</span>
            </button>
        </div>
    </div>
</template>

<script>

export default {
    props: {
        todo: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
.checked {
    text-decoration: line-through;
    color: lightgray;
}
</style>