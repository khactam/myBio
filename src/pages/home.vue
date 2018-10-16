<template>
  <f7-page :page-content="false">
    <!-- header -->
    <f7-navbar>
      <f7-nav-left>
        <f7-link icon-if-ios="f7:menu" icon-if-md="material:menu" panel-open="left"></f7-link>
      </f7-nav-left>
      <f7-nav-title>My personal app</f7-nav-title>
    </f7-navbar>
    <!-- main body -->
    <f7-tabs swipeable>
      <f7-tab id="skills" class="page-content" tab-active>
        <skills></skills>
      </f7-tab>
      <f7-tab id="career" class="page-content">
        <career></career>
      </f7-tab>
      <f7-tab id="tab-3" class="page-content">
        <f7-block>
          <p>test</p>
        </f7-block>
      </f7-tab>
    </f7-tabs>
    <!-- <f7-block-title>Modals</f7-block-title>
    <f7-block strong>
      <f7-row>
        <f7-col width="50">
          <f7-button fill raised popup-open="#popup">Popup</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button fill raised login-screen-open="#login-screen">Login Screen</f7-button>
        </f7-col>
      </f7-row>
    </f7-block> -->
    <!-- bottom -->
    <f7-toolbar tabbar>
      <f7-link tab-link="#skills" tab-link-active>
        <f7-icon f7="home"></f7-icon>
      </f7-link>
      <f7-link tab-link="#career">
        <f7-icon f7="graph_square"></f7-icon>
      </f7-link>
      <f7-link tab-link="#tab-3">
        <f7-icon f7="paper_plane"></f7-icon>
      </f7-link>
    </f7-toolbar>
  </f7-page>
</template>
<script>
import Skills from './skills.vue'
import Career from './career.vue'
export default {
  components: {
    skills: Skills,
    career: Career
  }
}
</script>
