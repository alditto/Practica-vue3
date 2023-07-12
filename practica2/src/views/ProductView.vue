<template>
    <div>
      <h5>Producto</h5>
      <tabs>
        <template v-slot:lista>
            <table class="highlight responsive-table card">
                <thead>
                    <tr>
                        <th>Imagen</th>
                        <th>Nombre</th>
                        <th>Descripcion</th>
                        <th>Precio</th>
                        <th>Colores</th>
                    </tr>
                </thead>

                <tbody>
                    <tr v-for="producto in Productos">
                        <td><img :src="producto.imagen" width="150" height="150" align="left" v-bind:alt="producto.nombre"></td>
                        <td>{{ producto.nombre }}</td>
                        <td>{{ producto.descripcion}}</td>
                        <td>{{ producto.precio}}</td>
                        <tr v-for="item in producto.colores">
                            <p>
                                <label>
                                  <input type="checkbox" />
                                  <span>{{ item.colores}}{{item}}</span>
                                </label>
                              </p>
                        </tr>
                        <a class="btn waves-effect waves-light red lighten-2" >Comprar</a>  
                    </tr>
                </tbody>
            </table>
        </template>
        <template v-slot:nuevo>Contenido nuevo</template>
      </tabs>
    </div>
  </template>
  <script>
  import Tabs from '@/components/Tabs.vue'
  export default{
    name: 'Product',
    data(){
      const api=process.env.VUE_APP_API;
      return{
        api,
        Productos:[]
      }
    },
    methods:{
        getProductos(){
            this.axios({
                method:'get',
                url: this.api +'/Productos'
            })
            .then((response) => {
                    this.Productos = response.data;
                    console.log(response);
                })
                .catch((error) => { console.log(error) })
                .finally(() => { });
        }
    },
    mounted(){
            this.getProductos();
    },
    components:{
        Tabs
    }
    
  }
  </script>
<Style>
</Style>