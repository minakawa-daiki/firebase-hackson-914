<template>
  <v-app>
    <v-container class="flex">
      <blood-sugar
        class="blood-sugar"
        :val="bloodSugarLevel"
      />
      <heart-beats class="heart-beats" :val="heartRate" />
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
  },
  data() {
    return {
      heartRate: 0,
      bloodSugarLevel: 0
    }
  },
  mounted() {
    this.$db
      .collection('users')
      .doc('oliver')
      .onSnapshot(function(snapshot) {
        this.heartRate = snapshot.data().heartRate
        this.bloodSugarLevel = snapshot.data().bloodSugarLevel
      })
  }
}
</script>

<style lang="postcss">
.flex {
  display: flex;
}
.heart-beats,
.blood-sugar {
  width: 50%;
}
</style>
