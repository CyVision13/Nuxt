<template>
    <div>
        <!-- <Header /> -->
        <input v-model="userId" type="text">
        <button @click="onLoadUser">Load User</button>
        <nuxt-child />
    </div>
</template>
<script>
import Header from '~/components/Header.vue'
export default {
    components: {
    Header
  },
    data(){
        return {
            userId: ''
        }
    },
    methods: {
        onLoadUser(){
            this.$router.push(`/users/${this.userId}`)
        }
    },
    layout: 'users'
}
</script>