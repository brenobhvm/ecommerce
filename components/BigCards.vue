<!-- Please remove this file from your project -->
<template>
  <div class="pl-4 pr-4 row">
    <div
      v-for="(item, index) in items"
      :key="index"
      class="col-md-6 col-sm-6 col-xs-12"
    >
      <v-card>
        <v-img
          :src="require(`../assets/img/home/${item.image}`)"
          class="white--text align-center"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
          height="400px"
        >
          <h1 v-if="item.text" class="text-center font-size">
            {{ item.text }}
          </h1>
          <div v-if="item.button" class="text-center">
            <v-btn :href="item.button.link" class="white--text " outlined>
              {{ item.button.text }}
            </v-btn>
          </div>
        </v-img>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BigCardsComponent',
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
