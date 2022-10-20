<script setup>
const { data: pokemon } = await useFetch('https://pokeapi.co/api/v2/pokemon/ditto')
</script>
<template>
  <div>

    <Head>
      <Title>{{ pokemon.name }}</Title>
      <Meta name="description" :content="pokemon.name" />
      <Meta property="og:title" :content="pokemon.name" />
      <Meta property="og:image" :content="pokemon.sprites.front_default" />
    </Head>

    {{ pokemon.name }}
    <div>
      <img :src="pokemon.sprites.front_default" alt="">
    </div>
  </div>
</template>