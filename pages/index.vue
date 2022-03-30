<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card
        style="background: linear-gradient(blue, yellow)"
      >
        <v-card-title class="headline text-center" style="word-break: break-word; font-size: 10em;">
          It has been {{ daysFromWar }} days since the full-scale russian war in Ukraine started.
        </v-card-title>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import moment from 'moment'
export default {
  name: 'IndexPage',
  computed: {
    daysFromWar () {
      const a = moment([2022, 1, 24]);
      const b = moment();
      return b.diff(a, 'days')
    }
  }
}
</script>
