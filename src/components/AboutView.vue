<script setup>
import { computed } from 'vue'
import { useRoute, useRouter } from 'vue-router'

const router = useRouter()
const route = useRoute()

const search = computed({
    get() {
        return route.query.search ?? ''
    },
    set(search) {
        router.replace({ query: { search } })
    },
})
</script>

<template>
    <div>
        <h1>About View</h1>
        <p>
            This is the about view. You can use the input below to set a query
            parameter in the URL.
        </p>
        <input v-model="search" placeholder="Type to set 'search' query param" />
        <p>
            Current 'search' query parameter: <strong>{{ search }}</strong>
        </p>
    </div>
</template>