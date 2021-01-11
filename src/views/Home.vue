<template>
<section>
  <section class="home">
      <header class="home__top-panel">
        <nav class="home__nav">
          <a href="#" class="home__nav-links">HOME</a>
          <a href="#" class="home__nav-links">PRODUCTS</a>
          <a href="#" class="home__nav-links">FAQS</a>
          <a href="#" class="home__nav-links">CONTACT US</a>
        </nav>
        <div class="home__logo">
          <a href="#">CBD</a>
        </div>
        <div class="home__user-buttons">
          <div class="home__link-wrapper"><a href="#" class="home__btn-links">LOGIN</a></div>
          <div class="home__link-wrapper"><i class="fas fa-search"></i><a href="#" class="home__btn-links--search">SEARCH </a></div>
         <div class="home__link-wrapper"> <a href="#" class="home__btn-links">CART (0)</a></div>
        </div>
      </header >
      <div class="home__content">
        <h1 class="home__title">Enhancing Life  Excelling in Care</h1>
        <h2 class="home__subtitle"> Choose Wisely. Choose CBD.</h2>
        <div class="home__btn"><a href="#" class="home__shop-link">START SHOPPING</a></div>
        <a href="#" class="home__prod-link">See all products <i class="fas fa-long-arrow-alt-right"></i></a>

      </div>
      <h3 class="home__vertical-text"> CBD POTION HEALTH</h3>
  </section>
  <main class="about">
    <div class="about__what-we-are">
<img class="about__border" src="../assets/about-border.png" alt="border">
<h3 class="about__title">WE ARE WHAT WE ARE</h3>
<img class="about__logos" src="../assets/Logos.png" alt="Logos">
    </div>
   <div class="tabs">
<tabs />

  </div></main>
  <section class="products">
<h3 class="products__title">CBD Featured Products</h3>
<splide :options="options" style="position: relative;">
   <div class="splide__arrows">
		<button class="splide__arrow splide__arrow--prev">
      
		</button>
		<button class="splide__arrow splide__arrow--next">
		</button>
	</div>
  <splide-slide>
    <div class="products__card">
<div class="products__stars-wrapper"><i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i></div>
<h4 class="products__subtitle">CBD 500 mg Orange Flavor Tincture</h4>
    <img src="../assets/prod1.png"></div>
    <div class="products__shop"><p class="products__price"> $49.99 USD</p> <button type="submit" class="products__btn"> SHOP</button></div>
  </splide-slide>
  <splide-slide>
    <div class="products__card">
<div class="products__stars-wrapper"><i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i></div>
<h4 class="products__subtitle">Black ICE CBD Muscle Rub 200 mg</h4>
    <img src="../assets/prod2.png"></div>
    <div class="products__shop"><p class="products__price">$49.99 USD</p> <button type="submit" class="products__btn"> SHOP</button></div>
  </splide-slide>
  <splide-slide>
    <div class="products__card">
<div class="products__stars-wrapper"><i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i>
<i class="fas fa-star"></i></div>
<h4 class="products__subtitle">CBD+Curcumin Coffee 750 mg</h4>
    <img src="../assets/prod3.png"></div>
    <div class="products__shop"><p class="products__price">$49.99 USD</p> <button type="submit" class="products__btn"> SHOP</button></div>
  </splide-slide>
  
</splide>
 </section>
 <accordeon />
</section>
</template>

<script>
import Tabs from "../components/tabs";
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import '@splidejs/splide/dist/css/themes/splide-default.min.css';
import Accordeon from '../components/accordeon.vue';



export default {
  name: 'Home',
  components: {
    Tabs,
   Splide, 
   SplideSlide,
   Accordeon, 
  },
  data () {
  return {
    options: {
  type: 'loop',
  perPage: 1,
  width: '100%',
  fixedWidth: '30%',
  height: '55vh',
  perMove: 1,
  gap: '6em',
  pagination: false,
  arrowPath: 'M39.726,10.352 L39.726,10.352 L30.637,1.269 C30.311,0.888 29.737,0.843 29.356,1.170 C28.975,1.496 28.930,2.070 29.257,2.451 C29.287,2.486 29.320,2.519 29.356,2.549 L36.890,10.088 L0.909,10.088 C0.407,10.088 -0.000,10.495 -0.000,10.997 C-0.000,11.498 0.407,11.904 0.909,11.904 L36.890,11.904 L29.356,19.434 C28.975,19.761 28.930,20.334 29.257,20.715 C29.583,21.096 30.157,21.141 30.538,20.814 C30.573,20.783 30.607,20.751 30.637,20.715 L39.726,11.632 C40.078,11.278 40.078,10.706 39.726,10.352 Z',
    },
    
     };
}
  
};
</script>
<style lang="scss">
@import '../styles/core/vars.scss';

.home {
  min-height: 100vh;
  
  background-image: linear-gradient( rgba(0, 0, 0, 0.5) ,rgba(255, 255, 255, 0.1)), url('../assets/bg-header.png');
  color: white; 
  position: relative;
  font-weight: 400;
  font-family: $main-font;
  &__top-panel {
    position: fixed;
    top: 0;
    height: 7%;
    display: flex;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid $white;
  }
  &__nav {
    min-width: 25%;
    display: flex;
    justify-content: space-around;
    font-size: $nav-size;
  }
  &__nav-links {
    &:hover {
      
opacity: 0.7;
    }
    }
  
  &__logo {
    font-size: 30px;
    &:hover {
opacity: 0.7;
    }
  }
  &__user-buttons {
    font-size: $nav-size;
    display: flex;
    width: 25%;
    justify-content: space-around;
    height: 100%;
    align-items: center;
  }
 
  &__link-wrapper {
    height: 100%;
    width: 100%;
    border-left: 1px solid $white;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    
    
  }
  &__btn-links {
    width: 100%;
    &--search {
      width: 50%;
&:hover {
opacity: 0.7;
    }
    }
    &:hover {
opacity: 0.7;
    }
    
  }
  &__content {
    display: flex;
    margin: auto;
    flex-direction: column;
    height: 90vh;
    width: 60%;
    justify-content: center;
    align-items: flex-end;
    padding-top: 100px;
  }
  &__title {
    font-size: $title-size;
    line-height: 75px;
    letter-spacing: 13px;
    text-transform: uppercase;
    text-align: right;
    width: 70%;
    margin-bottom: 15px;
    font-weight: 400;
  }&__subtitle {
    font-size: $sub-title-size;
    line-height: 75px;
    font-weight: 300;
    letter-spacing: 7px;
    margin-bottom: 50px;
  }
  &__btn {
    min-width: 280px;
    min-height: 70px;
    border: 1px solid $white;
    display: flex;
    align-items: center;
    cursor: pointer;
    position: relative;
    font-size: $btn-size;
    margin-bottom: 30px;
    &:after {
      position: absolute;
      content: "";
      border-top: 2px solid $white;
      width: 45px;
      right: 40px;
    }
  }
  &__shop-link {
    width: 200px;
    &:hover {
opacity: 0.7;
    }
  }
  &__prod-link {
    font-weight: 300px;
    font-size: $link-size;
  line-height: 75px;
  letter-spacing: 5px;
  &:hover {
opacity: 0.7;
    }
  }
  &__vertical-text {
    transform: rotate(270deg);
    position: absolute;
    left: 30px;
    font-size: $middle-size;
    bottom: 170px;
    display: block;
    &:before {
      content: "";
      border-bottom: 2px solid $white;
      width: 70px;
      height: 2px;
      position: absolute;
      bottom:18px;
      left: -90px;
    }
  }
.fa-long-arrow-alt-right {
  padding-left: 15px;
}


}
.about {
  background-color: $bgc-color;
  min-height: 100vh;
  text-align: center;
  padding-top: 2%;
  font-family: $main-font;
  
  &__border {
    position: absolute;
    left: 50%;
    top: 5%;
	-webkit-transform: translate(-50%);
    -ms-transform: translate(-50%);
        transform: translate(-50%);
        margin-bottom: 80px;
  }
  &__title {
    position: absolute;
    top: 45%;
    left: 50%;
    z-index: 100;
    font-size: $sub-title-size;
    line-height: 75px;
    letter-spacing: 6px;
    -webkit-transform: translate(-50%);
    -ms-transform: translate(-50%);
        transform: translate(-50%);
  }
  
  &__logos {
position: absolute;
top: 70%;
left: 50%;
-webkit-transform: translate(-50%);
    -ms-transform: translate(-50%);
        transform: translate(-50%);
  }
  &__what-we-are {
    width: 100%;
    height: 300px;
    position: relative;
    margin-bottom: 100px;
  }

}

.products {
  font-family: $main-font;
width: 100%;
text-transform: uppercase;
min-height: 80vh;
margin-bottom: 5%;
&__title {
  font-size: $logo-size;
  margin-bottom: 75px;
}
&__card {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 450px;
  background-color: $white;
  border: 1px solid $tabs-border;
}
&__stars-wrapper {
  color: $star-color;
}
&__shop {
  background-color: $price-bcg;
  height: 75px;
  border-left: 1px solid $price-border;
  border-bottom: 1px solid $price-border;
  text-align: left;
  color: $white;
}
&__price {
  width: 69%;
  text-align: left;
  height: 100%;
  margin: 0;
  display: inline-block;
  padding-left: 10%;
  font-size: $link-size;
  color: $black;
  border-bottom: 1px solid $price-border;
}
&__btn {
  width: 30%;
  height: 100%;
  font-size: $btn-size;
  text-align: left;
  padding-left: 5%;
  background-color: $text-color;
  color: $white;
  position: relative;
  &::after {
    content: '';
    position: absolute;
    width: 30%;
    border-bottom: 2px solid $white;
    top: 49%;
    right: 15%;
  }
  &:hover {
    opacity: 0.9;
  }
}
}

.splide {
  height: 600px;
&__arrows {
  position: absolute;
  top: 50%;
  z-index: 100;
  height: 100%;
  width: 100%;
  }}


.splide__arrow--prev {
  background: none;
  position: absolute;
  left: 47%;
  
  color: $arrow;
  
}

.splide__arrow--next {
  background: none;
  position: absolute;
  right: 47%;
  color: $arrow;
}



</style>
