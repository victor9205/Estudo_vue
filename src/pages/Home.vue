<template>
  <main>
    <img
      alt="Tela Home Mobile"
      id="background-home-mobile"
      src="https://github.com/victor9205/Estudo_vue/blob/main/public/assets/media/MobileLogoBk.gif?raw=true"
    />
  </main>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
main {
  background-image: url(https://github.com/victor9205/Estudo_vue/blob/main/public/assets/media/DesktopBk.gif?raw=true);
  background-repeat: no-repeat;
  background-size: 100%;
  background-position: center center;
  background-attachment: fixed;
  /* background-color:var(--color-background-home); */
  justify-content: center;
  align-items: center;
}

#main {
  background-image: url(https://github.com/victor9205/Estudo_vue/blob/main/public/assets/media/MobileLogoBk.gif);
  background-repeat: no-repeat;
  background-size: contain;
  background-position: center;
  background-attachment: fixed;
  /* background-color:var(--color-background-home); */
  justify-content: center;
  align-items: center;
}

#content {
  background-image: url(https://github.com/victor9205/Estudo_vue/blob/main/public/assets/media/MobileLogoBk.gif);
  background-repeat: no-repeat;
  background-size: cover;
}

  #subscribe {
    width: 340px;
  }

.text-top {
  color: var(--color-text-light);
  font-size: 22px;
  margin-bottom: 20px;
}
#background-home-mobile {
  width: 100%;
  height: 50%;
}

.text-bottom {
  color: var(--color-text-light);
  font-size: 18px;
  margin-top: 20px;
}

@media (min-width: 800px) {
  #subscribe {
    width: 370px;
  }

  #background-home-mobile {
    width: 0;
  }
}
</style>