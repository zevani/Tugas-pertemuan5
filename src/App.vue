<template>
  <div id="app">
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <a class="navbar-brand" href="#">Azila Store</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Products</a>
          </li>
        </ul>
      </div>
    </nav>

    <!-- Carousel -->
    <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <div class="carousel-caption d-none d-md-block">
            <h5>soft cookies dough</h5>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h5>melted chocolate inside</h5>
          </div>
        </div>
        <div class="carousel-item">
          <div class="carousel-caption d-none d-md-block">
            <h5>flavor variants</h5>
          </div>
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

    <!-- Cards Section -->
    <div class="container mt-5">
      <div class="row">
        <div class="col-md-4" v-for="product in products" :key="product.id">
          <div class="card">
            <img class="card-img-top" :src="product.image" alt="Product image">
            <div class="card-body">
              <h5 class="card-title">{{ product.name }}</h5>
              <p class="card-text">{{ product.description }}</p>
              <a href="#" class="btn btn-primary">Beli Sekarang</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer -->
    <footer class="bg-dark text-center text-lg-start mt-5 text-white">
      <div class="container p-4">
        <div class="row">
          <div class="col-lg-6 col-md-12 mb-4 mb-md-0">
            <h5 class="text-uppercase">MadebyMood.co</h5>
            <p>
              ARTISANAL COOKIES
            </p>
          </div>
          <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">Links</h5>
            <ul class="list-unstyled mb-0">
              <li>
                <a href="#!" class="text-white">Home</a>
              </li>
              <li>
                <a href="#!" class="text-white">Products</a>
              </li>
            </ul>
          </div>
          <div class="col-lg-3 col-md-6 mb-4 mb-md-0">
            <h5 class="text-uppercase">Kontak Kami</h5>
            <ul class="list-unstyled mb-0">
              <li>
                <a href="mailto:info@tokoonline.com" class="text-white">sy.zevanianandazellery@gmail.com</a>
              </li>
              <li>
                <a href="tel:+62123458899" class="text-white">223510698</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="text-center p-3 bg-secondary">
        © 2024 Azila Store. All rights reserved.
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { 
          id: 1, 
          name: 'Hijab Premium', 
          description: 'Hijab premium anti gerah & nerawang.', 
          image: 'https://snapy.co.id/gambar/artikel/kerudung-ukuran-pashmina.jpg'

        },
        { 
          id: 2, 
          name: 'Gamis satin', 
          description: 'Anti kusut dan anti gerah.', 
          image: 'https://image.popbela.com/content-images/post/20221031/4b11e6193b8e9012dc2f57396bf25a6e.jpg?width=1600&format=webp&w=1600' 
        },
        { 
          id: 3, 
          name: 'Hijab segiempat', 
          description: 'Cocok untuk anak SMA.', 
          image: 'https://www.iprint.id/wp-content/uploads/2023/07/4-cara-memakai-hijab-segi-empat-mudah-dan-tetap-trendi-1024x725.webp' 
        }
      ]
    }
  }
}

</script>

<style>
body {
    font-family: Arial, sans-serif;
}

.navbar-brand {
    font-weight: bold;
    color: #ffffff !important;
}

.nav-link {
    color: #ffffff !important;
}

.carousel-caption h5 {
    background-color: rgba(0, 0, 0, 0.5);
    padding: 10px;
    border-radius: 5px;
    color: #ffffff;
}

.carousel-caption p {
    background-color: rgba(0, 0, 0, 0.5);
    padding: 5px;
    border-radius: 5px;
    color: #ffffff;
}

.card-title {
    color: #007BFF;
}

.card-text {
    color: #343a40;
}

.btn-primary {
    background-color: #007BFF;
    border-color: #007BFF;
}

.footer {
    background-color: #343a40;
    padding: 20px 0;
}

.footer .container p {
    margin-bottom: 0;
}

.footer .list-unstyled li {
    margin-bottom: 10px;
}

.footer .text-center {
    background-color: #212529;
    color: white;
    padding: 10px 0;
}

.footer a {
    color: #ffffff;
}

</style>