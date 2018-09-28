<template>
  <v-container fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout justify-center>
        <v-flex
          xs12
          sm6
        >
          <v-card>
            <v-img
              class="white--text"
              height="200px"
              src="https://o.aolcdn.com/images/dims3/GLOB/legacy_thumbnail/630x315/format/jpg/quality/85/http%3A%2F%2Fi.huffpost.com%2Fgen%2F4239218%2Fimages%2Fn-FULL-DAY-KINDERGARTEN-628x314.jpg"
            >
              <v-container
                fill-height
                fluid
              >
                <v-layout fill-height>
                  <v-flex
                    xs12
                    align-end
                    flexbox
                  >
                    <span class="headline">Sarcelles - Jaurès</span>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-img>

            <v-list subheader>
              <v-subheader>Elèves</v-subheader>
              <v-list-tile
                v-for="item in items"
                :key="item.title"
                avatar
                @click="showAlert('zezette');"
              >
                <v-list-tile-avatar>
                  <img :src="item.avatar">
                </v-list-tile-avatar>

                <v-list-tile-content>
                  <v-list-tile-title>
                    {{ item.name + ' ' + item.firstName }}
                  </v-list-tile-title>
                  <v-list-tile-sub-title>{{ item.level }}</v-list-tile-sub-title>
                </v-list-tile-content>

                <v-list-tile-action>
                  <v-icon :color="item.active ? 'teal' : 'grey'">chat_bubble</v-icon>
                </v-list-tile-action>
              </v-list-tile>
            </v-list>
          </v-card>
        </v-flex>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<script>
export default {
  name: 'StudentList',
  data() {
    return {
      items: [
        {
          name: 'Martin', firstName: 'Pascal', avatar: 'https://fr.seaicons.com/wp-content/uploads/2015/10/Sex-Male-icon.png', level: 'Grande section',
        },
        {
          name: 'Jjjjjj', firstName: 'Lucie', avatar: 'https://fr.seaicons.com/wp-content/uploads/2015/10/Sex-Female-icon.png', level: 'Grande section',
        },
        {
          name: 'Kkkjkj', firstName: 'Leon', avatar: 'https://fr.seaicons.com/wp-content/uploads/2015/10/Sex-Male-icon.png', level: 'Grande section',
        },
        {
          name: 'Plllsdqqdq', firstName: 'Patrick', avatar: 'https://fr.seaicons.com/wp-content/uploads/2015/10/Sex-Male-icon.png', level: 'Moyenne section',
        },
        {
          name: 'Caqqqq', firstName: 'Emma', avatar: 'https://fr.seaicons.com/wp-content/uploads/2015/10/Sex-Female-icon.png', level: 'Grande section',
        },
      ],
      items2: [
        { title: 'Travis Howard', avatar: 'https://cdn.vuetifyjs.com/images/lists/5.jpg' },
      ],
    };
  },


  methods: {
    showAlert: () => {
    },
  }

  ,
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
/* h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
} */
<style scoped>
</style>
