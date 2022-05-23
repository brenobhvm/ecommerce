<!-- Please remove this file from your project -->
<template>
  <div class="pl-4 pr-4 row">
    <div
      v-for="(item, index) in items"
      :key="index"
      class="col-md-4 col-sm-4 col-xs-12"
    >
      <v-card outlined>
        <v-img
          :src="require(`../assets/img/home/${item.image}`)"
          class="white--text align-center"
          gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
          height="300px"
        >
          <h1 v-if="item.text" class="text-center font-size">
            {{ item.text }}
          </h1>
          <div v-if="item.button" class="text-center mt-2">
            <v-btn class="white--text caption" :href="item.button.link" text>
              {{ item.button.text }} <v-icon class="white--text caption">
                {{ item.button.icon }}
              </v-icon>
            </v-btn>
          </div>
        </v-img>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MediumCardsComponent',
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
