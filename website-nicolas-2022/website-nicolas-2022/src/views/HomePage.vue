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
      <ion-button @click="goToButton()">List des button</ion-button>
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
      <div>
        <ion-card>
          <ion-card-header>
            <ion-card-subtitle>Card Subtitle</ion-card-subtitle>
            <ion-card-title>Card Title</ion-card-title>
          </ion-card-header>

          <ion-card-content>
            Keep close to Nature's heart... and break clear away, once in
            awhile, and climb a mountain or spend a week in the woods. Wash your
            spirit clean.
          </ion-card-content>
        </ion-card>

        <ion-card>
          <ion-item>
            <ion-icon :icon="pin" slot="start"></ion-icon>
            <ion-label>ion-item in a card, icon left, button right</ion-label>
            <ion-button fill="outline" slot="end">View</ion-button>
          </ion-item>

          <ion-card-content>
            This is content, without any paragraph or header tags, within an
            ion-card-content element.
          </ion-card-content>
        </ion-card>

        <ion-card>
          <ion-item href="#" class="ion-activated">
            <ion-icon :icon="wifi" slot="start"></ion-icon>
            <ion-label>Card Link Item 1 activated</ion-label>
          </ion-item>

          <ion-item href="#">
            <ion-icon :icon="wine" slot="start"></ion-icon>
            <ion-label>Card Link Item 2</ion-label>
          </ion-item>

          <ion-item class="ion-activated">
            <ion-icon :icon="warning" slot="start"></ion-icon>
            <ion-label>Card Button Item 1 activated</ion-label>
          </ion-item>

          <ion-item>
            <ion-icon :icon="walk" slot="start"></ion-icon>
            <ion-label>Card Button Item 2</ion-label>
          </ion-item>
        </ion-card>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonCard,
  IonCardContent,
  IonCardHeader,
  IonCardSubtitle,
  IonCardTitle,
  IonIcon,
  IonItem,
  IonLabel,
} from "@ionic/vue";
import { pin, walk, warning, wifi, wine } from "ionicons/icons";
import {
  IonContent,
  IonHeader,
  IonPage,
  IonTitle,
  IonToolbar,
  IonButton,
} from "@ionic/vue";
import { defineComponent } from "vue";
import { useRouter } from "vue-router";

export default defineComponent({
  name: "HomePage",
  components: {
    IonCard,
    IonCardContent,
    IonCardHeader,
    IonCardSubtitle,
    IonCardTitle,
    IonIcon,
    IonItem,
    IonLabel,
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonButton,
  },
  setup() {
    const router = useRouter();
    const goToButton = () => {
      router.push("/button");
    };
    return { warning, goToButton };
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
