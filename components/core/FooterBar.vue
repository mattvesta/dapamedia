<template>
  <v-footer
    class="py-4"
    dark
    height="auto"
  >
    <v-container class="mx-auto">
      <v-row>
        <v-col cols="9">
          <!-- <base-btn
            v-for="social in socials"
            :key="social.meta.id"
            :href="social.href"
            class="ml-0 mr-3"
            square
            target="_blank"
          > -->
          <!-- <v-icon v-text="social.icon" /> -->
          <!-- </base-btn> -->
        </v-col>

        <v-spacer />

        <base-btn
          class="mr-0"
          square
          title="Go to top"
          @click="$vuetify.goTo(0)"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </base-btn>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
// import { ref, onMounted, defineComponent } from 'vue'
// import { butter } from '@/plugins/buttercms'

// export default defineComponent({
//   name: 'CoreFooter',
//   setup () {
//     const params = {
//       page: '1',
//       page_size: '10'
//     }
//     const socials = ref([])
//     const loaded = ref(false)
//     onMounted(async () => {
//       try {
//         await butter.content.retrieve(['socials'], params)
//           .then(function (resp) {
//             socials.value = resp.data.data.socials
//             loaded.value = true
//           })
//       } catch (error) {
//         console.log(error)
//       }
//     })
//     return {
//       socials,
//       loaded
//     }
//   }

// })
</script>
