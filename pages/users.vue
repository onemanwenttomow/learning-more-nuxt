<template>
    <div class="">
        <h1>My users component</h1>
        <nuxt-child />
        <input type="text" v-model="userId">
        <button @click="loadUser">Load User</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            userId: ''
        }
    },
    methods: {
        loadUser() {
            this.$router.push(`/users/${this.userId}`)
        }
    },
    layout: "users"
}
</script>
