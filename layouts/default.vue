<template>
  <v-app light>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      elevation="0"
      color=white
    >
      <v-toolbar-title>
        <v-img src="Logo.png" />
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-side-icon 
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
          >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
      </v-toolbar-side-icon>
          <v-avatar
            color="accent"
            size="48"
          />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
        class="min-button"

      >
      <v-icon>mdi-chevron-down</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      fixed: false,
      items: [
        {
          icon: 'mdi-cog',
          title: 'Settings',
          to: '/settings'
        }
      ],
      slides: [
        {
          icon: 'mdi-chevron-left',
          title: 'Previous',
          to: '/info'
        },
        {
          icon: 'mdi-chevron-right',
          title: 'Next',
          to: '/vote'
        }
      ],
      miniVariant: false,
      right: true,
      title: 'HiveSquared',
    }
  }
}
</script>

<style>
.min-button::before {
  display: none;
}
</style>
