<script lang="ts">
import Dropdown from './components/Dropdown.vue'
import DropdownItem from './components/DropdownItem.vue'
import DropdownTrigger from './components/DropdownTrigger.vue'
export default {
  name: 'App',
  components: {
    Dropdown,
    DropdownItem,
    DropdownTrigger,
  },
}
</script>

<template>
  <Dropdown>
    <template #trigger="{ toggleClass, iconClass, toggle }">
      <DropdownTrigger
        type="button"
        data-dropdown-toggle="dropdown"
        :class="toggleClass"
        @click="toggle"
      >
        Dropdown button
        <svg
          :class="iconClass"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="none"
          viewBox="0 0 24 24"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="m19 9-7 7-7-7"
          />
        </svg>
      </DropdownTrigger>
    </template>
    <template #menu="{ toggle }">
      <DropdownItem
        href="#"
        @click.prevent="toggle"
        class="inline-flex items-center w-full p-2 hover:bg-gray-100 hover:text-heading rounded"
      >
        Dashboard
      </DropdownItem>
      <DropdownItem
        href="#"
        @click.prevent="toggle"
        class="inline-flex items-center w-full p-2 hover:bg-gray-100 hover:text-heading rounded"
      >
        Settings
      </DropdownItem>
      <DropdownItem
        href="#"
        @click.prevent="toggle"
        class="inline-flex items-center w-full p-2 hover:bg-gray-100 hover:text-heading rounded"
      >
        Earnings
      </DropdownItem>
      <DropdownItem
        href="#"
        @click.prevent="toggle"
        class="inline-flex items-center w-full p-2 hover:bg-gray-100 hover:text-heading rounded"
      >
        Sign Out
      </DropdownItem>
    </template>
  </Dropdown>
</template>
