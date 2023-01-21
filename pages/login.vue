<template>
  <div>
    <v-container>
      <h1>Welcome <span v-if="currentUser">{{ currentUser.displayName }}</span></h1>

      <v-card elevation="2" class="pa-5">
        <SignIn />
      </v-card>
    </v-container>
  </div>
</template>
<script>
export default {
  computed: {
    currentUser() {
      return this.$store.state.user;
    }
  }
}
</script>