<script>
import AppSearch from './AppSearch.vue';
import axios from 'axios'


export default {
	name: 'AppHeader',
    components: {
    AppSearch
    },
	data() {
        return {
        }
    },
    methods: {
        cerca() {
            axios.get(`https://api.openbrewerydb.org/v1/breweries/search?query={${this.store.searchString}}` ).then(risultato => {
                
                this.store.breweries = risultato.data;
            });
        }
    },
    mounted() {}
}
</script>

<template>
    <div class="bg-dark text-light">
        <div class="container ">
            <div class="row d-flex justify-content-between align-items-center">
                <div class="col-6">
                    <h1 class="">Poland's Breweries</h1>
                </div>
                <div class="col-6">
                    <!-- content AppSearch -->
                    <AppSearch @search="cerca" />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
