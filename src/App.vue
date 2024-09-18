<script>
    import TodoList from './components/TodoList.vue';

export default {
  data() {
    return {
      count: 0
    }
  },
  components:{
    TodoList
  }
}
</script>

<template>
  <TodoList />
</template>

<style lang="scss">
  @use 'bootstrap/scss/bootstrap.scss';
  @use "./style/general.scss";
  

</style>
