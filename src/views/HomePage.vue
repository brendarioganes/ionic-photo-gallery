<template>
  <IonPage>
    <IonHeader>
      <IonToolbar>
        <IonTitle>Photo Gallery</IonTitle>
      </IonToolbar>
    </IonHeader>

    <IonContent :fullscreen="true">
      <div class="gallery-container">

        <div class="gallery-title">
          <span>MY IONIC APP</span>
          <h1>Photo Gallery</h1>
          <p>My favorite photos</p>
        </div>

        <IonGrid>
          <IonRow>

            <IonCol size="6">
              <IonCard class="photo-card">
                <img
                  src="/myimages/jana2.jpg"
                  alt="cutie jana"
                />
                <IonCardHeader>
                  <IonCardTitle>Pretty</IonCardTitle>
                </IonCardHeader>
              </IonCard>
            </IonCol>

            <IonCol size="6">
              <IonCard class="photo-card">
                <img
                  src="/myimages/jana3.jpg"
                  alt="sweet jana"
                />
                <IonCardHeader>
                  <IonCardTitle>Model</IonCardTitle>
                </IonCardHeader>
              </IonCard>
            </IonCol>

            <IonCol size="6">
              <IonCard class="photo-card">
                <img
                  src="/myimages/jana5.jpg"
                  alt="little jana"
                />
                <IonCardHeader>
                  <IonCardTitle>Cutie</IonCardTitle>
                </IonCardHeader>
              </IonCard>
            </IonCol>

            <IonCol size="6">
              <IonCard class="photo-card">
                <img
                  src="/myimages/jana4.jpg"
                  alt="big jana"
                />
                <IonCardHeader>
                  <IonCardTitle>Jana@9</IonCardTitle>
                </IonCardHeader>
              </IonCard>
            </IonCol>

          </IonRow>
        </IonGrid>

      </div>
    </IonContent>
  </IonPage>
</template>

<script setup lang="ts">
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
  IonGrid,
  IonRow,
  IonCol,
  IonCard,
  IonCardHeader,
  IonCardTitle
} from '@ionic/vue';
</script>

<style scoped>
ion-content {
  --background: url('/myimages/background.jpg') center / cover no-repeat;
}


.gallery-container {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  padding: 24px 16px;
}

.gallery-title {
  margin-bottom: 20px;
  text-align: center;
}

.gallery-title span {
  color: #3880ff;
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 2px;
}

.gallery-title h1 {
  margin: 5px 0;
  font-size: 2rem;
  font-weight: 700;
  color: #222;
}

.gallery-title p {
  margin: 0;
  color: #666;
}

ion-grid {
  padding: 0;
}

ion-col {
  padding: 6px;
}

.photo-card {
  margin: 0;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.12);
}

.photo-card img {
  width: 100%;
  height: 450px;
  object-fit: cover;
  display: block;
}

ion-card-header {
  padding: 12px;
}

ion-card-title {
  font-size: 1rem;
}
ion-toolbar {
  text-align: center;
}
</style>