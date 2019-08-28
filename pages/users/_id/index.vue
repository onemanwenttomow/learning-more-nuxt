<template>
    <h1>A singer user, with ID: {{ $route.params.id }}</h1>
</template>

<script>
export default {
    validate(data) {
        console.log(data);
        // return /^\d+$/.test(data.params.id)
        return !isNaN(data.params.id);
    },
    layout: "users"
}

</script>
