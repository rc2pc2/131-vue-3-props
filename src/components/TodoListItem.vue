<script>
export default {
    data() {
        return {

        }
    },
    props:{
        content: {
            type: String,
            required: true,
        },
        status: {
            type: Boolean,
            required: true,
        }
    },
    computed: {
        statusClass(){
            if (this.status === true){
                return "item-done"
            } 
            return "item-todo"
        }
    }
}
</script>

<template>
    <li :class="statusClass">
        {{ content }}
    </li>
</template>

<style scoped>
/* @import url("") */

    .item-done{
        text-decoration: line-through;
    }

    .item-todo{
        text-decoration: none;
    }
</style>