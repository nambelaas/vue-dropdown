<template>
  <component
    :is="tag"
    class="bg-blue-500 rounded-lg cursor-pointer outline inline-flex items-center justify-center text-white box-border border border-transparent hover:bg-blue-600 focus:ring-4 focus:ring-blue-300 shadow-xs font-medium leading-5 rounded-base text-sm px-4 py-2.5 focus:outline-none"
  >
    <slot></slot>
  </component>
</template>

<script lang="ts">
export default {
  name: 'DropdownTrigger',
  props: {
    tag: {
      type: String,
      default: 'button',
      validator: (value: string) => ['button', 'a'].includes(value),
    },
  },
}
</script>
