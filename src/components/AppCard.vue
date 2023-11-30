<script>

export default {
	name: 'AppCard',
    props: {
        birreria: Object,
    }
}
</script>

<template>
    <div class="card my-3">
        <div class="card-body">
            <h2 class="text-center"> {{ birreria.name }} </h2>
            <p>Type of Brewery: {{ birreria.brewery_type }} </p>
            <p>State: {{ birreria.state	 }} </p>
            <p>Country: {{ birreria.country	 }} </p>
            <p>City: {{ birreria.city	 }} </p>
            <p>Address: {{ birreria.address_1 }} </p>
        </div>
    </div>
</template>

<style scoped>
.card {
    width: 18%;
}
</style>
