<template>
  <div class="text-center m-2 flex flex-col max-w-[230px] shadow-md p-2 hover:shadow-[0px_0px_1px_#000]"
  >
    <router-link :to="{
      name: 'MovieDetails', params: {
        id: movie.imdbID
      }
    }">
      <div class="min-h-[120px] grid place-content-center">
        <p>{{ movie.Title }}</p>
        <p>{{ movie.Year }}</p>
      </div>
      <img :src="movie.Poster" class=" mx-auto block w-[230px] h-[330px]" alt="movie poster" >
    </router-link>
  </div>
</template>

<script setup>
const props = defineProps({
  movie: Object,
  loading:Boolean
})

</script>
