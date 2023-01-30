<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>

      <div id="container">
        <ion-list>
          <ion-item>
            <ion-input type="text" v-model="myField" label="My field v-model"></ion-input>
          </ion-item>
          <ion-item>
            <ion-input type="text" :value="myFieldValueOnInput" label="My field value+onInput" @input="event => myFieldValueOnInput = event.target.value"></ion-input>
          </ion-item>
          <ion-item>
            <ion-input type="text" :value="myFieldValueOnIonInput" label="My field value+onIonInput" @ion-input="event => myFieldValueOnIonInput = event.target.value"></ion-input>
          </ion-item>
        </ion-list>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonInput, IonList, IonItem } from '@ionic/vue';

const myField = ref('')
const myFieldValueOnInput = ref('')
const myFieldValueOnIonInput = ref('')
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
