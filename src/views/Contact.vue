<template>
   <div class="container">
      <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
         <div class="carousel-inner">
            <div class="carousel-item active">
               <img
                  src="https://images.unsplash.com/photo-1587620962725-abab7fe55159?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=889&q=80"
                  class="d-block w-100"
                  alt="img1"
               />
            </div>
            <div class="carousel-item">
               <img
                  src="https://images.unsplash.com/photo-1603468620905-8de7d86b781e?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=755&q=80"
                  class="d-block w-100"
                  alt="img2"
               />
            </div>
            <div class="carousel-item">
               <img
                  src="https://images.unsplash.com/photo-1603575448360-153f093fd0b2?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
                  class="d-block w-100"
                  alt="img3"
               />
            </div>
         </div>
      </div>
   </div>
   <div class="container mt-4 mb-4">
      <h1 class="text-center text-primary">Tabla de Contenido</h1>
      <table class="table table-striped">
         <thead>
            <tr>
               <th>#</th>
               <th>Nombre</th>
               <th>Username</th>
               <th>website</th>
               <th>phone</th>
               <!-- <th>Company</th> -->
            </tr>
         </thead>
         <tbody>
            <tr>
               <th>{{ $route.params.id }}</th>
               <td>{{ persona.name }}</td>
               <td>{{ persona.username }}</td>
               <td>{{ persona.website }}</td>
               <td>{{ persona.phone }}</td>
               <!-- <td>{{ persona.company.name }}</td> -->
            </tr>
         </tbody>
      </table>
   </div>
   <!-- <h1>Usuario - {{ $route.params.id }}</h1>
   <h2>Nombre: {{ persona.name }}</h2>
   <h2>Telefono: {{ persona.phone }}</h2>
   <h2>Website: {{ persona.website }}</h2> -->
</template>

<script>
export default {
   data() {
      return {
         persona: [],
      };
   },

   methods: {
      async getUser() {
         //  const user = 'this.$route.params.id';
         const response = await fetch(`http://localhost:3000/users/${this.$route.params.id}`);
         const data = await response.json();
         this.persona = data;
      },
   },

   created() {
      this.getUser();
   },
};
</script>

<style></style>
