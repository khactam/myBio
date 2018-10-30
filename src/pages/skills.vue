<template>
  <f7-page id="display-relative" :page-content="false">
    <f7-block-title>Portfolio</f7-block-title>
    <f7-card>
      <f7-list>
        <f7-list-item link="/about/" title="See my apps"></f7-list-item>
      </f7-list>
    </f7-card>
    <f7-card>
      <f7-row>
        <f7-col class="center-grid">
          <f7-block>ANGULARJS</f7-block>
          <f7-gauge
            type="circle"
            :value="0.8"
            :size="50"
            border-color="#0b0b70"
            :value-text="`80%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>VUE</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`70%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
      </f7-row>
    </f7-card>
    <f7-card>
      <f7-row>
        <f7-col class="center-grid">
          <f7-block>IONIC</f7-block>
          <f7-gauge
            type="circle"
            :value="0.8"
            :size="50"
            border-color="#0b0b70"
            :value-text="`90%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>CORDOVA</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`75%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
      </f7-row>
    </f7-card>
    <f7-card>
      <f7-row>
        <f7-col class="center-grid">
          <f7-block>ANGULAR</f7-block>
          <f7-gauge
            type="circle"
            :value="0.8"
            :size="50"
            border-color="#0b0b70"
            :value-text="`60%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>NODEJS</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`65%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>REACT</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`50%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
      </f7-row>
    </f7-card>
    <f7-card>
      <f7-row>
        <f7-col class="center-grid">
          <f7-block>SWIFT</f7-block>
          <f7-gauge
            type="circle"
            :value="0.8"
            :size="50"
            border-color="#0b0b70"
            :value-text="`40%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>JAVA</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`40%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>C#</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`50%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
        <f7-col class="center-grid">
          <f7-block>PHP</f7-block>
          <f7-gauge
            type="circle"
            :value="0.7"
            :size="50"
            border-color="#0b0b70"
            :value-text="`40%`"
            :value-font-size="10"
            :border-width="7"
            value-text-color="#002766"
            id="gauge-center"
          ></f7-gauge>
        </f7-col>
      </f7-row>
    </f7-card>
  </f7-page>
</template>
<script>
export default {
  mounted() {
    console.log('Ready to bem');
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
#gauge-center{
  padding-top: 3px;
  display: inline-block;
  margin: auto;
}
.center-grid{
  text-align:center;
  padding: 10px;
}
</style>

