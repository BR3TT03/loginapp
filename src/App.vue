<template>
  <v-app>
    <v-content>
      <v-dialog v-model="dialog" persistent max-width="400" no-click-animation overlay-opacity="0">
        <div>
        <toolbar />
        <router-view />
        </div>
      </v-dialog>
    </v-content>
  </v-app>
</template>
<script>
import toolbar from './components/toolbar'
export default {
  data () {
    return {
      dialog: 'true'
    }
  },
  components: {
    toolbar
  }
}
</script>
