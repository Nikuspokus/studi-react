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
        <strong>Ready to create an app?</strong>
        <p>
          Start with Ionic
          <a
            target="_blank"
            rel="noopener noreferrer"
            href="https://ionicframework.com/docs/components"
            >UI Components</a
          >
        </p>
      </div>
      <div>
        <!-- Default -->
        <ion-button>Default</ion-button>

        <!-- Anchor -->
        <ion-button href="#">Anchor</ion-button>

        <!-- Colors -->
        <ion-button color="primary">Primary</ion-button>
        <ion-button color="secondary">Secondary</ion-button>
        <ion-button color="tertiary">Tertiary</ion-button>
        <ion-button color="success">Success</ion-button>
        <ion-button color="warning">Warning</ion-button>
        <ion-button color="danger">Danger</ion-button>
        <ion-button color="light">Light</ion-button>
        <ion-button color="medium">Medium</ion-button>
        <ion-button color="dark">Dark</ion-button>

        <!-- Expand -->
        <ion-button expand="full">Full Button</ion-button>
        <ion-button expand="block">Block Button</ion-button>

        <!-- Round -->
        <ion-button shape="round">Round Button</ion-button>

        <!-- Fill -->
        <ion-button expand="full" fill="outline">Outline + Full</ion-button>
        <ion-button expand="block" fill="outline">Outline + Block</ion-button>
        <ion-button shape="round" fill="outline">Outline + Round</ion-button>

        <!-- Icons -->
        <ion-button>
          <ion-icon slot="start" name="star"></ion-icon>
          Left Icon
        </ion-button>

        <ion-button>
          Right Icon
          <ion-icon slot="end" name="star"></ion-icon>
        </ion-button>

        <ion-button>
          <ion-icon slot="icon-only" name="star"></ion-icon>
        </ion-button>

        <!-- Sizes -->
        <ion-button size="large">Large</ion-button>
        <ion-button>Default</ion-button>
        <ion-button size="small">Small</ion-button>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
  IonButton,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "ButtonList",
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton,
  },
});
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
