<template>
  <div>
    <!-- Header Section -->
    <header>
      <CreationHeader />
    </header>
    <main>
      <router-view />
      <!-- Content Section -->

      <HelloWorld msg="Bienvenue sur mon portfolio" author="Manel Louti" />

      <!-- Présentation Section -->
      <section id="presentation">
        <h2>Présentation</h2>
        <img
          src="@/assets/profile.png"
          alt="Photo de Manel Louti"
          class="profile-photo"
        />
        <p>
          Bonjour, je m'appelle Manel Louti, j'ai 20 ans et je suis actuellement
          en formation avec le Centre Européen de Formation en Développement Web
          et Web Mobile. Passionnée par la création et le design, je m'épanouis
          dans le développement de sites web, en particulier avec WordPress.
        </p>

        <div class="presentation-container">
          <div class="presentation-column">
            <h3>Compétences</h3>
            <ul>
              <li>WordPress</li>
              <li>HTML5 & CSS3</li>
              <li>JavaScript</li>
              <li>Vue.js</li>
              <li>Git & GitHub</li>
              <li>Capcut Pro</li>
            </ul>
          </div>
          <div class="presentation-column">
            <h3>Expérience</h3>
            <p>
              Je suis en cours de création d'un site web dédié à la création de
              sites internet,
              <a href="https://webmastour.com" target="_blank">webmastour.com</a
              >.
            </p>
            Ce projet est destiné aux jeunes entrepreneuses qui souhaitent créer
            leur propre site à un prix accessible, avec un suivi personnalisé.
            Le service inclut un hébergement gratuit pendant un an, une
            réduction de 50% pour les années suivantes, ainsi qu'une formation
            WordPress offerte. Ce projet me tient à cœur car il permet aux
            femmes de discuter librement de leurs projets et de se sentir à
            l'aise dans un environnement de soutien.

            <p>
              Je travaille également comme monteuse vidéo pour une psychologue
              active sur Instagram,
              <a
                href="https://www.instagram.com/hafsa.psychologue"
                target="_blank"
                >@hafsa.psychologue</a
              >. Je monte ses conférences et ses vidéos courtes pour ses réseaux
              sociaux.
            </p>
          </div>
        </div>

        <!-- Instagram Feed -->
        <div class="instagram-container">
          <div class="instagram-media-wrapper">
            <blockquote
              class="instagram-media"
              data-instgrm-permalink="https://www.instagram.com/reel/C_GoIfeIr4_/?utm_source=ig_embed&amp;utm_campaign=loading"
            >
              <div>
                <a
                  href="https://www.instagram.com/reel/C_GoIfeIr4_/?utm_source=ig_embed&amp;utm_campaign=loading"
                  target="_blank"
                >
                  <img
                    src="//www.instagram.com/embed.js"
                    alt="Instagram Feed"
                  />
                </a>
              </div>
            </blockquote>
          </div>

          <div class="instagram-media-wrapper">
            <blockquote
              class="instagram-media"
              data-instgrm-permalink="https://www.instagram.com/reel/C-nyIaGoehX/?utm_source=ig_embed&amp;utm_campaign=loading"
            >
              <div>
                <a
                  href="https://www.instagram.com/reel/C-nyIaGoehX/?utm_source=ig_embed&amp;utm_campaign=loading"
                  target="_blank"
                >
                  <img
                    src="//www.instagram.com/embed.js"
                    alt="Instagram Feed"
                  />
                </a>
              </div>
            </blockquote>
          </div>

          <div class="instagram-media-wrapper">
            <blockquote
              class="instagram-media"
              data-instgrm-permalink="https://www.instagram.com/reel/C_tSAfEo0W0/?utm_source=ig_embed&amp;utm_campaign=loading"
            >
              <div>
                <a
                  href="https://www.instagram.com/reel/C_tSAfEo0W0/?utm_source=ig_embed&amp;utm_campaign=loading"
                  target="_blank"
                >
                  <img
                    src="//www.instagram.com/embed.js"
                    alt="Instagram Feed"
                  />
                </a>
              </div>
            </blockquote>
          </div>
        </div>

        <div class="presentation-column">
          <h3>Objectifs</h3>
          <p>
            Je suis à la recherche d'opportunités pour renforcer mes compétences
            en développement web. Mon objectif est de gagner de l'expérience, de
            lancer mon business avec Webmastour, et de continuer à apprendre
            tout en contribuant à des projets significatifs.
          </p>
        </div>
      </section>

      <!-- Créations Section -->
      <section id="creations">
        <!-- Projet 1 : CV en ligne -->
        <h2>Créations</h2>

        <CreationItem
          title="CV en ligne"
          image="/cv.png"
          description="Une page web interactive de mon CV avec toutes les informations professionnelles."
          creationDate="26/12/2023"
          technologies="HTML, CSS"
          link="/path/to/cv.pdf"
          github="https://github.com/manellouti/cv-repo"
        />

        <!-- Projet 2 : Webmastour -->
        <CreationItem
          title="Webmastour"
          image="/site.png"
          description="Un site web dédié aux jeunes entrepreneuses souhaitant créer un site web abordable avec suivi et formation."
          creationDate="18/08/2024"
          technologies="Wordpress,flatsome studio"
          link="https://webmastour.com"
        />
      </section>

      <!-- Contact Section -->
      <section id="contact">
        <h2>Contact</h2>
        <form @submit.prevent="sendEmail">
          <label for="name">Nom</label>
          <input type="text" id="name" v-model="name" required />

          <label for="subject">Objet</label>
          <input type="text" id="subject" v-model="subject" required />

          <label for="message">Message</label>
          <textarea id="message" v-model="message" required></textarea>

          <button type="submit">Envoyer</button>
        </form>
      </section>
    </main>

    <!-- Footer Section -->
    <footer>
      <CreationFooter />
    </footer>
  </div>
</template>

<script>
import emailjs from "emailjs-com";
import CreationItem from "@/components/CreationItem.vue";

export default {
  components: {
    CreationItem, // Déclaration de CreationItem ici
  },
  data() {
    return {
      name: "",
      subject: "",
      message: "",
    };
  },
  methods: {
    sendEmail() {
      const serviceID = "service_yq4s3rs";
      const templateID = "template_cqknbjf";
      const userID = "user_1Wxw6lbhrUghbZyqZ";

      const templateParams = {
        name: this.name,
        subject: this.subject,
        message: this.message,
      };

      console.log("Envoi des données : ", templateParams); // Log pour vérifier les données envoyées

      emailjs
        .send(serviceID, templateID, templateParams, userID)
        .then((response) => {
          console.log(
            "Email envoyé avec succès !",
            response.status,
            response.text
          );

          // Réinitialiser le formulaire après envoi
          this.name = "";
          this.subject = "";
          this.message = "";
        })
        .catch((error) => {
          console.error("Erreur lors de l'envoi de l'email:", error);
        });
    },

    loadInstagramScript() {
      const script = document.createElement("script");
      script.src = "//www.instagram.com/embed.js";
      script.async = true;
      document.body.appendChild(script);
    },
  },
  mounted() {
    this.loadInstagramScript();
  },
};
</script>

<style>
/* Style général de l'application */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #f5f5f5;
  margin-top: 40px;
}

/* Photo de profil */
.profile-photo {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  margin-top: 20px;
  transition: transform 0.3s ease;
}

.profile-photo:hover {
  transform: scale(1.05);
}

/* Conteneur global de présentation */
#presentation {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 40px auto;
  max-width: 1000px;
  text-align: center;
}

/* Conteneur pour aligner compétences et expérience en deux colonnes */
.presentation-container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 40px;
  flex-wrap: wrap;
  margin-top: 30px;
  width: 100%;
}

/* Style pour les colonnes de compétences et d'expérience */
.presentation-column {
  flex: 1;
  min-width: 300px;
  padding: 20px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  background-color: #ffffff;
  text-align: left;
}

.presentation-column h3 {
  font-size: 1.5em;
  margin-bottom: 15px;
  color: #2c3e50;
}

.presentation-column ul {
  list-style-type: none;
  padding-left: 0;
}

.presentation-column ul li {
  margin-bottom: 10px;
  font-size: 1.1em;
}

.presentation-column p {
  font-size: 1.1em;
  line-height: 1.8;
}

/* Adaptation responsive pour petits écrans */
@media (max-width: 768px) {
  .presentation-container {
    flex-direction: column;
    gap: 20px;
  }
}

/* Conteneur des créations pour les modals dynamiques */
.creations-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-top: 40px;
  padding: 20px;
}

h2 {
  font-size: 2.5em;
  margin-bottom: 20px;
  color: #2b2e2a;
}

h3 {
  font-size: 1.8em;
  margin-top: 30px;
  margin-bottom: 15px;
  color: #2c3e50;
}

p,
ul {
  font-size: 1.2em;
  line-height: 1.8;
}

/* Conteneur des blocs Instagram */
.instagram-container {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  padding: 20px;
}

/* Blocs Instagram */
.instagram-media-wrapper {
  width: 300px;
  transition: box-shadow 0.3s ease, transform 0.3s ease;
}

.instagram-media-wrapper:hover {
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  transform: translateY(-5px);
}

.instagram-media {
  background: #fff;
  border-radius: 5px;
  box-shadow: 0 0 1px 0 rgba(0, 0, 0, 0.5), 0 1px 10px 0 rgba(0, 0, 0, 0.15);
  padding: 20px;
}

/* Boutons */
button {
  padding: 12px 24px;
  background-color: #ccc6ad;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

button:hover {
  background-color: #ccc6ad;
  transform: scale(1.05);
}

/* Formulaire */
form {
  margin-top: 40px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 px 15px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  gap: 10px;
}

input,
textarea {
  padding: 12px;
  width: 100%;
  max-width: 450px;
  border: 1px solid #ccc;
  border-radius: 5px;
  transition: border-color 0.3s ease;
}

input:focus,
textarea:focus {
  border-color: #ccc6ad;
}

/* Footer Instagram */
.instagram-media .footer-text a {
  color: #ccc6ad;
  transition: color 0.3s ease;
}

.instagram-media .footer-text a:hover {
  color: #ccc6ad;
}
</style>
