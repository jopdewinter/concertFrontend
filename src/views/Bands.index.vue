<template>
    <div class="list">
        <h1>Bands:</h1>
        <Bands></Bands>
    </div>
</template>

<script>
    import Bands from '@/components/Bands.index.vue'
    export default  {
        name: 'index',
        components: {
            Bands
        }
    }
</script>