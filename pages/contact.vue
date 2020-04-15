<template>
  <v-container fluid class="contact">
    <v-card class="mx-auto mt-8 px-8 py-10 text-center" max-width="750">
      <v-card-title class="justify-center">
        <h2 class="display-2 font-weight-light mb-10">Contact</h2>
      </v-card-title>

      <v-card-text>
        <v-form ref="form" v-model="valid">
          <v-text-field
            label="Name"
            v-model="name"
            required
            :rules="nameRules"
            outlined
            color="cyan"
            class="mb-2"
          ></v-text-field>
          <v-text-field
            label="Email"
            v-model="email"
            required
            :rules="emailRules"
            outlined
            color="cyan"
            class="mb-2"
          ></v-text-field>
          <v-textarea
            label="Message"
            v-model="message"
            required
            outlined
            :rules="messageRules"
            color="cyan"
            class="mb-2"
          ></v-textarea>
          <v-btn outlined color="cyan" @click="submit">Send</v-btn>
        </v-form>
      </v-card-text>
    </v-card>
  </v-container>
</template>

<script>
import axios from 'axios'

export default {
  head() {
    return {
      title: 'Contact'
    }
  },
  data() {
    return {
      valid: true,
      name: '',
      email: '',
      message: '',
      nameRules: [v => !!v || 'Name is required'],
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      ],
      messageRules: [v => !!v || 'Message is required']
    }
  },
  methods: {
    submit() {
      const CORS_PROXY = 'https://cors-anywhere.herokuapp.com/'
      const URL =
        'https://docs.google.com/forms/u/0/d/e/1FAIpQLSenehIKe5jEKctNUzPKqCECjr6kVFMWyyP7pZN9Euohqa8eFw/formResponse'
      const params = new FormData()
      params.append('entry.1545138541', this.email)
      params.append('entry.1546633810', this.name)
      params.append('entry.1170533306', this.message)

      if (this.$refs.form.validate()) {
        axios
          .post(CORS_PROXY + URL, params)
          .then(response => {
            console.log(response)
            window.alert('Your message was sent. Thx!!')
          })
          .catch(response => {
            console.log(response)
            window.alert('Error... Please retry.')
          })
      }
    }
  }
}
</script>

<style lang="scss">
.contact {
  background: linear-gradient(-135deg, #00bcd4, #e0f7fa);
  width: 100vw;
  height: 100vh;
}
</style>
