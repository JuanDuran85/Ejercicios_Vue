<template>
  <div class="content-container">
    <div class="section content-title-group">
      <h2 class="title">Heroes</h2>
      <div class="columns">
        <div class="column is-8" v-if="heroes">
          <ul>
            <li v-for="hero in heroes" :key="hero.id">
              <div class="card">
                <div class="card-content">
                  <div class="content">
                    <div :key="hero.name" class="name">
                      {{ hero.firstName }} {{ hero.lastName }}
                    </div>
                    <div class="description">{{ hero.description }}</div>
                  </div>
                </div>
                <footer class="card-footer">
                  <router-link :to="{name: 'HeroesDetail', params:{id: hero.id}}" class="link card-footer-item" tag="button">
                    <i class="fas fa-check"></i>
                    <span>Select</span>
                  </router-link>
                </footer>
              </div>
            </li>
          </ul>
          <div class="notification is-info" v-show="message">{{ message }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { heroWatchers, lifecycleHooks, data } from '../shared';

export default {
  name: 'Heroes',
  data() {
    return {
      heroes: [],
      message: '',
      capeMessage: '',
    };
  },
  mixins: [lifecycleHooks, heroWatchers],
  async created() {
    await this.loadHeroes();
  },
  methods: {
    async loadHeroes() {
      this.heroes = [];
      this.message = 'getting the heroes, please be patient';
      this.heroes = await data.getHeroes();
      this.message = '';
    },
    saveHero(hero) {
      const index = this.heroes.findIndex(h => h.id === hero.id);
      this.heroes.splice(index, 1, hero);
      this.heroes = [...this.heroes];
    },
  },
};
</script>

<style scoped lang="scss">

</style>
