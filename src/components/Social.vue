<template>
  <div class="container">
    <div class="row q-pt-md">
      <p class="texte">{{ title }}</p>
    </div>
    <div class="row q-gutter-lg q-pt-md">
      <q-btn
        round
        class="button"
        size="md"
        href="https://www.facebook.com/lescentresrelier"
        target="_blank">
        <q-icon name="fab fa-facebook" color="white"/>
      </q-btn>
      <q-btn
        round
        class="button"
        size="md"
        href="https://www.linkedin.com/company/centres-relier"
        target="_blank">
        <q-icon name="fab fa-linkedin" color="white"/>
      </q-btn>
      <q-btn
        round
        class="button"
        size="md"
        href="https://www.youtube.com/channel/UCPsRsuLXqMPdLNlyxMhV6IA"
        target="_blank">
        <q-icon name="fab fa-youtube" color="white"/>
      </q-btn>
      <q-btn
        round
        class="button"
        size="md"
        href="https://www.instagram.com/centresrelier/"
        target="_blank">
        <q-icon name="fab fa-instagram" color="white"/>
      </q-btn>
      <q-btn
        round
        class="button"
        size="md"
        href="https://centresrelier.org/"
        target="_blank">
        <q-icon name="link" color="white"/>
      </q-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: 'social-component',
  props: {
    title: String,
  },
};
</script>

<style lang="scss" scoped>
.container {
  height: 240px;
  background-color: #EDF9FF;
  background-repeat: no-repeat;
  background-position: left, 100%, 0%;
}

.texte {
  font-weight: 600;
  font-size: 24px;
  line-height: 24px;
  text-align: center;
  color: $secondary;
  padding-top: 53px;
}

.row {
  justify-content: center;
}

.button {
  background-color: $light-blue;
  transition: 0.3s;
}

.button:hover {
  background-color: $accent;
}
</style>
