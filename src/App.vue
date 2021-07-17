<template>
   <nav class="navbar navbar-expand-sm navbar-dark bg-primary">
      <div class="container">
         <a class="navbar-brand" href="#"
            ><img src="./assets/logo.png" alt="" class="navbar-brand-img"
         /></a>
         <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarScroll"
            aria-controls="navbarScroll"
            aria-expanded="false"
            aria-label="Toggle navigation"
         >
            <span class="navbar-toggler-icon"></span>
         </button>
         <div class="collapse navbar-collapse" id="navbarScroll">
            <ul
               class="navbar-nav me-auto my-2 my-lg-0 navbar-nav-scroll"
               style="--bs-scroll-height: 100px;"
            >
               <li class="nav-item">
                  <!-- <a class="nav-link active" aria-current="page" href="#">Home</a> -->
                  <router-link to="/" class="nav-link active" aria-current="page">Home</router-link>
               </li>
               <li class="nav-item">
                  <!-- <a class="nav-link active" aria-current="page" href="#">Contact</a> -->
                  <router-link to="/contacts" class="nav-link active" aria-current="page"
                     >Contacts</router-link
                  >
               </li>
            </ul>
            <form class="d-flex">
               <input
                  class="form-control me-2"
                  type="search"
                  placeholder="Search"
                  aria-label="Search"
               />
               <button class="btn btn-outline-success" type="submit">Search</button>
            </form>
         </div>
      </div>
   </nav>
   <router-view />
</template>

<style>
.navbar-brand-img {
   width: 50px;
}
</style>
