<template>
  <div class="dropdown">
    <slot name="trigger"></slot>
    <!-- Dropdown menu -->
    <div
      id="dropdown"
      class="z-10 bg-neutral-primary-medium border border-[0.5px] border-gray-200 rounded-lg shadow-sm w-44 mt-1"
    >
      <ul class="p-2 text-sm text-body font-medium" aria-labelledby="dropdownDefaultButton">
        

        <slot name="menu"></slot>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Dropdown',
}
</script>
