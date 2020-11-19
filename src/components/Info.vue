<template>
    <div>
        <v-btn
        href="#"
        target="_blank"
        text
        flat
         >
        <div class="text-center">
            <v-menu
              open-on-hover
              top
              offset-y
            >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  text
                  color="white"
                  dark
                  v-bind="attrs"
                  v-on="on"
                >
                  {{title}}
                </v-btn>
              </template>
                <v-card
                    class="mx-auto"
                    max-width="344"
                    outlined
                >
                    <v-list-item three-line>
                      <v-list-item-content>
                        <v-list-item-title class="headline mb-1">
                         {{titleMore}}
                        </v-list-item-title>
                        <v-list-item-subtitle>
                          {{completeInfo}}
                        </v-list-item-subtitle>
                      </v-list-item-content>

                      <v-list-item-avatar
                        tile
                        size="80"
                        color="grey"
                      ><img :src="images" alt=""></v-list-item-avatar>
                    </v-list-item>

                    <v-card-actions>
                      <v-btn
                        outlined
                        rounded
                        text
                      >
                        Button
                      </v-btn>
                    </v-card-actions>
              </v-card>
            </v-menu>
        </div>
        </v-btn>
    </div>
</template>
<script>
export default {
    name: "Info",
    props: ['title', 'titleMore', 'completeInfo', 'images'],
    data(){
        return{

        }
    }
  
}
</script>
