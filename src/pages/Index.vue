<template>
  <q-page class="flex flex-center">
    <div class="q-gutter-l" style="width: 800px">
      <q-input rounded outlined v-model="text" label="Voer een term in zoek naar een afbeelding">
        <template v-slot:prepend>
          <q-icon name="search" />
        </template>
      </q-input>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex'
}
</script>
