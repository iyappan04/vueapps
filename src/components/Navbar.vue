<template>
  <nav class="bg-gray-800 p-4">
    <ul class="flex space-x-4">
      <li :class="{ 'text-red-500': textColor === 'red', 'text-blue-500': textColor === 'blue' }">
        <router-link to="/">Home</router-link>
      </li>
      <li :class="{ 'text-red-500': textColor === 'red', 'text-blue-500': textColor === 'blue' }">
        <router-link to="/about">About</router-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  props: {
    textColor: {
      type: String,
      default: 'red'
    }
  }
}
</script>
