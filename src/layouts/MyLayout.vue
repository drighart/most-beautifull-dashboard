<template>
  <q-layout view="lHh Lpr lFf">
    <q-toolbar class="text-primary">
      <q-btn flat round dense icon="menu" />
      <img src="statics/app-logo-toolbar.png" to="/home">
      <q-toolbar-title>
        Afbeeldingen zoeken
      </q-toolbar-title>
      <q-space />

      <q-tabs v-model="tab" shrink>
        <q-route-tab name="tab1" label="Afbeeldingen" to="/home" exact/>
        <q-route-tab name="tab2" label="Map" to="/map" exact/>
      </q-tabs>
      <q-avatar>
        <img src="https://cdn.quasar.dev/img/boy-avatar.png">
      </q-avatar>
    </q-toolbar>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MyLayout',

  data () {
    return {
      leftDrawerOpen: false
    }
  }
}
</script>
