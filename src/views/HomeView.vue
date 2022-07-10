<template>
  <div class="home">
    <L-map v-model="zoom"
      v-model:zoom="zoom"
      :center="[47.41322, -1.219482]">
      <l-tile-layer
        url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
      ></l-tile-layer>
      <l-marker :lat-lng="[47.41322, -1.219482]">
        <l-icon :icon-url="icon" :icon-size="[56, 56]" />
      </l-marker>
    </L-map>
  </div>
</template>

<script>
// @ is an alias to /src
import {
  LMap,
  LTileLayer,
  LMarker,
  LIcon,
} from '@vue-leaflet/vue-leaflet';
import { ref } from 'vue';

export default {
  name: 'HomeView',
  components: {
    LMap,
    LTileLayer,
    LMarker,
    LIcon,
  },
  setup() {
    const zoom = ref(7);
    return {
      zoom,
    };
  },
};
</script>

<style lang="scss">
.home {
  width: 100%;
  height: 100%;
}
</style>
