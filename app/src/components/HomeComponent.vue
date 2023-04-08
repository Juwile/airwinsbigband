<template>
  <div>
    <h1>AIRWIN's Big Band</h1>
    <p>
      Wir bringen dich mit unseren Melodien in den Rausch der Jazz Musik. Nebst dem typischen Swing spielen wir Funk, Pop und Rock Arrangements. Der Kern hat AIRWIN’s Big Band im Sensebezirk, Freiburg. Mittlerweile wirken aber regelmässig auch Talente aus Bern, Basel oder der Romandie mit. Bandleader ist Erwin Mülhauser, der der Band auch ihren Namen gibt.
    </p>
    <div class="teaser-container">
      <div class="teaser">
        <h2>Über uns</h2>
        <img alt="Logo AIRWIN's Big Band" src="../assets/ABB_Bandfoto.jpg">
        <p>Freitext zu der Big Band des Sensebezirk und noch mehr und noch mehr</p>
        <button>Mehr Infos</button>
      </div>
      <div class="teaser">
        <h2>Aufnahmen</h2>
        <img alt="Logo AIRWIN's Big Band" src="../assets/ABB_Bandfoto.jpg">
        <p>Freitext zu der Big Band des Sensebezirk und noch mehr und noch mehr</p>
        <button>Mehr Infos</button>
      </div>
      <div class="teaser">
        <h2>Konzerte</h2>
        <img alt="Logo AIRWIN's Big Band" src="../assets/ABB_Bandfoto.jpg">
        <p>Freitext zu der Big Band des Sensebezirk und noch mehr und noch mehr</p>
        <button>Mehr Infos</button>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'HomeComponent',
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.teaser-container{
  display: flex;
  justify-content:center;
}

img{
  width: 100%;
}
.teaser{
  display: block;
  margin:0 2% 0 2%;
}

.teaser-container p{
  text-align: left;
}

</style>
