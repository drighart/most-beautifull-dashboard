<template>
  <div class="fully">
    <vl-map
      :load-tiles-while-animating="true"
      :load-tiles-while-interacting="true"
      data-projection="EPSG:4326">

      <vl-view :zoom.sync="zoom" :center.sync="center" :rotation.sync="rotation"></vl-view>

      <vl-layer-tile id="osm">
        <vl-source-osm></vl-source-osm>
      </vl-layer-tile>

      <vl-feature>
        <vl-geom-multi-point :coordinates="[[4.873064003762256, 52.20701787649713]]"></vl-geom-multi-point>
        <vl-interaction-draw :source="drawCollection" :type="drawType"></vl-interaction-draw>
      </vl-feature>
    </vl-map>
    <q-page-sticky position="top-left" :offset="[35, 100]">
        <div class="q-pa-md row items-start q-gutter-md">
            <q-card class="my-card">
                <q-card-section>
                    Teken een kader om het gebied waarin u de<br/>
                    afbeeldingen wilt selecteren. Middels de muiswiel<br/>
                    u inzoomen op de kaart. De kaart kunt u verplaatsen<br/>
                    door de muisknop ingedrukt te houden.
                </q-card-section>
            </q-card>
        </div>
    </q-page-sticky>

  </div>
</template>

<style scoped>
  .fully {
    position: fixed;
    height: 100%;
    width: 100%;
    object-fit: cover;
  }
</style>

<script>
export default {
  data () {
    return {
      zoom: 9,
      center: [4.873064003762256, 52.20701787649713],
      rotation: 0,
      drawType: 'Point',
      drawCollection: ''
    }
  }
}
</script>
