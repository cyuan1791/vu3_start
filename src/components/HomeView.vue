<script>
export default {
    methods: {
        goToAbout() {
            this.$router.push('/about')
        },
    },
}
</script>
<template>
    <div>
        <h1>Home View</h1>
        <p>Welcome to the home view of this Vue 3 application.</p>
        <button @click="goToAbout">Go to About View</button>
    </div>
</template>