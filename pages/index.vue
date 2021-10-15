<template>
<div>
  <section>
    <nav class="navbar navbar-expand-lg navbar-light fixed-top bg-light">
      <b-img src="logo.jpg" class="logo"></b-img>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Pricing</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Disabled</a>
          </li>
        </ul>
      </div>
    </nav>
  </section>

  <section>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      fade
      controls
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide img-src="1.jpg"></b-carousel-slide>
      <b-carousel-slide img-src="2.jpg"></b-carousel-slide>
      <b-carousel-slide img-src="3.jpg"></b-carousel-slide>
    </b-carousel>
  </section>

  <section>
    <b-media class="media-cafebatu">
    <template #aside>
      <b-img src="4.jpg" class="cafebatu-logo"></b-img>
    </template>
    <p class="cafebatu-title">Cafe Batu</p>
    <p class="cafebatu-note">
      Cafe batu menyediakan kopi terbaik di Indonesia dengan 30+ varian rasa. Biji Kopi terbaik dari seluruh dunia kami sediakan
    </p>
    </b-media>
  </section>

  <section class="product">
    <p>Our Best Product</p>
  </section>

  <section>
    <b-container>
      <b-row>
        <b-col>
          <b-img fluid src="10.jpg" alt="Image 1"></b-img>
        </b-col>
        <b-col>
          <b-img fluid src="9.jpg" alt="Image 2"></b-img>
        </b-col>
        <b-col>
          <b-img fluid src="7.jpg" alt="Image 1"></b-img>
        </b-col>
      </b-row>
        <b-row>
        <b-col>
          <b-img  fluid src="8.jpg" alt="Image 1"></b-img>
        </b-col>
        <b-col>
          <b-img  fluid src="4.jpg" alt="Image 2"></b-img>
        </b-col>
        <b-col>
          <b-img  fluid src="3.jpg" alt="Image 2"></b-img>
        </b-col>
      </b-row>
    </b-container>
  </section>
  
  <section class="socialmedia">
    <p class="socialmedia-follow">Follow our Media Social</p>
    <div class="container">
    <div class="container-socialmedia ">
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
      <div class="row">
        <div class="twitter">
          <a href="#" class="fa fa-twitter">  </a><p class="socialmedia-name">CafeBatu</p>
        </div>
        <div class="instagram">
          <a href="#" class="fa fa-instagram">  </a>   <p class="socialmedia-name">CafeBatu</p>
        </div>
        <div class="envelope">
          <a href="#" class="fa fa-envelope">  </a>  <p class="socialmedia-name">cafebatu@gmail.com</p>
        </div>
      </div>
    </div>
    </div>
  </section>
  
  <section>
    <footer class="footer1">
        <div class="container text-center">
          <div class="row">

            <div class="cabang">
              <h6 class="text-uppercase fw-bold mb-4">Cabang</h6>
              <p class="kota"> Kota Batu </p>
              <p class="alamat"> Jalan Kilimanjaro no 25, Batu</p>
              <p class="kota"> Kota Malang </p>
              <p class="alamat"> Jalan Soekarno Hatta no 1000, Malang </p>
            </div>

            <div class="produk">
              <h6 class="text-uppercase fw-bold mb-4">Produk</h6>
              <p>Kopi A</p>
              <p>Kopi B</p>
              <p>Kopi C</p>
              <p>Kopi D</p>
            </div>

            <div class="medsos">
              <h6 class="text-uppercase fw-bold mb-4"> Useful links </h6>
              <p>Pricing</p>
              <p>Settings </p>
              <p>Orders</p>
              <p>Help</p>
            </div>
        </div>
      </div>

      <section class="copyright">
        © 2021 Copyright: <a class="text-reset fw-bold">CafeBatu</a>
      </section>
    </footer>
  </section>
  
  </div>
</template>

<script>
export default {
    data() {
      return {
        slide: 0,
        sliding: null,
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
  }
</script>

<style>
  .caraousel{
  margin: auto;
  }
  .logo{
    height: 70px;
    width: 70px;
  }
  .media-cafebatu{
    text-align: center;
    background: grey;
    width: 60%;
    margin : 5% auto 5% auto ;
  }
  .cafebatu-logo{
    width: max-content;
    height: max-content;
  }
  .cafebatu-title{
    font-size: xx-large;
    color: white;
  }
  .cafebatu-note{
    text-align: left;
    font-family: 'Courier New', Courier, monospace;
    font-size: xx-large;
    color: white;
  }
  .product{
    text-align: center;
    font-size : xx-large;
    color: black;
  }
  .socialmedia{
    max-width: 100%;
    background: grey;
  }
  .socialmedia-follow{
    text-align: center;
    margin : 5% auto 1% auto ;
    font-size: xx-large;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  }
  .container-socialmedia{
    font-size: 75px;
    text-align: center;
  }
  .fa {
  padding: 5%;
}
.fa:hover {
  opacity: 0.7;
}
.twitter{
  width: 18%;
  height: 18%;
  margin: auto;
}
.fa-twitter {
  background: #55ACEE;
  color: white;
}
.instagram{
  width: 18%;
  height: 18%;
  margin: auto;
}
.fa-instagram{
  background: pink;
  color: white;
}
.envelope{
  width: 18%;
  height: 18%;
  margin: auto;
}
.fa-envelope{
  background: black;
  color: white;
}
.socialmedia-name{
  text-align: center;
  font-size: xx-large;
}
  .footer1{
    background : black;
    color: white;
    padding-top: 2%;
  }
  .cabang{
    margin: auto;
  }
  .kota{
    font-size: x-large;
    max-width: max-content;
    background: white;
    color: black;
    margin : auto;
  }
  .alamat{
    font-size: large;
    max-width: max-content;
    margin: auto;
    padding-bottom: 10%;
  }
  .produk{
    margin: auto;
    height : auto;
    font-size: large;
  }
  .medsos{
  margin: auto;
  height: auto;
  }
  .contact{
    margin: auto;
    height : auto;
  }
  .copyright{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    background: grey;
    text-align: center;
    font-size: medium;
  }
</style>