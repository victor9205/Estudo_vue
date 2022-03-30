<template>
  <main>
    <section class="container">
      <h1>contato</h1>
      <section class="contacts">
        <div data-v-e2804794="" class="contact">
          <div data-v-e2804794="" class="contact-title">Canal do YouTube</div>
          <a
            data-v-e2804794=""
            href="https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ"
            target="blank"
            >https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ</a
          >
        </div>

        <div class="contact">
          <div class="contact-title">Instagram</div>
          <a href="https://www.instagram.com/rezendefvictor/" target="blank"
            >instagram.com/rezendefvictor/</a
          >
        </div>

        <div class="contact">
          <div class="contact-title">Facebook</div>
          <a
            href="https://www.facebook.com/victor.freitasrezende"
            target="blank"
            >facebook.com/victor.freitasrezende</a
          >
        </div>

        <div class="contact">
          <div class="contact-title">Linkedin</div>
          <a href="www.linkedin.com/in/RezendeVictor" target="blank"
            >linkedin.com/in/RezendeVictor</a
          >
        </div>

        <div class="contact">
          <div class="contact-title">E-mail</div>
          <a href="victorrezende9205@gmail.com" target="blank"
            >victorrezende9205@gmail</a
          >
        </div>
      </section>
    </section>
  </main>
</template>

<script>
import api from "@/services/api.js";

export default {
  name: "Contato",
  data() {
    return {
      contacts: [],
    };
  },
  mounted() {
    api.get("/contacts.json").then((response) => {
      this.contacts = response.data;
    });
  },
};
</script>

<style scoped>
main {
  align-items: center;
}

.contacts {
  margin-bottom: 40px;
  color: var(--color-text-dark);
}

.contact-title {
  font-weight: 600;
  font-size: 18px;
}

.contact a {
  color: var(--color-text-dark);
}

.contact {
  margin-bottom: 20px;
}
</style>