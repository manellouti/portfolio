<!-- src/components/CreationFooter.vue -->
<template>
  <footer>
    <div class="social-icons">
      <a href="https://github.com/manellouti" target="_blank">
        <img src="/github.png" alt="GitHub" />
      </a>
      <a href="https://www.linkedin.com/in/manel-louti-5aa336281/" target="_blank">
        <img src="/linkedin.png" alt="LinkedIn" />
      </a>
      <a href="https://www.instagram.com/webmastour/?next=" target="_blank">
        <img src="/instagram.png" alt="Instagram" />
      </a>
      <a href="https://www.tiktok.com/@webmastour.com?lang=fr" target="_blank">
        <img src="/tiktok.png" alt="TikTok" />
      </a>
    </div>
    <p>Dernière mise à jour du site : {{ lastUpdated }}</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      lastUpdated: new Date().toLocaleDateString(), // Date de la dernière mise à jour
    };
  },
};
</script>

<style scoped>
footer {
  background-color: #93A299;
  padding: 20px;
  text-align: center;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 10px;
}

.social-icons img {
  width: 30px;
  height: 30px;
  transition: transform 0.3s;
}

.social-icons img:hover {
  transform: scale(1.2);
}

p {
  font-size: 0.9em;
  color: #555;
}
</style>