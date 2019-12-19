<template>
  <q-page class="flex flex-center">
    <div class="q-gutter-l" style="width: 800px">
      <q-input rounded outlined autofocus v-model="text" label="Voer een term in en zoek naar een afbeelding" style="font-size: 24px; height: 200px">
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
