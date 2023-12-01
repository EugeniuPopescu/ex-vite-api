<script>
import AppCard from './AppCard.vue'
import axios from 'axios'
import { store } from "../store.js"

export default {
	name: 'AppContent',
    components: {
        AppCard
    },
	data() {
        return {
            store,
        }
    },
    mounted() {
        this.getBreweries();
    },
    methods: {
        getBreweries() {
            axios.get(this.store.apiUrl).then(risultato => {
                this.store.breweries = risultato.data;
                console.log(risultato.data);
			});
        }
    },
}
</script>

<template>
    <div class="bg-dark-subtle">
        <div class="container d-flex flex-wrap justify-content-between">
            <AppCard v-for="brewery in store.breweries"  :birreria="brewery" />
        </div>
    </div>
</template>

<style scoped>

</style>