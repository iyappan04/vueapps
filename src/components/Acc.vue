<template>
  <div id="app">
    <div v-for="(item, index) in accordionItems" :key="index">
      <div
        @click="toggleAccordion(index)"
        :class="{ 'bg-blue-500 text-white': activeIndex === index, 'bg-gray-200': activeIndex !== index }"
        class="cursor-pointer p-4 mb-2 rounded flex justify-between items-center"
      >
        {{ item.title }}
        <span v-if="activeIndex === index">-</span>
        <span v-else>+</span>
      </div>
      <div v-show="activeIndex === index" class="p-4 bg-gray-100">{{ item.content }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Acc",
  data() {
    return {
      activeIndex: null,
      accordionItems: [
        {
          title: "Accordion Item 1",
          content: "Content for Accordion Item 1"
        },
        {
          title: "Accordion Item 2",
          content: "Content for Accordion Item 2"
        },
        {
          title: "Accordion Item 3",
          content: "Content for Accordion Item 3"
        }
      ]
    };
  },
  methods: {
    toggleAccordion(index) {
      if (this.activeIndex === index) {
        this.activeIndex = null;
      } else {
        this.activeIndex = index;
      }
    }
  }
};
</script>