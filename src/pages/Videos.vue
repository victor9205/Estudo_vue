<template>
  <main>
    <section class="container">
      <h1>Vídeos</h1>

      <div class="text-top">
        Vídeos novos toda <b>quinta</b> às <b>20h</b><b>(Modelo)</b>
      </div>
      <a
        href="https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ"
        target=" blank"
      >
        <img
          alt="Inscreva-se"
          id="subscribe"
          src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg"
        />
        
<br />
      </a>
      <br />
      <br />
      <div class="text-bottom">
        https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ
      </div>

      <section class="videos">
        <div data-v-b7b48a08="" class="video">
          <a
            data-v-b7b48a08=""
            href="https://www.youtube.com/watch?v=vMUjisiXLeg&ab_channel=VictorRezende"
            target="blanck"
            ><img
              data-v-b7b48a08=""
              src="https://i.ytimg.com/an_webp/vMUjisiXLeg/mqdefault_6s.webp?du=3000&sqp=COD0lJIG&rs=AOn4CLDij7nV85C3PnwaHrOqqZNJ6JUKvA"
              alt="Rain Code"
            />
            <div data-v-b7b48a08="" class="video-title">Rain code</div>
          </a>
        </div>

        <div data-v-b7b48a08="" class="video">
          <a
            data-v-b7b48a08=""
            href="https://www.youtube.com/watch?v=XUceMBdfjeQ&ab_channel=VictorRezende"
            target="blanck"
            ><img
              data-v-b7b48a08=""
              src="https://i.ytimg.com/an_webp/XUceMBdfjeQ/mqdefault_6s.webp?du=3000&sqp=COzJlJIG&rs=AOn4CLDu4XkQPPD0oO4_SR19XnSr0mZBnQ"
              alt="Programing music zone"
            />
            <div data-v-b7b48a08="" class="video-title">
              Programing music zone
            </div>
          </a>
        </div>

        <div data-v-b7b48a08="" class="video">
          <a
            data-v-b7b48a08=""
            href="https://www.youtube.com/watch?v=CEDca4wHxSw&ab_channel=VictorRezende"
            target="blanck"
            ><img
              data-v-b7b48a08=""
              src="https://i.ytimg.com/an_webp/CEDca4wHxSw/mqdefault_6s.webp?du=3000&sqp=CNz2lJIG&rs=AOn4CLCcpphg8icvnkjloxFeRHWeoXjjMA"
              alt="Black and white Victor Rezende logo"
            />
            <div data-v-b7b48a08="" class="video-title">
              Black and white Victor Rezende logo
            </div>
          </a>
        </div>
      </section>
    </section>
  </main>
</template>

<script>
import api from "@/services/api.js";

export default {
  name: "Videos",
  data() {
    return {
      videos: [],
    };
  },
  mounted() {
    api.get("/videos.json").then((response) => {
      this.videos = response.data;
    });
  },
};
</script>

<style scoped>
main {
  align-items: center;
}

subscribe {
  width: 370px;
}

.videos {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.video {
  width: 80%;
  margin-bottom: 30px;
}

.video img {
  width: 100%;
}

.video a {
  color: var(--color-text-dark);
  font-weight: 600;
  margin-bottom: 30px;
  text-align: center;
}

@media (min-width: 800px) {
  #subscribe {
    width: 340px;
  }

  .videos {
    flex-direction: row;
    align-items: flex-start;
    flex-wrap: wrap;
  }

  .video {
    margin-right: 30px;
    width: 300px;
  }
}
</style>