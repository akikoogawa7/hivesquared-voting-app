<template>
<v-container>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card elevation="0">
        <v-card-title>
          Recorded Decisions
        </v-card-title>
        <v-card-subtitle class="headline">
          Yes, we should implement After Action Reviews
        </v-card-subtitle>
        <v-card-text>
          <p>This means we decided as a group to implement After Action Reviews.</p>
        </v-card-text>
      </v-card>
    </v-col>
    <v-col>
      Vote component
    </v-col>
  </v-row>
  <v-row>
      <v-card-actions>
    <v-spacer />
    <v-btn
      color="primary"
      nuxt
      to="/results"
    >
      Continue
    </v-btn>
  </v-card-actions>
  </v-row>
</v-container>
</template>

<script>
export default {
  data () {
    return {
      value: 100,
    }
  }
}
</script>