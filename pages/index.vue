<template>
  <v-row class="mt-0 mx-0 overflow-hidden">
    <!--Start header section-->
    <v-col
      cols="12"
      class="header-section pa-0 d-flex flex-column justify-space-between"
    >
      <top-header />
      <v-container>
        <v-col class="text-panel white--text mx-auto px-12">
          Royal Coster Diamonds is famous for the highest level of craftsmanship
          since 1840.
        </v-col>
      </v-container>
      <sub-header />
    </v-col>
    <!--End header section-->

    <!--Start text section-->
    <v-col
      cols="12"
      class="text-section d-flex justify-center align-center"
    >
      <p class="mx-auto text-center">
        With an extensive stock of loose and set diamonds, we have the most
        beautiful diamond jewelry. For more than 180 years, our craftsmen and
        women create beauty that lasts for centuries.
      </p>
      <div class="rotate-logo">
        <img src="~/assets/img/image 1.png" alt="rotate-logo" />
        <div id="circle">
          <svg
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            width="300px"
            height="300px"
            viewBox="0 0 300 300"
            enable-background="new 0 0 300 300"
            xml:space="preserve"
          >
            <defs>
              <path
                id="circlePath"
                d="M 150, 150 m -60, 0 a 60,60 0 0,1 120,0 a 60,60 0 0,1 -120,0 "
              />
            </defs>
            <circle cx="150" cy="100" r="75" fill="none" />
            <g>
              <use xlink:href="#circlePath" fill="none" />
              <text fill="#000">
                <textPath class="svg_text" xlink:href="#circlePath">
                  DISCOVER THE JEWELRY COLLECTION
                </textPath>
              </text>
            </g>
          </svg>
        </div>
      </div>
    </v-col>
    <!--End text section-->

    <!--Start shopping section-->
    <v-col cols="12" class="shopping-section d-flex align-center">
      <v-col cols="4" class="image-panel--left text-center">
        <img src="~/assets/img/Rectangle 95.png" alt="ads-img" />
      </v-col>
      <v-col cols="4" class="text-panel text-center">
        <h3>Rings</h3>
        <p class="mt-3">Earrrings<br />Bracelets<br />Necklaces<br />Watches</p>
        <v-btn
          tile
          color="grey darken-4"
          class="px-lg-8 py-lg-5 px-md-7 py-md-4 white--text"
          >SHOP NOW</v-btn
        >
      </v-col>
      <v-col cols="4" class="image-panel--right text-center">
        <img src="~/assets/img/Group 88.png" class="d-block mb-10 top-img" />
        <img src="~/assets/img/Rectangle 90.png" class="bottom-img" />
      </v-col>
      <div class="blur-pink-area"></div>
      <div class="blur-blue-area"></div>
    </v-col>
    <!--End shopping section-->

    <!--Start banner section-->
    <v-col cols="12" class="banner-section pa-0">
      <img src="~/assets/img/Rectangle 62.jpg" alt="video-image" />
    </v-col>
    <!--End banner section-->

    <!--Start Collection Section-->
    <v-col cols="12" class="collection-section pt-16">
      <div class="text-panel mx-auto mt-16 pt-16">
        <h2 class="collection-title mb-10 pt-16">
          Latest Collection
        </h2>
        <div class="d-flex align-center justify-space-between">
          <p class="collection-description">
            Making a luxurious lifestyle accessible for a generous group by our
            Jewelry Collection.
          </p>
          <img class="carousel-arrow" src="~/assets/img/Group 95.png" />
        </div>
      </div>
      <div class="slider-panel">
        <VueSlickCarousel v-bind="collectionCarouselSettings">
          <div
            v-for="(item, index) in collectionImages"
            :key="index"
            :class="
              index % 2 == 0
                ? 'pt-10 pr-5 carousel-item d-flex justify-center'
                : 'pr-5 carousel-item d-flex justify-center'
            "
          >
            <img :src="item.url" alt="carousel-img" />
          </div>
        </VueSlickCarousel>
      </div>
    </v-col>
    <!--End Collection Section-->

    <!--Start Product Section-->
    <v-col
      cols="12"
      class="product-section d-flex flex-column justify-center align-center"
    >
      <h2 class="product-section__title mt-16">Amazing Experience</h2>
      <VueSlickCarousel
        v-bind="productCarouselSettiing"
        class="product-carousel mt-16"
      >
        <div
          v-for="(item, index) in productImages"
          :key="index"
          class="carousel-item d-flex justify-center"
        >
          <img :src="item.url" alt="carousel-img" />
          <img src="~/assets/img/Group 104.png" class="video-ico" />
        </div>
      </VueSlickCarousel>
      <img src="~/assets/img/Group 95.png" class="mx-auto mt-10" />
    </v-col>
    <!--End Product Section-->

    <!--Start Contact Section-->
    <v-col
      cols="12"
      class="contact-section d-flex flex-column justify-center align-center"
    >
      <v-container class="contact-text-panel px-0">
        <h2 class="contact-title">Follow Us on<br />Instagram</h2>
        <p class="contact-info mt-5">@royalcosterdiamonds</p>
      </v-container>
      <VueSlickCarousel
        v-bind="contactCarouselSettings"
        class="contact-carousel mt-10"
      >
        <div
          v-for="(item, index) in contactImages"
          :key="index"
          class="carousel-item d-flex justify-center"
        >
          <img :src="item.url" alt="carousel-img" />
        </div>
      </VueSlickCarousel>
    </v-col>
    <!--End Contact Section-->
    <main-footer />
  </v-row>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "MyComponent",
  components: { VueSlickCarousel },
  data: () => ({
    collectionCarouselSettings: {
      dots: false,
      infinite: true,
      slidesToShow: 4.9,
      // slidesToScroll: 1,
      autoplay: true,
      centerMode: true,
      centerPadding: "20px",
      responsive: [
        {
          breakpoint: 768,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 3
          }
        },
        {
          breakpoint: 480,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 1
          }
        }
      ]
    },
    productCarouselSettiing: {
      arrows: false,
      dots: false,
      infinite: true,
      centerMode: true,
      autoplay: true,
      // speed: 2000,
      // autoplaySpeed: 2000,
      // cssEase: "linear",
      centerPadding: "20px",
      slidesToShow: 4.32,
      responsive: [
        {
          breakpoint: 768,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 3
          }
        },
        {
          breakpoint: 480,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 1
          }
        }
      ]
    },
    contactCarouselSettings: {
      dots: false,
      infinite: true,
      slidesToShow: 6.6,
      slidesToScroll: 1,
      autoplay: true,
      centerMode: true,
      centerPadding: "20px",
      responsive: [
        {
          breakpoint: 768,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 3
          }
        },
        {
          breakpoint: 480,
          settings: {
            arrows: false,
            centerMode: true,
            centerPadding: "40px",
            slidesToShow: 1
          }
        }
      ]
    },
    collectionImages: [
      { url: require("~/assets/img/Rectangle 105.png") },
      { url: require("~/assets/img/Group 96.png") },
      { url: require("~/assets/img/Group 97.png") },
      { url: require("~/assets/img/Group 98.png") },
      { url: require("~/assets/img/Group 96.png") },
      { url: require("~/assets/img/Group 97.png") },
      { url: require("~/assets/img/Group 98.png") },
      { url: require("~/assets/img/Group 96.png") },
      { url: require("~/assets/img/Group 97.png") },
      { url: require("~/assets/img/Group 98.png") }
    ],
    productImages: [
      { url: require("~/assets/img/Group 100.png") },
      { url: require("~/assets/img/Group 101.png") },
      { url: require("~/assets/img/Group 102.png") },
      { url: require("~/assets/img/Group 103.png") },
      { url: require("~/assets/img/Group 101.png") },
      { url: require("~/assets/img/Group 102.png") },
      { url: require("~/assets/img/Group 103.png") }
    ],
    contactImages: [
      { url: require("~/assets/img/Rectangle 112.png") },
      { url: require("~/assets/img/Rectangle 113.png") },
      { url: require("~/assets/img/Rectangle 114.png") },
      { url: require("~/assets/img/Rectangle 115.png") },
      { url: require("~/assets/img/Rectangle 135 (1).png") },
      { url: require("~/assets/img/Rectangle 113.png") },
      { url: require("~/assets/img/Rectangle 114.png") },
      { url: require("~/assets/img/Rectangle 115.png") },
      { url: require("~/assets/img/Rectangle 135 (1).png") }
    ]
  })
};
</script>

<style scoped>
/** Header section*/
.header-section {
  background: url("~/assets/img/Rectangle 137.jpg");
  background-size: cover;
}
.header-section .text-panel {
  font-size: 72px;
  line-height: 120%;
  text-align: center;
  width: 60%;
  font-family: Canela, sans-serif;
  font-weight: normal;
}
.header-section .container {
  padding-top: 13%;
  padding-bottom: 13%;
}
/**Text section */
.text-section {
  position: relative;
  padding-top: 14%;
  padding-bottom: 14%;
  background-color: #f7f3ec;
}
.text-section p {
  width: 65%;
  line-height: 132%;
  color: #01215c;
  font-weight: 250;
  font-size: 64px;
  font-family: Canela, sans-serif;
}
#circle {
  position: absolute;
  width: 100%;
  z-index: 10;
  padding-bottom: 540px;
  overflow: hidden;
}

.rotate-logo {
  position: absolute;
  bottom: -270px;
  height: 540px;
  z-index: 10;
  width: 100%;
}

.rotate-logo > img {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100px;
  height: 100px;
}

#circle .svg_text {
  letter-spacing: 6.5px;
  font-weight: lighter;
  font-family: Montserrat, sans-serif;
  font-size: 8px;
  font-weight: normal;
}

#circle svg {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 540px;

  -webkit-animation-name: rotate;
  -moz-animation-name: rotate;
  -ms-animation-name: rotate;
  -o-animation-name: rotate;
  animation-name: rotate;
  -webkit-animation-duration: 10s;
  -moz-animation-duration: 10s;
  -ms-animation-duration: 10s;
  -o-animation-duration: 10s;
  animation-duration: 10s;
  -webkit-animation-iteration-count: infinite;
  -moz-animation-iteration-count: infinite;
  -ms-animation-iteration-count: infinite;
  -o-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  -moz-animation-timing-function: linear;
  -ms-animation-timing-function: linear;
  -o-animation-timing-function: linear;
  animation-timing-function: linear;
}

@-webkit-keyframes rotate {
  from {
    -webkit-transform: rotate(360deg);
  }
  to {
    -webkit-transform: rotate(0);
  }
}
@-moz-keyframes rotate {
  from {
    -moz-transform: rotate(360deg);
  }
  to {
    -moz-transform: rotate(0);
  }
}
@-ms-keyframes rotate {
  from {
    -ms-transform: rotate(360deg);
  }
  to {
    -ms-transform: rotate(0);
  }
}
@-o-keyframes rotate {
  from {
    -o-transform: rotate(360deg);
  }
  to {
    -o-transform: rotate(0);
  }
}
@keyframes rotate {
  from {
    transform: rotate(360deg);
  }
  to {
    transform: rotate(0);
  }
}

/**Shopping section */
.shopping-section {
  position: relative;
  background: white;
  padding-top: 11%;
  padding-bottom: 11%;
}
.shopping-section > .col {
  position: relative;
  z-index: 10;
}
.shopping-section .image-panel--left img {
  width: 80%;
}
.shopping-section .image-panel--right img.top-img {
  width: 50%;
}
.shopping-section .image-panel--right img.bottom-img {
  width: 35%;
}
.shopping-section .blur-pink-area {
  content: "";
  position: absolute;
  width: 25vw;
  height: 25vw;
  background: #fad3da;
  opacity: 0.7;
  filter: blur(300px);
  right: 50%;
  top: 50%;
  transform: translate(0, -50%);
}
.shopping-section .blur-blue-area {
  content: "";
  position: absolute;
  width: 15vw;
  height: 15vw;
  background: #13439b;
  opacity: 0.3;
  filter: blur(300px);
  left: 55%;
  top: 50%;
}
.shopping-section .text-panel h3 {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 72px;
  line-height: 104.5%;
  color: #000000;
  box-sizing: border-box;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
}
.shopping-section .text-panel p {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: 250;
  font-size: 72px;
  line-height: 140%;
  color: rgba(0, 0, 0, 0.5);
}
.shopping-section .text-panel button {
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 17px;
  text-transform: uppercase;
  color: #ffffff;
}
/**Content banner section */
.banner-section {
  position: relative;
}
.banner-section > img {
  width: 100%;
  height: 100%;
}

.banner-section:hover::after {
  content: "PLAY VIDEO";
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
  width: 130px;
  height: 130px;
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border: 1px solid #ffffff;
  font-family: Montserrat, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 110%;
  color: #ffffff;
}

/**collection section */
.collection-section {
  position: relative;
  background: linear-gradient(
    180deg,
    rgba(236, 227, 212, 0.7) 0%,
    #f7f3ec 100%
  );
}
.collection-section .text-panel {
  width: 80%;
  padding-bottom: 20%;
}
.collection-title {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: 250;
  font-size: 244px;
  line-height: 100%;
  color: #01215c;
  mix-blend-mode: normal;
}
.collection-description {
  width: 42%;
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 24px;
  line-height: 163%;
  color: rgba(0, 0, 0, 0.7);
}
.collection-section .slider-panel {
  position: absolute;
  width: 100%;
  bottom: 0;
  transform: translate(0, 30%);
}
.collection-section .carousel-item img {
  width: 95%;
}

/**product section */
.product-section {
  padding-top: 12%;
  padding-bottom: 12%;
  background: white;
}
.product-section .product-carousel {
  width: 100%;
}
.product-carousel .carousel-item {
  height: 500px;
  position: relative;
  display: flex;
  align-items: center;
}
.product-section .carousel-item img {
  margin: auto;
  width: 80%;
}
.product-carousel .slick-track .slick-slide {
  display: flex;
  align-items: center;
}
.product-section .slick-center.slick-current img {
  width: 100%;
}
.product-carousel .video-ico {
  position: absolute;
  width: 50px !important;
  height: 50px !important;
  top: 45%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10;
  display: none;
}
.product-section .slick-center.slick-current:hover .video-ico {
  display: block;
}
.product-section__title {
  width: 50%;
  font-family: Canela, sans-serif;
  font-size: 144px;
  line-height: 110%;
  text-align: center;
  color: #01215c;
}

/**contact section */
.contact-section {
  height: 100vh;
  background: linear-gradient(180deg, #f7f3ec 0%, rgba(247, 243, 236, 0) 100%);
}
.contact-text-panel {
  width: 80%;
}
.contact-section .contact-title {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 72px;
  line-height: 110%;
  color: #01215c;
  mix-blend-mode: normal;
}
.contact-section .contact-info {
  font-family: Canela, sans-serif;
  font-style: normal;
  font-weight: 250;
  font-size: 36px;
  line-height: 110%;
  color: #01215c;
  mix-blend-mode: normal;
}
.contact-section .contact-carousel {
  width: 100%;
}
.contact-carousel .carousel-item img {
  width: 90%;
  height: 100%;
}

@media (max-width: 1440px) {
  /**header section */
  .header-section .text-panel {
    width: auto;
  }

  /**text section */
  .text-section p {
    width: 85%;
  }
}

@media (max-width: 1228px) {
  /**collection section */
  .collection-title {
    font-size: 150px;
  }

  /**product section */
  .product-section__title {
    width: 80%;
  }
  .product-section .carousel-item img {
    width: 100%;
  }
  .product-section .slick-center.slick-current img {
    width: 130%;
  }
}

@media (max-width: 1024px) {
  /**product section */
  .product-section__title {
    width: 100%;
  }

  /**shopping section */
  .shopping-section .text-panel h3,
  .shopping-section .text-panel p {
    font-size: 55px;
  }

  @media (max-width: 768px) {
    /**header section */
    .header-section .text-panel {
      font-size: 60px;
    }

    /**text section */
    .text-section p {
      font-size: 60px;
    }

    /**collection section */
    .collection-title {
      font-size: 110px;
    }

    /**product section */
    .product-section__title {
      font-size: 110px;
    }
  }
}
</style>
