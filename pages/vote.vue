<template>
<v-container>
  <v-col class="padding-bottom">
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card elevation="0">
      <v-slide-item class="text-right pb-2">
        <div>2/3</div>
        </v-slide-item>
      <v-progress-linear v-model="value" :indeterminate="query" :query="true"></v-progress-linear>
        <v-card-title>
          Vote
        </v-card-title>
        <v-card-subtitle class="headline">
          <h3>Should we implement After Action Reviews?</h3>
        </v-card-subtitle>
        <v-card-text>
          <p>We want your input on whether we should do after action reviews as a group after our projects end.</p>
        </v-card-text>
      </v-card>
    </v-col>
    <v-col>
      Image
    </v-col>
  </v-row>
  </v-col>
  <v-row class="bottom-buttons">
    <v-col lg=6 md=4 sm=2 justify="left">
    <v-card-actions>
    <v-btn
      large
      elevation="0"
      min-height="4"
      min-width="6"
      class="btn-style"
      color="primary"
      nuxt
      to="/"
    >
      <v-icon>mdi-chevron-left</v-icon>
    </v-btn>
      <v-list-item-title align="left">
      Previous
      <p>Main</p>
      </v-list-item-title>
  </v-card-actions>
    </v-col>
    <v-col lg=6 md=4 sm=2 justify="right">
    <v-card-actions>
      <v-list-item-title align="right">
        Next
        <p>Vote</p>
      </v-list-item-title>
    <v-spacer />
    <v-btn
      large
      elevation="0"
      min-height="4"
      min-width="6"
      class="btn-style"
      color="primary"
      nuxt
      to="/results"
    >
      <v-icon>mdi-chevron-right</v-icon>
    </v-btn>
    </v-card-actions>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
export default {
  data () {
    return {
      value: 50,
      query: false,
    }
  }
}
</script>

<style>
.btn-style {
  border-radius: 8px;
}
.padding-bottom {
  margin-bottom: 10rem;
}
</style>