<template>
  <q-card class="card q-mt-lg q-mb-sm">
    <div class="row">
      <div class="col-md-4">
        <div class="row">
          <div class="col-md-12 col">
            <div class="img-container q-mt-md q-ml-md">
              <img class="img" :src="'http://localhost:1337' + organisme.img" />
            </div>
          </div>
          <div class="col-md-12">
            <p class="title-coordinates">coordonées</p>
            <br>
            <p class="coordinates">{{ organisme.coordinate }}</p>
          </div>
          <div class="col-md-12 q-mb-md">
            <p class="title-thematique">thématique</p>
            <br>
            <div v-if="organisme.thematique.length <= 4" class="row">
              <div class="col-md-1">
              </div>
              <div class="col-md-10">
                <div class="row row-icons">
                  <div v-if="organisme.thematique.includes('addiction')" class="icon-container">
                    <q-img src="../assets/thematique-icons/addiction.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Addiction</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('violence')" class="icon-container">
                    <q-img src="../assets/thematique-icons/violence.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Violence</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('discimination')" class="icon-container">
                    <q-img src="../assets/thematique-icons/discrimination.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Discrimination</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('harcèlement')" class="icon-container">
                    <q-img src="../assets/thematique-icons/harcèlement.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Harcèlement</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('santé mentale')" class="icon-container">
                    <q-img src="../assets/thematique-icons/santémentale.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Santé mentale</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('sexualité')" class="icon-container">
                    <q-img src="../assets/thematique-icons/sexualité.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Sexualité</strong>
                    </q-tooltip>
                  </div>
                </div>
              </div>
              <div class="col-md-1">
              </div>
            </div>
            <div v-if="organisme.thematique.length > 4" class="row">
              <div class="col-md-2">
              </div>
              <div class="col-md-8">
                <div class="row row-icons">
                  <div v-if="organisme.thematique.includes('addiction')" class="icon-container">
                    <q-img src="../assets/thematique-icons/addiction.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Addiction</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('violence')" class="icon-container">
                    <q-img src="../assets/thematique-icons/violence.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Violence</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('discimination')" class="icon-container">
                    <q-img src="../assets/thematique-icons/discrimination.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Discrimination</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('harcèlement')" class="icon-container">
                    <q-img src="../assets/thematique-icons/harcèlement.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Harcèlement</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('santé mentale')" class="icon-container">
                    <q-img src="../assets/thematique-icons/santémentale.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Santé mentale</strong>
                    </q-tooltip>
                  </div>
                  <div v-if="organisme.thematique.includes('sexualité')" class="icon-container">
                    <q-img src="../assets/thematique-icons/sexualité.png"
                           height="55px"
                           width="55px"/>
                    <q-tooltip class="tooltip bg-secondary"
                               anchor="top middle"
                               self="bottom middle"
                               :offset="[0, 5]">
                      <strong>Sexualité</strong>
                    </q-tooltip>
                  </div>
                </div>
              </div>
              <div class="col-md-2">
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-8">
        <div class="row">
          <div class="col-md-12">
            <div class="row">
              <div class="col-md-5"></div>
              <div class="col-md-7">
                <p class="title q-pt-lg  q-pr-lg q-ml-lg">{{ organisme.title }}</p>
              </div>
            </div>
          </div>
          <div class="col-md-12 q-pr-lg texte-container">
            <p class="title-description">description</p>
            <br>
            <p class="description">{{ organisme.description }}</p>
          </div>
          <div class="col-md-12 q-mb-md button-container">
            <router-link
              class="link"
              :to="{ name: 'organismeDetail', params: { id: organisme.id } }">
              <q-btn
                class="button"
                rounded
                size="md">
                En savoir +
              </q-btn>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </q-card>
</template>

<script>
export default {
  name: 'organisme-card-component',
  props: {
    organisme: {},
  },
};

</script>
<script setup>
</script>

<style lang="scss" scoped>
.card {
  border: 4px solid $accent;
  border-radius: 15px;
  width: 980px;
  background-image: url( '../assets/background-card.png' );
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center, 100%, 0%;
}

.img-container {
  height: 172px;
  width: 288px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  border-radius: 10px;
}

.img {
  max-height: 172px;
  max-width: 288px;
  object-fit: contain;
  border-radius: 10px;
}

.title-coordinates {
  font-weight: 900;
  color: $accent;
  font-size: 18px;
  text-align: center;
  margin: 10px 24px 0 24px;
}

.coordinates {
  white-space: pre-line;
  font-weight: 500;
  color: #26256C;
  font-size: 18px;
  text-align: center;
  margin: 0 24px 15px 24px;
}

.title-thematique {
  font-weight: 900;
  color: $accent;
  font-size: 18px;
  text-align: center;
  margin: 10px 24px 0 24px;
}

.title {
  font-size: 24px;
  font-weight: bolder;
  color: $accent;
  text-align: center;
}

.title-description {
  font-weight: 900;
  color: $accent;
  font-size: 18px;
  margin: 0;
}

.texte-container {
  overflow-wrap: break-word;
}

.description {
  white-space: pre-line;
  font-weight: 500;
  color: $accent;
  font-size: 18px;
}

.button-container {
  text-align: center;
}

.button {
  text-transform: none;
  border: 3px solid $accent;
  font-family: 'Montserrat', sans-serif;
  font-weight: bolder;
  font-size: 28px;
  color: $accent;
  transition: 0.3s;
}

.button:hover {
  background-color: $accent;
  color: white;
}

.link {
  text-decoration: none;
}

.row-icons {
  justify-content: center;
}

.icon-container {
  background-image:
    url( '../assets/thematique-icons/round-blue.svg' );
  background-repeat: no-repeat;
  background-position: center, 100%, 0%;
  padding: 0 5px 10px 5px;
}

</style>
