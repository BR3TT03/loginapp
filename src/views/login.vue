<template>
      <v-dialog
      v-model="dialog"
      persistent
      max-width="400"
      no-click-animation
      overlay-opacity=1
      >
        <v-card tile>
              <v-toolbar
                color="primary"
                dark
                flat
              >
                <v-toolbar-title>Famas Login</v-toolbar-title>
                <v-spacer />
              </v-toolbar>
              <v-card-text>
                <v-form>
                  <v-text-field
                    label="Login"
                    name="login"
                    prepend-icon="mdi-account"
                    type="text"
                  />
                  <v-text-field
                    id="password"
                    label="Password"
                    name="password"
                    prepend-icon="mdi-lock"
                    type="password"
                  />
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer />
                <v-btn color="primary">LOGIN</v-btn>
                <v-btn color="primary"><router-link to="/register">REGISTER</router-link></v-btn>
              </v-card-actions>
            </v-card>
          <!-- </v-col>
      </v-container> -->
      </v-dialog>
</template>
<script>
export default {
  data () {
    return { 
        dialog:'true',
      }
    },
    props: {
      source: String,
    },
  }
</script>