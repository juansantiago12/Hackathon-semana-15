<template>
   <div class="container mb-4 mt-4 bg-secondary bg-gradient">
      <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
         <div class="carousel-inner">
            <div class="carousel-item active d-flex justify-content-center">
               <img
                  src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=702&q=80"
                  class="d-block w-80"
                  alt="..."
               />
            </div>
            <div class="carousel-item d-flex justify-content-center">
               <img
                  src="https://images.unsplash.com/photo-1532618793091-ec5fe9635fbd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
                  class="d-block w-80"
                  alt="..."
               />
            </div>
            <div class="carousel-item d-flex justify-content-center">
               <img
                  src="https://images.unsplash.com/photo-1532619187608-e5375cab36aa?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
                  class="d-block w-80"
                  alt="..."
               />
            </div>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: 'HelloWorld',
   props: {
      msg: String,
   },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
   margin: 40px 0 0;
}
ul {
   list-style-type: none;
   padding: 0;
}
li {
   display: inline-block;
   margin: 0 10px;
}
a {
   color: #42b983;
}
</style>
