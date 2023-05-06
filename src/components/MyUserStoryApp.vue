<script setup >
import {ref, reactive, onMounted} from "vue";

const items = (['abc','123']);

// You will need some datamodel that you can bind to your form

// you will need some button add and save events

onMounted(()=>{
  console.log("OnMounted");
});
</script>

<template>
  <v-main class="bg-grey-lighten-3">
    <v-container>
      <v-row>
        <v-col cols="2">
          <v-sheet rounded="lg">
            <h4>This is optional, could be your select list</h4>
            <v-list rounded="lg">
              <v-list-item
                v-for="n in 5"
                :key="n"
                items
              >
                <v-list-item-title>
                  List Item {{ n }}
                </v-list-item-title>
              </v-list-item>

              <v-divider class="my-2"></v-divider>

              <v-list-item
                link
                color="grey-lighten-4"
              >
                <v-list-item-title>
                  Refresh
                </v-list-item-title>
              </v-list-item>
            </v-list>
          </v-sheet>
        </v-col>

        <v-col>
          <v-sheet
            min-height="70vh"
            rounded="lg"
          >
            <!--  -->
            <v-form>
              <h3>Your User Story Form Goes Here </h3>

            </v-form>
          </v-sheet>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<style scoped>

</style>
