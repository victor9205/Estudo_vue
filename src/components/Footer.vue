<template>
  <footer>
    <a
      data-v-40ab164b=""
      href="https://www.instagram.com/rezendefvictor/"
      target="blank"
      class="socialLink"
      ><img
        data-v-40ab164b=""
        alt="Instagram"
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/icons/instagram.svg"
    /></a>

    <a
      data-v-40ab164b=""
      href="https://www.facebook.com/victor.freitasrezende"
      target="blank"
      class="socialLink"
      ><img
        data-v-40ab164b=""
        alt="Facebook"
        src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/icons/facebook.svg"
    /></a>

    <a
      data-v-40ab164b=""
      href="https://www.linkedin.com/in/RezendeVictor/"
      target="blank"
      class="socialLink"
      ><img
        data-v-40ab164b=""
        alt="Linkedin"
        src="https://trustworksglobal.com/wp-content/themes/trustworks-global/assets/svg/linkedin.svg"
    /></a>
  </footer>
</template>

<script>
import api from "@/services/api.js";

export default {
  name: "Footer",
  data() {
    return {
      socialLinks: [],
    };
  },

  mounted() {
    api.get("/social-links.json").then((response) => {
      this.socialLinks = response.data;
    });
  },
};
</script>

<style scoped>
footer {
  width: 100%;
  height: 50px;
  background-color: var(--color-background-nav);
  display: flex;
  justify-content: center;
  align-items: center;
}

.socialLink {
  border: 2px solid var(--color-text-lighty);
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  margin: 0 10px;
}

.socialLink img {
  width: 20px;
}
</style>
