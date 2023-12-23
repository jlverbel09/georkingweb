<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button color="primary"></ion-menu-button>
        </ion-buttons>
        <ion-title>{{ $route.params.id }}</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">

      <ion-item v-for="(item, index) in [
        {
          id : 1,
          nombre: 'Jorge Verbel',
        },
        {
          id : 1,
          nombre: 'Maria Luisa',
        },
        {
          id : 1,
          nombre: 'Jose Marco',
        },
        {
          id : 1,
          nombre: 'Daniela Santos',
        },
      ]" :key="index">
        <ion-label>{{ item.id  }} - {{ item.nombre }}</ion-label>
        <ion-button color="warning" shape="round">Editar</ion-button>
        <ion-button color="danger" shape="round">Eliminar</ion-button>
      </ion-item>

    </ion-content>
  </ion-page>
</template>

<script >

import { IonButton, IonContent, IonHeader, IonMenuButton, IonPage, IonTitle, IonToolbar, IonItem, IonLabel } from '@ionic/vue';

import { defineComponent } from 'vue';

export default defineComponent({
  components: { IonItem, IonLabel, IonButton },
});

</script>

<style scoped>

</style>
