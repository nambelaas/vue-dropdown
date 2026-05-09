<script lang="ts">
import Dropdown from './components/Dropdown.vue'
export default {
  name: 'App',
  components: {
    Dropdown,
  },
}
</script>

<template>
  <Dropdown>
    <template #trigger="{ toggleClass, toggle }">
      <button
        id="dropdownDefaultButton"
        data-dropdown-toggle="dropdown"
        class="bg-blue-500 rounded-lg cursor-pointer outline inline-flex items-center justify-center text-white box-border border border-transparent hover:bg-blue-600 focus:ring-4 focus:ring-blue-300 shadow-xs font-medium leading-5 rounded-base text-sm px-4 py-2.5 focus:outline-none"
        :class="toggleClass"
        type="button"
        @click="toggle"
      >
        Dropdown button
        <svg
          class="w-4 h-4 ms-1.5 -me-0.5"
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
      </button>
    </template>
    <template #menu="{ toggle }">
      <li>
        <a
          href="#"
          @click.prevent="toggle"
          class="inline-flex items-center w-full p-2 hover:bg-neutral-tertiary-medium hover:text-heading rounded"
          >Dashboard</a
        >
      </li>
      <li>
        <a
          href="#"
          @click.prevent="toggle"
          class="inline-flex items-center w-full p-2 hover:bg-neutral-tertiary-medium hover:text-heading rounded"
          >Settings</a
        >
      </li>
      <li>
        <a
          href="#"
          @click.prevent="toggle"
          class="inline-flex items-center w-full p-2 hover:bg-neutral-tertiary-medium hover:text-heading rounded"
          >Earnings</a
        >
      </li>
      <li>
        <a
          href="#"
          @click.prevent="toggle"
          class="inline-flex items-center w-full p-2 hover:bg-neutral-tertiary-medium hover:text-heading rounded"
          >Sign out</a
        >
      </li>
    </template>
  </Dropdown>
</template>
