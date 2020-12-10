<template>
      <v-img
        height="100vh"
        style="background-color: rgba(0,0,0,0.5)"
        src="https://i.imgur.com/V5IyNcF.gif"
      >
        <v-layout 
        row
        >
          <v-container>

            <v-row style="height: 80vh;" class="fill-height" justify="center" align="center">
              <v-col style="padding-top: 200px !important;" cols="12">
                <CountDown />
              </v-col>
              <v-col style="margin-top: -200px !important;" cols="12">
                <v-row justify="center">
                  <v-dialog
                    v-model="dialog1"
                    max-width="600px"
                  >
                    <template v-slot:activator="{ on, attrs }" class="text-xs-center">
                      <v-btn
                        color="primary"
                        dark
                        v-bind="attrs"
                        v-on="on"
                      >
                      Register Now
                      </v-btn>
                    </template>
                    <v-card>
                      <v-card-title>
                        <span class="headline">Fill this to register</span>
                      </v-card-title>
                      <v-card-text>
                        <v-container>
                          <v-row>
                            <v-col
                              cols="12"
                              sm="6"
                            >
                              <v-text-field
                                label="first name*"
                                required
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col
                              cols="12"
                              sm="6"
                            
                            >
                              <v-text-field
                                label="last name*"
                                required
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col cols="12">
                              <v-text-field
                                label="Email*"
                                type="email"
                                placeholder="e.g myname@example.com"
                                required
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col cols="12">
                              <v-text-field
                                label="Telephone*"
                                type="tel"
                                placeholder="+237 671234567"
                                required
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col
                              cols="12"
                              
                            >
                              <v-select
                                :items="['9-17', '18-29', '30-54', '54+']"
                                label="Age*"
                                required
                                outlined
                              ></v-select>
                            </v-col>
                            <v-col
                              cols="12"
                              
                            >
                              <v-text-field
                                label="Any Expectation?"
                                type="text"
                                outlined
                              ></v-text-field>
                            </v-col>
                          </v-row>
                        </v-container>
                        <small>*indicates required field</small>
                      </v-card-text>
                      <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn
                          color="purple darken-1"
                          text
                          @click="dialog1 = false"
                        >
                          Save
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                  </v-dialog>
                </v-row>
              </v-col>
            
          </v-row> 
          </v-container>
        </v-layout>
       <Events />
      </v-img>
</template>

<script>
import CountDown from './CountDown'
import Events from './Events'
  export default {
    name: 'Main',
    components:{
      CountDown,
      Events,
    },

    data: () => ({
      dialog1: false,
    }),
  }
</script>
