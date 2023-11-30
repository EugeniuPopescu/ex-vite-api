<script>

export default {
	name: 'AppCard',
    props: {
        birreria: Object,
    }
}
</script>

<template>
    <div class="">
        <div class="card">
            <h2>Brewery: {{ birreria.name }} </h2>
            <p>Type of Brewery: {{ birreria.brewery_type }} </p>
            <p>City: {{ birreria.city	 }} </p>
            <p>Address: {{ birreria.address_1 }} </p>
        </div>
    </div>
</template>

<style scoped>

</style>
