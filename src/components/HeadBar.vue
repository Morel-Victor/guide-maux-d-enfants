<template>
  <div v-if="$q.screen.gt.sm" class="container">
    <div class="row">
      <p class="texte">
        {{ title1 }}
        <br>
        {{ title2 }}
      </p>
    </div>
  </div>
  <div v-else class="container-mobile">
    <div class="row-mobile">
      <p class="texte-mobile">
        {{ title1 }}
        <br>
        {{ title2 }}
      </p>
    </div>
  </div>
</template>

<script setup>
const title1 = 'Le guide Maux d\'enfants mode d\'emploi';
const title2 = 'Des organismes gratuits pour accompagner vos enfants';
</script>

<style lang="scss" scoped>
.container {
  height: 128px;
  background-color: $primary;
  background-image:
    url( '/statics/ellipse1.svg' ),
    url( '/statics/ellipse2.svg' );
  background-repeat: no-repeat;
  background-position: left, 100%, 0%;
}

.container-mobile {
  height: 100px;
  background-color: $primary;
  background-image:
    url( '/statics/ellipse1mobile.svg' ),
    url( '/statics/ellipse2mobile.svg' );
  background-repeat: no-repeat;
  background-position: left, 100%, 100%;
}

.texte-mobile {
  font-weight: 600;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: $secondary;
  padding: 20px 10px 0px 10px;
  margin-bottom: 0;
  height: 100px;
}

.texte {
  font-weight: 600;
  font-size: 20px;
  line-height: 24px;
  text-align: center;
  color: $secondary;
  padding-top: 40px;
}

.row {
  height: 145px;
  justify-content: center;
}

.row-mobile {
  height: 100px;
  justify-content: center;
}

@media only screen and (min-device-width : 280px) and (max-device-width : 344px) {
  .texte-mobile {
    font-size: 14px;
    padding-top: 15px;
  }
}

</style>
