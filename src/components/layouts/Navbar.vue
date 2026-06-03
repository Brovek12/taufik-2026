<script setup>
import { ref } from 'vue'

const menus = ref([
  {
    label: 'Home',
    path: '/'
  },
  {
    label: 'Features',
    path: '#features'
  },
  {
    label: 'About',
    path: '#about'
  }
])
</script>

<template>
  <div class="navbar bg-base-100 shadow-sm px-6 lg:px-12">
   <div class="flex-1">
    <img src="/favicon.png" alt="gambar" class="w-10 h-10" />
</div>
    <input
  type="checkbox"
  class="toggle theme-controller"
  value="synthwave"
/>
    <div class="flex-none">
      <ul class="menu menu-horizontal px-1">
        <li
          v-for="menu in menus"
          :key="menu.label"
        >
          <a :href="menu.path">
            {{ menu.label }}
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>