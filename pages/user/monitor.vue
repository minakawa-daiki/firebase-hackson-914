<template>
  <v-app>
    <v-container class="flex">
      <v-container>
        <h2>Blood</h2>
        <line-chart
          :chart-data="datacollection"
        ></line-chart>
        {{ datacollection }}
      </v-container>
      <!-- <heart-beats class="heart-beats" :val="heartRate" /> -->
    </v-container>
  </v-app>
</template>

<script>
// import HeartBeats from '@/components/HeartBeats'

export default {
  components: {
    // HeartBeats
  },
  data() {
    return {
      datacollection: {},
      heartRate: [],
      BloodSugar: []
    }
  },
  async mounted() {
    const oliverRef = this.$db
      .collection('users')
      .doc('oliver')
    const metricsRef = oliverRef
      .collection('metrics')
      .orderBy('createdAt')
      .limit(30)
    const metricsSnapshots = await metricsRef.get()
    const metricsDocs = metricsSnapshots.docs
    const heartRates = await Promise.all(
      metricsDocs.map((doc) => doc.data().heartRate)
    )
    const bloodSugarLevels = await Promise.all(
      metricsDocs.map((doc) => doc.data().bloodSugarLevel)
    )
    await oliverRef.onSnapshot((snapshot) => {
      heartRates.push(snapshot.data().heartRate)
      bloodSugarLevels.push(snapshot.data().bloodSugarLevel)
      this.BloodSugar = bloodSugarLevels
      this.heartRates = heartRates
      this.fillData()
    })
  },
  methods: {
    fillData() {
      console.log(this.BloodSugar)
      this.datacollection = {
        labels: this.BloodSugar,
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: this.BloodSugar
          },
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: this.BloodSugar
          }
        ]
      }
    }
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
