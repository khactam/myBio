<template>
  <f7-page>
    <f7-navbar title="About My App" back-link="Back"></f7-navbar>
    <f7-card v-for="app in apps" :key="app.name">
      <f7-card-header>
        {{app.name}}
        <img :src="app.imgName" width="40" style="border-radius: 7px;" />
      </f7-card-header>
      <f7-card-content>
        <f7-row>
          <f7-col>
            {{app.description}}
          </f7-col>
        </f7-row>
        <br>
        <f7-row>
          <f7-col>
            <f7-link :href="app.link.apple" external>
              <img src="../../static/img/applestore.png" width="145">
            </f7-link>
          </f7-col>
          <f7-col>
            <f7-link :href="app.link.google" external>
              <img src="../../static/img/googlestore.png" width="170" id="google-store-pic">
            </f7-link>
          </f7-col>
        </f7-row>
      </f7-card-content>
    </f7-card>
    <f7-list>
      <f7-list-item title="Ivan Petrov" after="CEO">
      </f7-list-item>
      <f7-list-item title="John Doe" badge="5">
        <f7-icon slot="media" icon="demo-list-icon"></f7-icon>
      </f7-list-item>
      <f7-list-item title="Jenna Smith">
        <f7-icon slot="media" icon="demo-list-icon"></f7-icon>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      apps: [
        {
          name: "HyvääSuomesta",
          description: "The emoji application for HyvääSuomesta that included their event (summer 2017) for taking a picture or choosing from camera roll to put emojis in. The application was received nice feedback from customer and also the users. The purpose of the application is to spread their brands and marketing.",
          link: {
            apple: "https://itunes.apple.com/us/app/id1224610973",
            google: "https://play.google.com/store/apps/details?id=com.hyvaasuomesta.hyvaasuomesta&hl=en_US"
          },
          imgName: "../../static/img/hyvaa.png"
        },
        {
          name: "Raute",
          description: "The application for the exhibition of Raute. The main purpose of the app is to connect people and the company during the exhibition time, to check if any person at the desk and also to deliver company's latest technology and innovation to people during the exhibition and people using the app.",
          link: {
            apple: "https://itunes.apple.com/fi/app/raute/id1222893322?mt=8",
            google: "https://play.google.com/store/apps/details?id=com.superapp.raute"
          },
          imgName: "../../static/img/raute.png"
        },
        {
          name: "Harkkakyydit",
          description: "The application is for sharing cars within sport clubs. The application's idea was inspired by the sharing business which is dynamic and popular recently all over the world. The success of Uber, AirBnb or Lyft drives our customer to the idea to share cars within sport teams in some events where they can pay less and enjoy more.",
          link: {
            apple: "https://itunes.apple.com/kg/app/harkkakyydit/id1294238413?mt=8",
            google: "https://play.google.com/store/apps/details?id=com.superapp.kimppakyyti"
          },
          imgName: "../../static/img/harkkakyydit.png"
        }
      ]
    }
  }
}
</script>
<style scoped>
#google-store-pic{

}
</style>

