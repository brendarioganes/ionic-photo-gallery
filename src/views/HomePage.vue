<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>My Photo Gallery</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content class="ion-padding">
      <CameraComponent @photo-captured="addPhoto" />

      <PhotoGalleryComponent :photos="photos" />
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
} from "@ionic/vue";

import { ref } from "vue";

import CameraComponent from "@/components/CameraComponent.vue";
import PhotoGalleryComponent from "@/components/PhotoGalleryComponent.vue";

const photos = ref<string[]>([]);

const addPhoto = (photo: string) => {
  photos.value.unshift(photo);
};
</script>
<style scoped>
ion-content {
  --background: #f7f3ff;
}

ion-toolbar {
  --background: #6c4ab6;
  --color: white;
}

ion-title {
  font-weight: 700;
}

ion-card {
  --background: white;
  border-radius: 16px;
  box-shadow: 0 4px 12px rgba(108, 74, 182, 0.15);
}

ion-card-title {
  color: #5a3d91;
  font-weight: 700;
}

ion-button {
  --background: #6c4ab6;
  --background-hover: #5a3d91;
  --color: white;
  --border-radius: 12px;
  font-weight: 600;
}
</style>