<template>
  <div>Completed Todo: {{ numberOfCompletedTodo }}</div>
</template>
 
<script>
export default {
  props: {
    todos: {
      type: Array,
      required: true,
    },
  },
  computed: {
    numberOfCompletedTodo() {
      return this.todos.filter((todo) => todo.checked).length;
    },
  },
}; // 컴퓨티드(computed) 속성은 템플릿의 데이터 표현을 더 직관적이고 간결하게 도와주는 속성입니다.
</script>

<style>
</style>