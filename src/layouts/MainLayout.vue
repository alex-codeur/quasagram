<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white text-grey-10" bordered>
      <q-toolbar class="contain">
        <q-btn
          to="/camera"
          flat
          round
          icon="eva-camera-outline"
          size="15px"
          class="large-screen-only q-mr-sm"
          dense
        />
        <q-separator class="large-screen-only" vertical spaced />
        <q-toolbar-title class="text-grand-hotel text-bold">
          Quasagram
        </q-toolbar-title>
        <q-btn
          to="/"
          flat
          round
          icon="eva-home-outline"
          size="15px"
          class="large-screen-only"
          dense
        />
      </q-toolbar>
    </q-header>

    <q-footer class="bg-white small-screen-only" bordered>
      <q-tabs
        class="text-grey-10"
        active-color="primary"
        indicator-color="transparent"
      >
        <q-route-tab to="/" name="mail" icon="eva-home-outline" label="Home" />
        <q-route-tab
          to="/camera"
          name="camera"
          icon="eva-camera-outline"
          label="Camera"
        />
      </q-tabs>
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",
});
</script>

<style lang="sass">
.q-toolbar
  @media ( min-width:  $breakpoint-sm-min)
    height: 77px
.q-toolbar__title
  font-size: 30px
  @media ( max-width:  $breakpoint-xs-max)
    text-align: center
.q-footer
  .q-tab__icon
    font-size: 30px
</style>
