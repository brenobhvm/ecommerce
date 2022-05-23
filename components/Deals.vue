<!-- Please remove this file from your project -->
<template>
  <v-container>
    <v-row no-gutters>
      <v-col :cols="12">
        <v-card-text
          class=""
          tile
          outlined
        >
          <v-card-title class="subheading ">
            {{ title }}
          </v-card-title>
          <v-divider />
          <br>
          <div class="row">
            <div
              v-for="(item, index) in items"
              :key="index"
              class="col-12 col-md-3 col-sm-6 col-xs-6 text-center"
            >
              <v-hover
                v-slot="{ hover }"
                open-delay="200"
              >
                <v-card
                  :elevation="hover ? 16 : 2"
                >
                  <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="require(`../assets/img/home/${item.image}`)"
                  >
                    <v-card-title v-if="item.title">
                      {{ item.title }}
                    </v-card-title>
                  </v-img>

                  <v-card-text class="text--primary text-center">
                    <div v-if="item.discount">
                      {{ item.discount }}
                    </div>
                    <div v-if="item.brand">
                      {{ item.brand }}
                    </div>
                  </v-card-text>

                  <div v-if="item.button" class="text-center">
                    <v-btn
                      :href="item.button.link"
                      class="ma-2"
                      outlined
                      color="info"
                    >
                      {{ item.button.text }}
                    </v-btn>
                  </div>
                </v-card>
              </v-hover>
            </div>
          </div>
        </v-card-text>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'DealsComponent',
  props: {
    title: {
      type: String,
      default: ''
    },
    items: {
      type: Array,
      default () {
        return []
      }
    }
  }
}
</script>
