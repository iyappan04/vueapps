<template>
  <div id="app">
    <div class="flex p-4">
      <div
        v-for="(tab, index) in tabs"
        :key="index"
        @click="activeTab = index"
        :class="{ 'bg-blue-500': activeTab === index, 'text-white': activeTab === index }"
        class="cursor-pointer px-4 py-2 mr-2 rounded hover:bg-blue-400"
      >{{ tab }}</div>
    </div>

    <div v-show="activeTab === 0">Content for Tab 1</div>
    <div v-show="activeTab === 1">Content for Tab 2</div>
    <div v-show="activeTab === 2">Content for Tab 3</div>
  </div>
</template>

<script>
export default {
  name: 'Tabs',
   data(){
    return{
        activeTab: 0,
        tabs: ['Tab 1', 'Tab 2', 'Tab 3'],
    }
  }
}
</script>


<style scoped>
</style>
