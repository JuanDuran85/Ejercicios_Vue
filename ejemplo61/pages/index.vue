<template>
  <div class="container">
    <div class="tile is-parent">
        <article class="tile is-child notification is-info">
          <p class="title">Ejemplo con NuxtJS y VueJS</p>
          <p class="subtitle">Información de Albums</p>
        </article>
    </div>
    <div class="columns is-multiline">
        <albums-card v-for="(item,index) in albums" :key="index" :album="item"></albums-card>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import env from '../config/env';
import albumsCard from '../components/AlbumsCard.vue';

export default {
    name: 'Index',
    data() {
        return {
            albums: [],
        }
    },
    created() {
        axios.get(`${env.apiUrl}/albums`).then(response=>{
            this.albums = response.data;
        })
    },
    components: {
        albumsCard
    }
}
</script>

<style scoped>

</style>