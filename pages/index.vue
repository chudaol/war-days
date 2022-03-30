<template>
  <v-row justify="center" align="center" class="mt-12 pt-12">
    <v-col cols="12" sm="8" md="6">
      <v-card
        style="background: linear-gradient(blue, yellow)"
      >
        <v-card-title class="headline text-center" style="word-break: break-word; font-size: 10em;">
          <h2>
            It has been <span class="font-weight-bold">{{ daysFromWar }}</span> days since the full-scale russian war in Ukraine started.
          </h2>
        </v-card-title>
        <v-card-text class="text-center">
          The war started on <strong>24.02.2022</strong>
        </v-card-text>
        <v-card-actions class="justify-center">
          <v-btn
            href="https://bit.ly/help-ua-now"
          >
            Help Ukraine
          </v-btn>
        </v-card-actions>
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
