<template>
  <div id="app" class="container">
    <h1 class="text-center">Tabla de Usuarios</h1>
        <table class="table table-striped">
            <thead>
              <tr>
                <th>#</th>
                <th>Nombre</th>
                <th>Apellido</th>
                <th>RUN</th>
                <th>Nacimiento</th>
                <th>Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <th>1</th>
                <td>{{personas[0].nombre}}</td>
                <td>{{personas[0].apellido}}</td>
                <td>{{personas[0].RUN}}</td>
                <td>{{personas[0].fecha}}</td>
                <td>{{personas[0].edad}}</td>
              </tr>
              <tr>
                <th>2</th>
                <td>{{personas[1].nombre}}</td>
                <td>{{personas[1].apellido}}</td>
                <td>{{personas[1].RUN}}</td>
                <td>{{personas[1].fecha}}</td>
                <td>{{personas[1].edad}}</td>
              </tr>
              <tr>
                <th>3</th>
                <td>{{personas[2].nombre}}</td>
                <td>{{personas[2].apellido}}</td>
                <td>{{personas[2].RUN}}</td>
                <td>{{personas[2].fecha}}</td>
                <td>{{personas[2].edad}}</td>
              </tr>
            </tbody>
          </table>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      personas: [
          {nombre:"Jose",apellido:"Pérez",RUN:"123456-2",fecha:"12-04-67",edad:"52"},
          {nombre:"María",apellido:"Rodríguez",RUN:"654321-1",fecha:"30-11-90",edad:"29"},
          {nombre:"Manuel",apellido:"Patiño",RUN:"14223456-6",fecha:"02-12-59",edad:"60"}
      ]
    }
  },
}
</script>