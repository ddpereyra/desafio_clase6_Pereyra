<template>
  <div>
    Maximo {{limite}} items
    <div>
        Nombre: <input id='itName' type="text" v-model="nombre" />
        Rating: <input type="text" id='itRating' v-model="rating" />
        <button @click="AgregarItem(listado, nombre, rating)">Agregar</button> 
    </div>
    <br />
    <table :style="tblstyle" style='width: 320px' >
        <thead>
            <th style='width: 150px'>Nombre</th>
            <th style='width: 50px'>Ingreso</th>
            <th style='width: 50px'>Rating</th>
        </thead>
        <tbody>
            <tr v-for="item in listado" :key="item.id" style='text-align: center;'>
                <td style="display:none;">{{ item.id }}</td>
                <td :class="{'limite':(item.id>limite)}" style='width: 150px; text-align: left'>{{ item.nombre }}</td>
                <td :class="{'limite':(item.id>limite)}" style='width: 50px'>{{ item.fecha }}</td>
                <td :class="{'limite':(item.id>limite)}" style='width: 50px'>{{ item.rating }}</td>
            </tr>
        </tbody>
    </table>
    <hr />
  </div>
</template>

<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.10.6/moment.js"></script>
<script>
/* eslint-disabled */
export default {
  name: 'FormularioRegistro',
  props: {
    nombre: String,
    rating: String,
    limite: Number,
    listado: Array
  },
  methods: {
      AgregarItem(listado, name, rating){
          if(name!='' && name!=undefined && rating!='' && rating!=undefined){
              const fecha = moment(String(new Date())).format('MM/DD/YYYY')
              listado.push({id:listado.length+1, nombre: name, fecha: fecha, rating: rating})
          }
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.limite { 
    background-color: red;
    color:white;
}
</style>
