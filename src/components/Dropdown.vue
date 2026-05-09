<template>
  <div class="dropdown">
    <slot name="trigger" :toggleClass="toggleClass" :iconClass="iconClass" :toggle="toggle"></slot>
    <!-- Dropdown menu -->
    <div id="dropdown" :class="toggleClass">
      <ul class="p-2 text-sm text-body font-medium" aria-labelledby="dropdownDefaultButton">
        <slot name="menu" :toggle="toggle"></slot>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Dropdown',
  computed: {
    toggleClass() {
      return this.isOpen
        ? 'z-10 bg-neutral-primary-medium border border-[0.5px] border-gray-200 rounded-lg shadow-sm w-44 mt-1'
        : 'hidden z-10 bg-neutral-primary-medium border border-[0.5px] border-gray-200 rounded-lg shadow-sm w-44 mt-1'
    },
    iconClass() {
        return this.isOpen ? 'w-4 h-4 ms-1.5 -me-0.5 rotate-180' : 'w-4 h-4 ms-1.5 -me-0.5'
    }
  },
  data: () => ({
    isOpen: false,
  }),
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    },
  },
}
</script>
