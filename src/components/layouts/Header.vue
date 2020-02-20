<template>
    <div>    
        <v-app-bar absolute color="white" elevate-on-scroll scroll-target="#scrolling-techniques-7" flat>
          <v-container>
            <v-row>
              <v-toolbar-title>Instant</v-toolbar-title>
                <v-spacer></v-spacer>

                <v-btn @click.stop="dialog = true" icon>
                    <v-icon>mdi-lightbulb-on-outline</v-icon>
                </v-btn>

                <v-btn color="mainColor" class="mx-4">
                    <v-icon>mdi-cube-send</v-icon>
                </v-btn>
            </v-row>
          </v-container>
        </v-app-bar>
        
        <v-dialog v-model="dialog" max-width="600" id="org_border">
          <v-row justify="center">
            <v-card id="main">
                <v-container>
                    <v-img src="@/assets/content/our_solution.png">
                    </v-img>
                    <v-card-text>
                    By Instant you would be able to share and transfer your Data between the mobile phones or between the browsers.
                    All Data will be deleted after few minutes and it won't recover.
                    you Do Not need registration, use Instant instantly.
                    </v-card-text>

                    <v-card-actions>
                    <v-spacer></v-spacer>

                    <v-btn color="mainColor" class="mx-4" @click="dialog = false">
                        <v-icon>mdi-export</v-icon>
                    </v-btn>
                    </v-card-actions>
                </v-container>
            </v-card>
          </v-row>
        </v-dialog>
    </div>
</template>
<script>
  export default {
    data () {
      return {
        dialog: false,
      }
    },
  }
</script>
<style>
    #org_border{
        border-radius: 5px;
        overflow: hidden;
    }
</style>