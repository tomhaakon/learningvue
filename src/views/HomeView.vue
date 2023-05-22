<template>
  <div>
    <p>{{ test }}</p>
    <p v-if="isLoggedin == true">heihei</p>
    <v-textarea v-model="test"></v-textarea>
    <v-row>
      <v-col
        cols="4"
        v-for="(person, personIndex) in people"
        :key="personIndex"
      >
        <v-card class="pa-5 ma-5" v-if="person.age > 28">
          <p>{{ person.name }}</p>
        </v-card>
      </v-col>
      <v-col cols="12" xl="2" lg="2" md="2" sm="12" xs="12">
        <p>Hei</p>
      </v-col>
      <v-col cols="6" v-if="$vuetify.breakpoint.mdAndDown">
        <p>Hei</p>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import HelloWorld from "../components/HelloWorld";

export default {
  name: "Home",

  components: {
    HelloWorld,
  },

  data() {
    return {
      test: "",
      isLoggedin: false,
      people: [
        {
          name: "bob",
          age: 29,
        },
        {
          name: "per",
          age: 99,
        },
      ],
    };
  },
};
</script>
