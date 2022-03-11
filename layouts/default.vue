<template>
  <v-app>
    <core-app-bar />
  </v-app>
</template>
<script>

export default ({
  name: 'App',
  components: {
    // CoreDrawer: () => import('@/components/core/Drawer'),
    // CoreFooter: () => import('@/components/core/Footer'),
    CoreAppBar: () => import('@/components/core/AppBar')
    // CoreView: () => import('@/components/core/View')
  }
})
</script>
  <style lang="sass">

  </style>
