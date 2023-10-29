<template>
  <div class="navbar">
    <nav>
      <ul>
        <li v-for="section in sections" :key="section.id">
          <a :href="'#' + section.id" @click="scrollToSection(section.id)" :class="{ 'active': activeSection === section.id }">{{ section.title }}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeSection: 'section1', 
      sections: [
        { id: 'section1', title: 'Section 1' },
        { id: 'section2', title: 'Section 2' },
        { id: 'section3', title: 'Section 3' },
      ],
    };
  },
  methods: {
    scrollToSection(id) {
      this.activeSection = id;
      document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>

*{
    scroll-behavior: smooth;
}
.navbar {
  background-color: #333;
  color: #fff;
  padding: 10px;
}

.navbar nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
}

.navbar nav ul li {
  margin: 0 20px;
}

.navbar nav ul li a {
  color: #fff;
  text-decoration: none;
}



.active {
  font-weight: bold;
}
</style>
