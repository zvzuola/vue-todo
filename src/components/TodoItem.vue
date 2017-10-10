<template>
  <div>
    <div>{{todo.text}}<button @click="$emit('remove')">X</button></div>
    <slot></slot>
  </div>
</template>
<script>
export default {
  props: ['todo'],
};
</script>

