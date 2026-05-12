<template>
  <div class="dropdown">
    <slot name="trigger" :toggleClass="toggleClass" :iconClass="iconClass" :toggle="toggle"></slot>
    <!-- Dropdown menu -->
    <div id="dropdown" :class="toggleClass" v-on-click-outside="dropdownHandler">
      <ul class="p-2 text-sm text-body font-medium" aria-labelledby="dropdownDefaultButton">
        <slot name="menu" :toggle="toggle"></slot>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed, ref } from 'vue'
import { vOnClickOutside } from '@vueuse/components'

let isOpen = ref(false)

const toggle = () => {
  isOpen.value = !isOpen.value
}
const dropdownHandler = () => {
  isOpen.value = false
}

const toggleClass = computed(() => {
  return isOpen.value
    ? 'z-10 bg-neutral-primary-medium border border-[0.5px] border-gray-200 rounded-lg shadow-sm w-44 mt-1'
    : 'hidden z-10 bg-neutral-primary-medium border border-[0.5px] border-gray-200 rounded-lg shadow-sm w-44 mt-1'
})
const iconClass = computed(() => {
  return isOpen.value ? 'w-4 h-4 ms-1.5 -me-0.5 rotate-180' : 'w-4 h-4 ms-1.5 -me-0.5'
})
</script>
