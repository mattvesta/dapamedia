<template>
  <v-app-bar
    app
    flat
  >
    <v-app-bar-nav-icon
      class="hidden-md-and-up"
      @click="toggleDrawer"
    />

    <v-container class="mx-auto py-0">
      <v-row align="center">
        <v-img
          :src="require('@/static/v.png')"
          class="mr-5"
          contain
          height="48"
          width="48"
          max-width="48"
          @click="$vuetify.goTo(0)"
        />
        <v-btn
          v-for="(link, i) in links"
          :key="i"
          v-bind="link"
          class="hidden-sm-and-down"
          text
          @click="onClick($event, link)"
        >
          {{ link.text }}
        </v-btn>
        <router-link
          to="/Blog"
          class="v-btn"
        >
          <v-btn
            class="hidden-sm-and-down"
            text
            value="Blog"
            name="Blog"
          >
            Blog
          </v-btn>
        </router-link>
        <router-link
          to="/Podcasts"
          class="v-btn"
        >
          <v-btn
            class="hidden-sm-and-down"
            text
            value="Podcasts"
            name="Podcasts"
          >
            Podcasts
          </v-btn>
        </router-link>
        <router-link
          to="/League"
          class="v-btn"
        >
          <v-btn
            class="hidden-sm-and-down"
            text
            value="League"
            name="League"
          >
            Fantasy Football
          </v-btn>
        </router-link>
        <router-link
          to="/News"
          class="v-btn"
        >
          <v-btn
            class="hidden-sm-and-down"
            text
            value="League"
            name="League"
          >
            Gaming
          </v-btn>
        </router-link>
        <router-link
          to="/About"
          class="v-btn"
        >
          <v-btn
            class="hidden-sm-and-down"
            text
            value="League"
            name="League"
          >
            About
          </v-btn>
        </router-link>
        <v-spacer />

        <v-text-field
          append-icon="mdi-magnify"
          flat
          hide-details
          solo-inverted
          style="max-width: 300px;"
        />
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
// Utilities
import {
  mapGetters,
  mapMutations
} from 'vuex'

export default {
  name: 'CoreAppBar',

  computed: {
    ...mapGetters(['links'])
  },

  methods: {
    ...mapMutations(['toggleDrawer']),
    onClick (e, item) {
      e.stopPropagation()

      if (item.to || !item.href) { return }

      this.$vuetify.goTo(item.href.endsWith('!') ? 0 : item.href)
    }
  }
}
</script>
