<template>
    <div>
        <input v-model="userId" type="text">
        <button @click="onLoadUser">Load User</button>
        <nuxt-child />
    </div>
</template>
<script>
export default {
    data(){
        return {
            userId: ''
        }
    },
    methods: {
        onLoadUser(){
            this.$router.push(`/users/${this.userId}`)
        }
    }
}
</script>