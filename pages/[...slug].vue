<script setup>
    
    const route = useRoute()
    const slug = ref('')

    if(route.params.slug) {
        let lastIndex = route.params.slug.length - 1
        
        if(!route.params.slug[lastIndex]) {
            slug.value = route.params.slug[lastIndex - 1]
        } else {
            slug.value = route.params.slug[lastIndex]
        }
    } else {
        slug.value = 'produtos'
    }

    const { data, pending, error, refresh } = await useFetch('http://teste.com.pt/bliss-market/wp-json/wp/v2/pages', {
        query: { slug: slug.value }
    })

</script>
<template>
    <div>
        <NavBar />
        <br>
        <hr>
        <br>
        <!-- {{ data }} -->
        {{ data[0].title.rendered }}
        <br>
        {{ data[0].content.rendered }}
        <br><br>
        <hr>
        <br>
        <CarHero />
    </div>
</template>
