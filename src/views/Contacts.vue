<template>
   <div class="container">
      <h1 class="text-center text-primary">Componente de contactos</h1>
   </div>
   <div class="container">
      <div class="row">
         <div
            v-for="(user, index) in users"
            :key="index"
            class="col-6 col-sm-6 col-md-4 col-lg-3 mb-3"
         >
            <article class="card border border-primary border-1">
               <img :src="user.image" class="card-img-top" />
               <div class="card-body">
                  <h5 class="card-title fs-6 text-primary">{{ user.name }}</h5>
                  <h5 class="card-title h6 text-success">{{ user.email }}</h5>
                  <p class="card-text">
                     Some quick example text to build on the card title and make up the bulk
                  </p>
                  <!-- <a href="#" class="btn btn-primary">About me</a> -->
                  <router-link :to="`/contacts/${user.id}`" class="btn btn-primary"
                     >About me</router-link
                  >
               </div>
            </article>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   data() {
      return {
         users: [],
      };
   },

   methods: {
      async getUsers() {
         const response = await fetch('http://localhost:3000/users');
         const data = await response.json();
         this.users = data;
      },
   },

   created() {
      this.getUsers();
   },
};
</script>

<style></style>
