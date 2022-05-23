<!-- Please remove this file from your project -->
<template>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item, index) in items"
      :key="index"
      :src="require(`../assets/img/home/${item.image}`)"
    >
      <v-row
        v-if="item.text"
        class="fill-height"
        align="center"
        justify="center"
      >
        <div class="display-2 white--text pl-5 pr-5 hidden-sm-only">
          <strong>{{ item.text }}</strong>
        </div>
        <br>
      </v-row>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  name: 'CarrosselComponent',
  props: {
    items: {
      type: Array,
      default () {
        return []
      }
    }
  }
}
</script>
