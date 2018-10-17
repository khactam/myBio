<template>
  <f7-page>
    <f7-navbar title="About Me"></f7-navbar>
    <f7-card style="background-color:transparent;box-shadow:none;">
        <img src="../../static/img/peachpit.jpg" width="100%" style="border-radius:50%" />
    </f7-card>
    <f7-card>
      <f7-card-header>
        BIO
      </f7-card-header>
      <f7-card-content>
        <b>Fullname</b>: Khac Tam Nguyen
        <br>
        <b>Funnyname</b>: Tommi
        <br>
        <b>D.O.B</b>: 23.3.1995
        <br>
        <b>Nationality</b>: Vietnam
        <br>
        <b>Zodiac</b>: Aries
      </f7-card-content>
    </f7-card>
    <f7-card
  content="Hello, few words about me. I'm a developer who love doing right thing but still drink when I code so thing is not so right. Love being somewhere that is strange and new (can be a new house of a lady) or just being somewhere peaceful (like in random lady's bed)."></f7-card>
    <f7-list media-list inset>
      <f7-list-item
        title="My anthem"
        link="https://www.youtube.com/watch?v=PRXtbLqIx04"
        external
        subtitle="Peach Pit">
        <img slot="media" src="../../static/img/peachpit.jpg" width="50" />
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>
<script>
export default {}
</script>
<style scoped>

</style>

