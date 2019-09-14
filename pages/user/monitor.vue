<template>
  <v-app>
    <v-container>
      <BloodSugar />
      <HeartBeats />
    </v-container>
  </v-app>
</template>

<script>
import BloodSugar from '@/components/BloodSugar'
import HeartBeats from '@/components/HeartBeats'
export default {
  components: {
    BloodSugar,
    HeartBeats
  }
}
</script>
