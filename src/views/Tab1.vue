<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <div id="main">
        <header>
          <h1>CIAO</h1>
        </header>
        
        <div class="input">
          <button @click="stampa()">check</button>
          <ion-item>
            <ion-input type="text" clear-input='true' @input="get($event)" id="nuovo" placeholder="nuovo panino"></ion-input>
          </ion-item>
        </div>

      </div>
      <ExploreContainer name="Tab 1 page" />
    </ion-content>
  </ion-page>
</template>

<script lang="js">
import { IonPage, IonContent } from '@ionic/vue';


export default  {
  name: 'Tab1',
  components: {IonContent, IonPage },

  data(){
      return{
        text: ''
      }
  },

    methods: {
      stampa(){
        console.log(this.text);
      },
      get($event){
        this.text = $event.target.value
      }
    }
}
</script>