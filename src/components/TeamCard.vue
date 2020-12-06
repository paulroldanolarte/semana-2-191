<template>
    <div>
            <div class="card">
               <div class="card text-white bg-info border-dark">
                   <div class="d-flex justify-content-center p-2">
                       <img v-bind:src="member.image" alt="Foto del ProTeam" height="350" width="400">          
                   </div>
                   <div class="card-body">
                       <h5 class="card-text text-center">{{member.codigo}}</h5>
                       <h5 class="card-title">{{member.nombre}}</h5> 
                       <p class="card-text text-justify">{{member.descripcion}}</p>
                       
                      
                       
                   </div>
                   <div class="card-footer">
                       <small class="font-weight-bold text-justify">{{member.rol}}</small>
                   </div>
               </div>
           
    </div>
    </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style scoped>

.card {
    min-height: 730px;
}

</style>
