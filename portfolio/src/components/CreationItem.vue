<template>
  <div class="creation-item">
    <!-- Image et titre du projet -->
    <img :src="image" :alt="title" @click="openModal" />
    <h3 @click="openModal">{{ title }}</h3>

    <!-- Modal -->
    <div v-if="isModalOpen" class="modal-overlay" @click="closeModal">
      <div class="modal-content" @click.stop>
        <button class="close-button" @click="closeModal">&times;</button>
        <h3>{{ title }}</h3>
        <p><strong>Date de création :</strong> {{ creationDate }}</p>
        <p><strong>Technologies utilisées :</strong> {{ technologies }}</p>
        <p>{{ description }}</p>
        <a v-if="link" :href="link" target="_blank">Voir le site</a>
        <a v-if="github" :href="github" target="_blank">Voir sur GitHub</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    image: String,
    description: String,
    creationDate: String,
    technologies: String,
    link: String,
    github: String,
  },
  data() {
    return {
      isModalOpen: false,
    };
  },
  methods: {
    openModal() {
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
    },
  },
};
</script>

<style scoped>
.creation-item {
  text-align: center;
  cursor: pointer;
  margin-bottom: 20px;
}

.creation-item img {
  width: 100%;
  height: auto;
  max-width: 300px;
  border-radius: 5px;
  transition: box-shadow 0.3s ease;
}

.creation-item h3 {
  margin-top: 10px;
  font-size: 1.2em;
  color: #333;
}

.creation-item img:hover,
.creation-item h3:hover {
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
}

.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background: white;
  padding: 20px;
  border-radius: 8px;
  max-width: 500px;
  width: 90%;
  position: relative;
  text-align: center;
}

.close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  background: transparent;
  border: none;
  font-size: 1.5em;
  cursor: pointer;
}
</style>