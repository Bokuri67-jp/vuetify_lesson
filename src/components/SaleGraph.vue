<template>
  <v-card
    class="mx-auto text-center"
    color="green"
    dark
  >
    <v-card-text>
      <v-sheet color="rgba(0, 0, 0, .12)">
        <v-sparkline
          :labels="labels"
          :value="value"
          color="rgba(255, 255, 255, .7)"
          stroke-linecap="round"
          smooth
        >
        </v-sparkline>
      </v-sheet>
    </v-card-text>
    <v-card-text>
      <div class="display-1 font-weight-thick">Sales</div>
    </v-card-text>
  </v-card>

</template>

<script>

export default {
  data: () => ({
    labels: [
      '12am',
      '3am',
      '6am',
      '9am',
      '12am',
      '3am',
      '6am',
      '9am'
    ],
    value: [
      423,
      446,
      675,
      675,
      510,
      510,
      590,
      590,
      610,
      610,
      760,
      760
    ]
  })
}
</script>
