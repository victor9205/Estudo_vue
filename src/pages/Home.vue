<template>
  <main>
      <div class="text-top">Vídeos novos toda <b>quinta</b> às <b>20h</b><b>(Modelo)</b></div>

      <a href="https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ" target=" blank">
        <img alt="Inscreva-se" id="subscribe" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg">
      </a>
      <div class="text-bottom">https://www.youtube.com/channel/UC7467puGC8SbXr7vJV_YTpQ</div>
        
      

  </main>
</template>

<script>
export default {
  name: "Home"
}
</script>

<style scoped>

main{
    background-image: url('https://i.pinimg.com/originals/50/5f/62/505f6223f3624bfcd158cf827bd337da.jpg');
    background-repeat: no-repeat;
    background-size: 100%;
    /* background-color:var(--color-background-home); */
    justify-content: center;
    align-items: center;
}


.text-top{
    color: var(--color-text-light);
    font-size: 22px;
    margin-bottom: 20px;
}

#subscribe{
    width:340px;

}


.text-bottom{
    color: var(--color-text-light);
    font-size:18px;
    margin-top: 20px;
}

@media (min-width: 700px){
    #subscribe{
        width: 370px;  
    }
}
</style>