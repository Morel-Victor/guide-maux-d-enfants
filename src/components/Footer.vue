<template>
  <div class="container">
    <div class="row">
      <p class="texte">{{ title }}</p>
    </div>
    <div class="col-md-12 q-mt-sm button-container">
      <router-link
        class="link"
        :to="{ name: `${url}` }">
        <q-btn
          class="button"
          rounded
          size="md">
          <p class="texte-button">{{ buttonText }}</p>
        </q-btn>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'footer-component',
  props: {
    title: String,
    url: String,
    buttonText: String,
  },
};
</script>

<style lang="scss" scoped>
.container {
  height: 370px;
  background-color: $green;
  background-image:
    url( '../assets/ellipse1-green-left-svg.svg' ),
    url( '../assets/ellipse2-green-right-svg.svg' );
  background-repeat: no-repeat;
  background-position: left, 100%, 0%;
}

.texte {
  font-weight: 600;
  font-size: 26px;
  line-height: 28px;
  text-align: center;
  color: $secondary;
  white-space: pre-line;
  padding-top: 100px;
}

.row {
  justify-content: center;
}

.button-container {
  text-align: center;
}

.button {
  text-transform: none;
  border: 3px solid $accent;
  font-family: 'Montserrat', sans-serif;
  font-weight: bolder;
  color: $accent;
  transition: 0.3s;
}

.button:hover {
  background-color: $accent;
  color: white;
}

.texte-button {
  font-size: 26px;
  margin: 5px 10px 5px 10px;
}

.link {
  text-decoration: none;
}

</style>
