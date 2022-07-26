<template>
<div style="padding: 5px 15px;">
  <ul class="nav justify-content-end">
  <li class="nav-item">
    <a class="nav-link active" aria-current="page" href="#">Login</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">coupon</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Event</a>
  </li>
</ul>
</div>
  <div class="fw-bold" style="padding: 0px 15px">
    <nav class="navbar navbar-expand-lg navbar-light  ">
  <div class="container-fluid ">
    <a class="navbar-brand fs-1 " href="#">내가 왕</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#" >Home</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            category
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Live</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">My</a>
        </li>
      </ul>
      <form class="d-flex" >
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search" >
        <button class="btn btn-outline-success" type="submit"  >Search</button>
      </form>
    </div>
  </div>
</nav>
  </div>
</template>

<script>
export default {
    name : 'Navbar',
}
</script>

<style>

.navbar{
  position:relative;bottom:10px;
}
.navbar-expand-lg .navbar-nav .nav-link {
    padding-right: 100px;
    padding-left:  0px;
}


.navbar-brand {
    padding-bottom: 20px;
    margin-right: 100px;
    margin-left: 30px;
}

.form-control {
  border-radius: 15px;
}
.btn-outline-success {
    color: #000;
    border-color: #000;
}
.btn-outline-success:hover {
    color: #fff;
    background-color: green;
    border-color: green;
}
</style>