<template>
  <v-card tile>
    <v-card-text>
      <v-form>
        <v-text-field label="First Name" name="login" prepend-icon="mdi-account" type="text" />
        <v-text-field label="Last Name" name="login" prepend-icon="mdi-account" type="text" />
        <v-text-field
          label="Create Your Username"
          name="login"
          prepend-icon="mdi-account-edit"
          type="text"
        />

        <v-text-field
          v-model="pass"
          label="Set Password"
          name="password"
          prepend-icon="mdi-lock"
          type="password"
        />
        <v-text-field
          v-model="pass1"
          label="Re-enter Password"
          name="password"
          prepend-icon="mdi-lock"
          type="password"
          @keyup="verify"
        />
        <v-sheet class="red--text" v-model="warning">{{warning}}</v-sheet>
      </v-form>
    </v-card-text>
    <v-card-actions>
      <v-spacer />
      <v-btn color="primary">REGISTER</v-btn>
    </v-card-actions>
  </v-card>
  <!-- </v-col>

  </v-container>-->
</template>

<script>
export default {
  data () {
    return {
      dialog: 'true',
      warning: '',
      pass: '',
      pass1: ''
    }
  },
  methods: {
    verify: function (event) {
      if (this.pass !== this.pass1 && this.pass1.length > 0) {
        this.warning = 'Passwords do not match'
      } else this.warning = ''
    }
  }
}
</script>
