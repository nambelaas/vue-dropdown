<template>
  <li>
    <a v-bind="$attrs">
      <slot></slot>
    </a>
  </li>
</template>

<script setup lang="ts">
defineOptions({
  inheritAttrs: false,
})
</script>
