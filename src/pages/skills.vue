<template>
  <f7-page id="display-relative">
    <f7-block-title id="title-fixed">SKILLS</f7-block-title>
    <f7-card>
      <f7-card-content>
        <f7-block-header>ANGULARJS</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="85" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>IONIC</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="80" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>CORDOVA</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="80" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>NODEJS</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="75" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>VUEJS</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="65" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>PHP</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="55" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
      <f7-card-content>
        <f7-block-header>SWIFT</f7-block-header>
        <p><f7-progressbar class="color-red" :progress="50" id="demo-inline-progressbar"></f7-progressbar></p>
      </f7-card-content>
    </f7-card>
  </f7-page>
</template>
<script>
export default {
  mounted() {
    console.log('okadfasdfasfd');
  },
  name: 'skills'
}
</script>
<style scoped>
#display-relative {
  padding-top: 0px!important;
  position: relative;
}
#title-fixed{
  margin-top:10px!important;
}
#display-relative > .page-content{
  padding-top: 0px!important;
}
</style>

