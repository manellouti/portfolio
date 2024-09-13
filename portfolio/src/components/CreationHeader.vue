<!-- src/components/CreationHeader.vue -->
<template>
  <header>
    <nav>
      <img src="/logo.png" alt="Logo" class="logo" @click="scrollToTop" />
      <ul>
        <li><a href="#presentation">Présentation</a></li>
        <li><a href="#creations">Créations</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  methods: {
    scrollToTop() {
      // Scroll vers le haut de la page
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }
  }
};
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #CCC6AD;
}

.logo {
  width: 100px;
  height: auto;
  cursor: pointer;
}

ul {
  list-style-type: none;
  display: flex;
  gap: 20px;
}

li {
  font-size: 1.2em;
}

a {
  text-decoration: none;
  color: #333;
  transition: color 0.3s;
}

a:hover {
  color: #007bff;
}
</style>