<template>
  <div class="container">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import { mapActions } from "vuex";

import Header from "./components/Header";

export default {
  name: "App",
  components: {
    Header,
  },
  methods: {
    ...mapActions(["setPagesAction"]),
  },
  async created() {
    this.setPagesAction();
  },
};
</script>

