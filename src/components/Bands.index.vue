<template>
    <div id="bands">
        <div v-for="band in bands" class="band">
            <h3>{{ band.name }}</h3>
            <p>Description: {{ band.description }}</p>
            <p>Origin: {{ band.origin }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Band',
        data () {
            return {
                bands: []
            }
        },

        created () {
            this.$http.get('http://localhost:8000/getAll').then(function(data) {
                this.bands = data.body
            })
        }
    }
</script>

<style>
    .band {
        width: 40%;
        background: lightgray;
        margin: auto;
        padding: 15px;
        border-radius: 10px;
    }
</style>