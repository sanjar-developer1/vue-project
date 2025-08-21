<template>
    <div>
        <h1>Child component</h1>
        <GrandChildComponent />
    </div>
</template>
<script>
import GrandChildComponent from './GrandChildComponent.vue'
export default {
    components: { GrandChildComponent },
}
</script>
<style></style>