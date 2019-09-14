<template>
  <v-container>
    <h2>Blood</h2>
    <line-chart :chart-data="datacollection"></line-chart>
  </v-container>
</template>

<script>
export default {
  props: {
    val: {
      type: Array,
      default: () => []
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
        labels: this.val,
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: this.val
          },
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: this.val
          }
        ]
      }
    },
    getRandomInt() {
      return Math.floor(Math.random() * (50 - 5 + 1)) + 5
    }
  }
}
</script>
