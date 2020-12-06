<template>
  <div>
    <div class="card text-white bg-dark" style="width: 18rem;">
      <img :src="member.image" class="card-img-top objetfit" alt="perfil" />
      <div class="card-body">
        <h5 class="card-title">{{member.codigo}} - {{member.nombre}}</h5>
        <p class="card-text">
          {{member.descripcion}}
        </p>
        <ul >
            <li class="list">{{member.rol}}</li>
        </ul>
        
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "TeamCard",
        props: ["member"],
        data(){
          return{
            teamemb: null
          }
            
        }
        
    };
</script>

<style scoped>
  .objetfit{
    width: 286px;
    height: 280px;
    object-fit: cover;
  }
  .list{
    list-style: none;
  }
</style>
