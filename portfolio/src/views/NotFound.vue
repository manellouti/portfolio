<template>
  <div class="not-found">
    <h1>404</h1>
    <h2>Oups ! Page non trouvée</h2>
    <img src="@/assets/page404.jpg" alt="Page non trouvée" class="error-image" />
    <p>La page que vous cherchez n'existe pas.</p>
    <router-link to="/">Retourner à l'accueil</router-link>
  </div>
</template>

<style>
.not-found {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  height: 100vh;
  background-color: #f5f5f5;
  color: #333;
}

.not-found h1 {
  font-size: 5em;
  margin: 0;
}

.not-found h2 {
  font-size: 2em;
  margin: 10px 0;
}

.error-image {
  width: 50%;
  max-width: 400px;
  height: auto;
  margin: 20px 0;
}

.not-found p {
  font-size: 1.2em;
}

.not-found a {
  color: #ccc6ad;
  text-decoration: none;
}

.not-found a:hover {
  text-decoration: underline;
}
</style>
