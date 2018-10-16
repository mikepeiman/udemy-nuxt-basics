<template>
  <!-- // this component name same as  -->
  <div>
    <h1>This is the users.vue component</h1>
    <div>
      <input type="text" v-model="user_id">
      <button @click="onLoadUser">Load user</button>
      <p>Below is the nuxt-child component</p>
      <nuxt-child />
    </div>
</div>
</template>

<script>
export default {
  data() {
    return {
      user_id: null
    }
  },
  methods: {
    onLoadUser() {
      this.$router.push('/users/' + this.user_id)
    }
  }
}
</script>