<template>
    <div>
        <h1>Grand Child Component</h1>
        <p>Username: {{ username }}</p>
        <p>Age: {{ age }}</p>
    </div>
</template>
<script>

export default {
    name: "GrandChildComponent",
    inject: ["username", "age"]
}
</script>
<style></style>