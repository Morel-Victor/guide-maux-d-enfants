<template>
  <div class="container">
    <router-link
      class="link"
      :to="{ name: 'help' }">
      <div>
        <img class="img" src="/statics/i.png" />
      </div>
    </router-link>
    <q-tooltip class="tooltip bg-secondary"
               anchor="top middle"
               self="bottom middle"
               :offset="[0, 5]">
      <strong>plus d'infos</strong>
    </q-tooltip>
  </div>
</template>
<script setup>
</script>
<style scoped>
.img {
  width: 14px;
  padding-top: 7px;
}
.container {
  width: 50px;
  height: 50px;
  border: 3px solid #26256C;
  border-radius: 200px;
  margin-left: 10px;
  transition: background-color 0.3s;
  text-align-last: center;
}

.container:hover {
  background-color: rgba(38, 37, 108, 0.3);
  cursor: pointer;
}

@media only screen and (min-device-width : 320px) and (max-device-width : 768px) {
  .container {
    width: 46px;
    height: 46px;
  }
}
</style>
