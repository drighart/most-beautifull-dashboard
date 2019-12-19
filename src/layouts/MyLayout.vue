<template>
  <q-layout view="lHh Lpr lFf">
    <q-toolbar class="text-primary">
      <q-btn flat round dense icon="menu" />
      <img src="statics/icons/icon-128x128.png">
      <q-toolbar-title>
        Afbeeldingen zoeken
      </q-toolbar-title>
      <q-space />

      <q-tabs v-model="tab" shrink>
        <q-tab name="tab1" label="Map" />
        <q-tab name="tab2" label="Tab 2" />
        <q-tab name="tab3" label="Tab 3" />
      </q-tabs>
      <q-avatar>
        <img src="https://cdn.quasar.dev/img/boy-avatar.png">
      </q-avatar>
      <q-btn flat round dense icon="more_vert" />
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
