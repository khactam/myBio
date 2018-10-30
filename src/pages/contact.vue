<template>
  <f7-page>
    <f7-block-title>Contact me</f7-block-title>
    <f7-list inline-labels no-hairlines-md>
      <f7-list-item>
        <f7-icon icon="demo-list-icon" slot="media"></f7-icon>
        <f7-label>Name:</f7-label>
        <f7-input :value="dataInfo.name" @input="dataInfo.name = $event.target.value" type="text" placeholder="Your name" clear-button></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon icon="demo-list-icon" slot="media"></f7-icon>
        <f7-label>Phone:</f7-label>
        <f7-input :value="dataInfo.number" @input="dataInfo.number = $event.target.value" type="number" placeholder="Your phone" clear-button></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon icon="demo-list-icon" slot="media"></f7-icon>
        <f7-label>E-mail:</f7-label>
        <f7-input :value="dataInfo.email" @input="dataInfo.email = $event.target.value" type="email" placeholder="Your e-mail" clear-button></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-icon icon="demo-list-icon" slot="media"></f7-icon>
        <f7-label>Describe:</f7-label>
        <f7-input :value="dataInfo.description" @input="dataInfo.description = $event.target.value" type="textarea" resizable placeholder="Your sharing?"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-button style="margin:20px;" big raised outline v-on:click="sendEmail">Send</f7-button>
  </f7-page>
</template>
<script>
  export default {
    data (){
      return{
        dataInfo:{
          name:'',
          number:'',
          email:'',
          description:''
        },
        apikey: "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"
      }
    },
    methods: {
      send (e) {
        if (this.dataInfo.name && this.dataInfo.number && this.dataInfo.email && this.validEmail(this.dataInfo.email)) {
          console.log('OK');
          sendEmail()
        }
        if (!this.dataInfo.name) {
          console.log('Name required.');
        }
        if (!this.dataInfo.number) {
          console.log('Number required.');
        }
        if (!this.dataInfo.email) {
          console.log('Email required.');
        } else if (!this.validEmail(this.dataInfo.email)) {
          console.log('Valid email required.');
        }
      },
      validEmail: function (email) {
        var re = /^(([^<>()\[\]\\.,;:\s@"]+(\.[^<>()\[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
        return re.test(email);
      },
      sendEmail: function() {
        console.log("sent");
        let data = {
            "personalizations": [
              {
                "to": [
                  {
                    "email": "khactam95@gmail.com"
                  }
                ],
                "subject": "Hello, World!"
              }
            ],
            "from": {
              "email": this.dataInfo.email,
              "name": "test"
            },
            "reply_to": {
              "email": "khactam95@gmail.com",
              "name": "Tam Nguyen"
            },
            "content": [
              {
                "type": "text/plain",
                "value": "Hello, World!"
              }
            ]
          }
        axios.post('https://api.sendgrid.com/v3/mail/send' , data, {
          headers: {
            'Authorization' : 'Bearer ' + this.apikey,
            'Content-Type': 'application/json',
            "Access-Control-Allow-Origin": "*"
          },
        })
        .then((response) => {
          console.log(response.data);
        })
      }
    }
  }
</script>
<style scoped>

</style>
