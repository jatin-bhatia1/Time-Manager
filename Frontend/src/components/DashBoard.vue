<template>
  <div>
    <div class="jumbotron jumbotron-fluid" id="main">
      <h1>Welcome to your DashBoard!</h1>

      <div class="container">
        <div class="loggedin" v-if="this.$store.getters.getIsAuthenticated">
          <h4>You're signed in!</h4>
          <ChartManager />
        </div>
        <div class="loggedout" v-else>
          <h4>Please Login yourself!</h4>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ChartManager from "./ChartManager.vue";

export default {
  data() {
    return {
      UserId: this.$store.getters.getUserId,
    };
  },
  async mounted() {
    console.log(this.$store.getters.getRoleLevel);
  },
  computed: {},
  methods: {},
  components: {
    //User,
    ChartManager,
  },
};
</script>