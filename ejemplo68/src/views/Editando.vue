<template>
  <div class="container">
    <div v-if="juegoEditar">
      <h2 class="text-center mt-5">Editando la opinión de: {{juegoEditar.juego.name}}</h2>
      <form>
        <div class="mb-3">
          <label for="nombre" class="form-label">Nombre:</label>
          <input type="text" class="form-control" id="nombre" v-model="juegoEditar.nombre">
        </div>
        <div class="mb-3">
          <label for="opiniones" class="form-label">Opiniones</label>
          <textarea class="form-control" id="opiniones" rows="3" v-model="juegoEditar.opinion"></textarea>
        </div>
        <button type="button" class="btn btn-primary" @click="$router.go(-1)">Regresar</button>
        <button type="button" class="btn btn-info mx-4" @click.prevent="guardando">Guardar</button>
      </form>
    </div>
    <div v-else>
      <div class="alert alert-danger mt-5 text-center" role="alert">
        La opinión que deseas editar no existe
        <button type="button" class="btn btn-primary" @click="$router.push({name: 'Administracion'})">Regresar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Editando',
  props: ['id'],
  data() {
    return {
      juegoEditar: null,
    }
  },
  created() {
    let resultado = this.$store.getters.enviandoOpiniones.find(result => result.id === this.id);

    if (resultado !== undefined) {
      this.juegoEditar = resultado; 
    } else {
      this.juegoEditar = null;
    }
  },
  methods: {
    guardando(){
      let juegoEditado = {
        nombre: this.juegoEditar.nombre,
        opinion: this.juegoEditar.opinion,
        juego: this.juegoEditar.juego,
        id: this.juegoEditar.id
      };
      this.$router.push({name: 'Administracion'});
      this.$store.dispatch('guardandoEdicion',juegoEditado);  
    }
  }
}
</script>