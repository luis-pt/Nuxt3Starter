<script setup>
    const { data, pending, error, refresh } = await useFetch('http://teste.com.pt/bliss-market/wp-json/wp/v2/posts', {
        query: { slug: 'ux-pie' }
    })
    const route = useRoute()
</script>
<template>
    <div>
        <NavBar />
        <br>
        <hr>
        <br>
        <!-- {{ data }} -->
        {{ route }}
        <br><br>
        <hr>
        <br>
        <CarHero />
    </div>
</template>
