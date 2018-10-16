<template :page-content="false">
  <f7-page id="display-relative">
    <f7-block>
      <f7-card outline v-for="career in careers" :key="career.title">
        <f7-card-header class="no-border">
          <div class="time" v-if="typeof(career.time.end) === 'number'">{{career.time.start}} - {{career.time.end}}</div>
          <div class="time" v-else-if="typeof(career.time.end) !== 'number'">{{career.time.start}} - Present</div>
          <div class="job-title">{{career.title}} ({{career.time.period}} years)</div>
        </f7-card-header>
        <f7-card-content>
          <div class="padding-fixed">
            <b>Company</b>: {{career.company}}
          </div>
          <div class="padding-fixed">
            <b>Description</b>: {{career.description}}
          </div>
        </f7-card-content>
      </f7-card>
    </f7-block>
  </f7-page>
</template>
<script>
export default {
  data () {
    return {
      careers: [
        {
          time: {
            start: 2016,
            end: new Date(),
            period: 0

          },
          title: "Software Engineer",
          description: "Develope amazing and exciting mobile applications and web applications for the clients. Been using various tools and programming languages to create mobile application such as Angular and AngularJS, Ionic and Cordova, Framework 7 and Vue for hybrid mobile applications and Swift for iOS. Many products are now live in AppStore and PlayStore like HyvääSuomesta, Raute, Matkaan, Harkkakyydit and so on.",
          company: "SuperApp Oy"
        },
        {
          time: {
            start: 2014,
            end: new Date(),
            period: 0
          },
          title: "Freelance developer",
          description: "Doing freelance for some hobby projects and private projects for customers. Been doing web applications and wordpress sites. The main technology used are AngularJS, Angular, PHP, Wordpress and ReactJS. Been trying ReactJS for few times but still need more projects to get used to it and master it. Coding is fun!",
          company: "Self-employed"
        },
        {
          time: {
            start: 2014,
            end: 2016,
            period: 0
          },
          title: "Co-founder",
          description: "Being a guy who loves travelling is the main reason to start my very first business. The idea of Klicking Meters is to connect people who love backpacking but don't have experience or friend who share the same hobby. I wasn't the first guy who started this but I joint and found it interesting and put efforts into it. Klicking Meters later on was stopped because we have different plans and since I moved oversea, I needed to focus on career path as a software engineer but one day, I will absolutely come back for it.",
          company: "Klicking Meters"
        },
      ]
    }
  },
  created () {
    this.careers.forEach(career => {
      if(typeof(career.time.end) !== "number") {
        let endTime = career.time.end.getFullYear();
        career.time.period = endTime - career.time.start;
      }
      else{
        career.time.period = career.time.end - career.time.start;
      }
    });
  }
}
</script>
<style scoped>
.time{
  font-size: 13px;
}
.job-title{
  float: left;
}
.padding-fixed{
  padding-bottom: 10px;
}
</style>
