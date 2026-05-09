<template>
  <li>
    <a v-bind="$attrs">
        <slot></slot>
    </a>
  </li>
</template>

<script lang="ts">
export default {
  name: 'DropdownItem',
  inheritAttrs: false,
}
</script>
