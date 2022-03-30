<template>
  <main>
    <section class="container">
      <h1>Vídeos</h1>

      <section class="videos">
        <div data-v-b7b48a08="" class="video">
          <a
            data-v-b7b48a08=""
            href="https://www.youtube.com/watch?v=vMUjisiXLeg&ab_channel=VictorRezende"
            target="blanck"
            ><img
              data-v-b7b48a08=""
              src="https://i.ytimg.com/an_webp/vMUjisiXLeg/mqdefault_6s.webp?du=3000&sqp=CNCdkpIG&rs=AOn4CLCQTDLy1TDochc8OHEu5AmSa6WfgQ"
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
              src="https://i.ytimg.com/an_webp/XUceMBdfjeQ/mqdefault_6s.webp?du=3000&sqp=CJzJkpIG&rs=AOn4CLDI1F1asAClz9zMNmS8RTsZ0BVHyA"
              alt="Programing music zone"
            />
            <div data-v-b7b48a08="" class="video-title">Programing music zone</div>
          </a>
        </div>

                <div data-v-b7b48a08="" class="video">
          <a
            data-v-b7b48a08=""
            href="https://www.youtube.com/watch?v=CEDca4wHxSw&ab_channel=VictorRezende"
            target="blanck"
            ><img
              data-v-b7b48a08=""
              src="https://i.ytimg.com/an_webp/CEDca4wHxSw/mqdefault_6s.webp?du=3000&sqp=CKC1kpIG&rs=AOn4CLDF7_Yxs1H5-7SpQMFuqTPFMbIpHQ"
              alt="Black and white Victor Rezende logo"
            />
            <div data-v-b7b48a08="" class="video-title">Black and white Victor Rezende logo</div>
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

@media (min-width: 700px) {
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