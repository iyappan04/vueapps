<template>
  <div id="app">
    <navbars></navbars>
    <section id="section1" class="section">
      <h2>Section 1</h2>
      <p>Content for Section 1 goes here.</p>
    </section>
    <section id="section2" class="section">
      <h2>Section 2</h2>
      <p>Content for Section 2 goes here.</p>
    </section>
    <section id="section3" class="section">
      <h2>Section 3</h2>
      <p>Content for Section 3 goes here.</p>
    </section>
  </div>
</template>

<script>
import Navbars from './Navbars.vue';

export default {
  components: {
    Navbars,
  },
};
</script>

<style>
*{
    scroll-behavior: smooth;
}

.section {
  padding: 50px 0;
  text-align: center;
  background-color: #f5f5f5;
}

#section1{
    height: 100vh;
    background-color: aqua;
}
#section2{
    height: 100vh;
    background-color: rgb(90, 216, 216);
}
#section3{
    height: 100vh;
    background-color: rgb(122, 14, 122);
}

</style>
