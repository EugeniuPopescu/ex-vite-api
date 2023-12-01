<script>
import AppSearch from './AppSearch.vue';
import axios from 'axios'
import { store } from "../store.js"



export default {
	name: 'AppHeader',
    components: {
    AppSearch
    },
	data() {
        return {
            store
        }
    },
    methods: {
        cerca() {
            let address = `https://api.openbrewerydb.org/v1/breweries/search?query={${this.store.searchString}}`

            axios.get( address ).then(risultato => {
                
                this.store.breweries = risultato.data;

            }).catch(errore => {
                this.store.breweries = [];
                console.error('IUBIULHNLUINLIUNLIUJ');
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
