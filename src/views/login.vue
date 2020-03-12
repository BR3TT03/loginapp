<template>
  <v-card tile>
    <v-card-text>
      <v-form>
        <v-text-field label="UserName" name="username" prepend-icon="mdi-account" type="text" v-model="userName" />
        <v-text-field
          id="password"
          label="Password"
          name="password"
          prepend-icon="mdi-lock"
          type="password"
          v-model="password"
        />
      </v-form>
    </v-card-text>
    <v-card-actions>
      <v-spacer />
      <v-btn color="primary" @click="authenticate">LOGIN</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
import axios from 'axios'
export default {
  data () {
    return {
      userName: '',
      password: '',
      dialog: 'true'

    }
  },
  methods: {
    authenticate: function () {
      axios.post('http://10.42.0.88:9090/auth', {
        userName: this.userName,
        password: this.password
      })
        .then(response => {
          console.log(response)
        })
        .catch(error => {
          console.log(error)
        })
    }
  }
}
</script>
