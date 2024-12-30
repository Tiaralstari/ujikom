<template>
  <div class="he d-flex justify-content-center m-2" >
    <div class="row" style="width: 25%;">
      <div class="col-2"><img src="../assets/jabar.png" alt=""></div>
      <div class="col-3"><img src="../assets/smk.png" alt="" class="me-3">
      </div>
      <div class="col">
        <h5>SMKN NEGERI 4 </h5>
        <h5>TASIKMALAYA</h5>
      </div>
    </div>


  </div>
  <nav class="navbar navbar-expand-lg navbar-light shadow py-4 d-flex justify-content-center">
    <div class="c">
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
        aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse px-5" id="navbarNavDropdown">
        <ul class="navbar-nav mx-5 pt-2">
          <nuxt-link to="/">
            <li class="nav-item">
              <h6>HOME</h6>
            </li>
          </nuxt-link>
          <li class="nav-item mx-3">
            <nuxt-link to="/profile">
              <h6>PROFILE</h6>
            </nuxt-link>
          </li>
          <li class="nav-item mx-3">
            <nuxt-link to="/eskul">
              <h6>EKSTRAKULIKULER</h6>
            </nuxt-link>
          </li>
          <li class="nav-item mx-3">
            <nuxt-link to="/galeri">
              <h6>GALERI</h6>
            </nuxt-link>
          </li>
          <li class="nav-item mx-3">
            <nuxt-link to="/prestasi">
              <h6>PRESTASI</h6>
            </nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

</template>
<style scoped>
img {
  height: 50px;
  margin-left: 10px;
}

li {
  font-family: sans-serif;
}
*{
  text-decoration: none;
  color: black ;

}
.he{
  background-color: white;
}
.navbar{
  position: sticky;
  top :0;
  background-color: #4870a4;
  z-index: 1;
}
</style>