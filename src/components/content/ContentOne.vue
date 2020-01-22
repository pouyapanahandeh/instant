<template>
    <v-container id="centerize" fluid>
        <v-row justify="center" align="center">
            <v-col cols="1"></v-col>
            <v-col cols="4" align-self="center">
                <v-container fluid>
                    <v-tabs>
                        <v-tab>Send File</v-tab>
                            <v-tab-item>
                                <v-container>
                                    <v-row align="center">
                                        <v-text-field label="Type your message" outlined></v-text-field>
                                    </v-row>
                                    <v-row align="center">

                                    </v-row>
                                    <v-row align="center">
                                        <v-file-input
                                            v-model="files"
                                            color="mainColor"
                                            counter
                                            label="File input"
                                            multiple
                                            placeholder="Select your files"
                                            outlined
                                            :show-size="1000"
                                        >
                                            <template v-slot:selection="{ index, text }">
                                            <v-chip
                                                v-if="index < 2"
                                                color="mainColor"
                                                dark
                                                label
                                                small
                                            >
                                                {{ text }}
                                            </v-chip>

                                            <span
                                                v-else-if="index === 2"
                                                class="overline grey--text text--darken-3 mx-2"
                                            >
                                                +{{ files.length - 2 }} File(s)
                                            </span>
                                            </template>
                                        </v-file-input>
                                    </v-row>
                                    <v-row align="center">
                                        <v-btn color="mainColor" block>
                                            Instant
                                            <v-icon>mdi-cube-send</v-icon>
                                        </v-btn>
                                    </v-row>
                                </v-container>
                            </v-tab-item>
                    <v-tab>Get File</v-tab>
                        <v-tab-item>
                            <v-container>
                                <v-row align="center">
                                    <v-text-field placeholder="Type the file number" outlined></v-text-field>
                                </v-row>
                                <v-row align="center">
                                    <v-btn color="mainColor" block>
                                        Instant
                                        <v-icon>mdi-cube-scan</v-icon>
                                    </v-btn>
                                </v-row>
                            </v-container>
                        </v-tab-item>    
                    </v-tabs>
                </v-container>
            </v-col>
            <v-col cols="2"></v-col>
            <v-col cols="4" align-self="center">
                <v-container>
                    <v-row>
                        <v-col cols="12">
                            <v-container>
                                <v-row align="center">
                                    <v-img src="@/assets/content/content_one.png" alt="car crossing the earth"></v-img>
                                </v-row>
                            </v-container>
                        </v-col>
                    </v-row>
                </v-container>
            </v-col>
            <v-col cols="1"></v-col>
        </v-row>
    </v-container>
</template>
<script>
  export default {
    data: () => ({
      files: [],
    }),
  }
</script>
<style>
    #centerize{
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>