<template>
  <v-container>
    <h2>Heart</h2>
    <line-chart :chart-data="datacollection"></line-chart>
  </v-container>
</template>

<script>
export default {
  props: {
    val: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      datacollection: null
    }
  },
  mounted() {
    this.fillData()
  },
  methods: {
    fillData() {
      this.datacollection = {
        labels: [this.getRandomInt(), this.getRandomInt()],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [this.getRandomInt(), this.getRandomInt()]
          },
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [this.getRandomInt(), this.getRandomInt()]
          }
        ]
      }
    }
  }
}
</script>
