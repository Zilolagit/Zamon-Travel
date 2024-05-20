<template>
  <!-- Header Start -->
  <header class="header">
    <div class="container">
      <div class="row">
        <div class="col-6 col-lg-3 d-flex align-items-center">
          <div class="header__logo">
            <a href="/">
              <img src="../public/logo.svg" alt="logo" />
            </a>
          </div>
        </div>
        <div class="col-lg-6 d-none d-lg-flex justify-content-end align-items-center">
          <ul class="header__list">
            <li class="header__item header__item-active">
              <a href="/">{{ $t('home') }}</a>
            </li>
            <li class="header__item"><a href="#about">{{ $t('about') }}</a></li>
            <li class="header__item"><a href="#tour">{{ $t('tours') }}</a></li>
            <li class="header__item"><a href="#contacts">{{ $t('contacts') }}</a></li>
          </ul>
        </div>
        <div class="col-lg-3 d-none d-lg-flex justify-content-end" style="gap: 25px">
          <ul class="header__lang">
            <li @click="changeLang('uz')"><a href="#" @click="$i18n.locale = 'uz'">UZ</a></li>
            <li @click="changeLang('en')"><a href="#" @click="$i18n.locale = 'en'">ENG</a></li>
            <li @click="changeLang('ru')"><a href="#" @click="$i18n.locale = 'ru'">RU</a></li>
          </ul>
          <ul class="header__social">
            <li>
              <a href="#"><i class="fa-brands fa-telegram"></i></a>
            </li>
            <li>
              <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </li>
          </ul>
        </div>
        <div class="col-6 d-flex justify-content-end align-items-center d-lg-none">
          <div class="header__bars" @click="openMenu">
            <div class="header__bar header__bar-first"></div>
            <div class="header__bar header__bar-second"></div>
            <div class="header__bar header__bar-third"></div>
          </div>
        </div>
      </div>
      <div class="header__mobile" v-if="isOpen">
        <ul class="header__menu">
          <li><a href="/">{{ $t('home') }}</a></li>
          <li><a href="#about">{{ $t('about') }}</a></li>
          <li><a href="#tours">{{ $t('tours') }}</a></li>
          <li><a href="#contacts">{{ $t('contacts') }}</a></li>
          <li><a href="#">UZ</a></li>
          <li><a href="#">ENG</a></li>
          <li><a href="#">RU</a></li>
          <li>
            <a href="#"><i class="fa-brands fa-telegram"></i> </a>
          </li>
          <li>
            <a href="#"><i class="fa-brands fa-instagram"></i> </a>
          </li>
        </ul>
      </div>
    </div>
  </header>
  <!-- Header End -->

  <!-- Hero Start -->
  <section class="hero">
    <div class="container-fluid" style="padding-left: 0; padding-right: 0">
      <div id="carouselExampleDark" class="carousel carousel-dark carousel-fade">
        <div class="carousel-indicators">
          <div class="hero__indicate">
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active"
              aria-current="true" aria-label="Slide 1"></button>
            <p>1</p>
          </div>
          <div class="hero__indicate">
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1"
              aria-label="Slide 2"></button>
            <p>2</p>
          </div>
          <div class="hero__indicate">
            <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="2"
              aria-label="Slide 3"></button>
            <p>3</p>
          </div>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active" style="
              background-image: url(../public/istanbul1.jpg);
            " data-bs-interval="1000">
            <div>
              <div class="container text-center">
                <h2>{{ $t('hero_desc') }}</h2>
                <h1>{{ $t('hero_title_first') }}</h1>
                <div class="hero__btn">
                  <a href="#contacts"><button class="button">{{ $t('go_there') }}</button></a>
                </div>
                <div class="hero__card">
                  <div class="row">
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-user"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('population') }}</p>
                        <h4>8.66 M</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-globe"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('territory') }}</p>
                        <h4>513.120 KM2</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-house"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('price') }}</p>
                        <h4>$165.450</h4>
                      </div>
                    </div>
                    <div
                      class="col-6 col-lg-3 mb-lg-0 d-flex justify-content-lg-end justify-content-start align-items-center">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore') }}
                        </button>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="carousel-item" data-bs-interval="2000" style="
              background-image: url(../public/sharm.jpg);
            ">
            <div>
              <div class="container text-center">
                <h2>{{ $t('hero_desc') }}</h2>
                <h1>{{ $t('hero_title_second') }}</h1>
                <div class="hero__btn">
                  <a href="#contacts"><button class="button">{{ $t('go_there') }}</button></a>
                </div>
                <div class="hero__card">
                  <div class="row">
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-user"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('population') }}</p>
                        <h4>8.66 M</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-globe"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('territory') }}</p>
                        <h4>513.120 KM2</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-house"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('price') }}</p>
                        <h4>$165.450</h4>
                      </div>
                    </div>
                    <div
                      class="col-6 col-lg-3 mb-lg-0 d-flex justify-content-lg-end justify-content-start align-items-center">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore') }}
                        </button>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="carousel-item text-center" style="
              background-image: url(../public/dubay1.jpg);
            ">
            <div>
              <div class="container text-center">
                <h2>{{ $t('hero_desc') }}</h2>
                <h1>{{ $t('hero_title_third') }}</h1>
                <div class="hero__btn">
                  <a href="#contacts"><button class="button">{{ $t('go_there') }}</button></a>
                </div>
                <div class="hero__card">
                  <div class="row">
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-user"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('population') }}:</p>
                        <h4>8.66 M</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-4 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-globe"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('territory') }}</p>
                        <h4>513.120 KM2</h4>
                      </div>
                    </div>
                    <div class="col-6 col-lg-3 mb-lg-0 d-flex align-items-center" style="gap: 20px">
                      <div class="hero__icon">
                        <i class="fa-solid fa-house"></i>
                      </div>
                      <div class="hero__box">
                        <p>{{ $t('price') }}</p>
                        <h4>$165.450</h4>
                      </div>
                    </div>
                    <div
                      class="col-6 col-lg-3 mb-lg-0 d-flex justify-content-lg-end justify-content-start align-items-center">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore') }}
                        </button>
                      </a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Hero End -->

  <!-- Offer Start -->
  <section class="offer" id="tour">
    <div class="container">
      <h2>{{ $t('offer_title') }}</h2>
      <p>
        {{ $t('offer_desc') }}
      </p>
      <swiper :slidesPerView="3" :spaceBetween="30" :navigation="true" :modules="modules" :autoplay="{
                delay: 10,
                disableOnInteraction: false,
              }" class="mySwiper">
        <swiper-slide>
          <img src="../public/bg-1.jpg" alt="bg-1" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card1.title') }}</h4>
              <h3>$450</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card1.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card1.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card1.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card1.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-2.jpg" alt="bg-2" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card2.title') }}</h4>
              <h3>$550</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card2.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card2.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card2.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card2.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-3.jpg" alt="bg-3" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card3.title') }}</h4>
              <h3>$550</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card3.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card3.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card3.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card3.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-4.jpg" alt="bg-4" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card4.title') }}</h4>
              <h3>$550</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card4.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card4.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card4.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card4.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-5.jpg" alt="bg-5" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card5.title') }}</h4>
              <h3>$550</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card5.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card5.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card5.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card5.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-6.jpg" alt="bg-6" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('card6.title') }}</h4>
              <h3>$550</h3>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('card6.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('deal') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-car"></i>
              <span>{{ $t('card6.car') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-plane"></i>
              <span>{{ $t('card6.plane') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-building"></i>
              <span>{{ $t('card6.building') }} </span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
  <!-- Offer End -->

  <!-- Visa Start -->
  <section class="visa">
    <div class="container">
      <h2>{{ $t('visa_title') }}</h2>
      <p>
        {{ $t('visa_desc') }}
      </p>
      <swiper :slidesPerView="3" :spaceBetween="30" :navigation="true" :modules="modules" :autoplay="{
                delay: 10,
                disableOnInteraction: false,
              }" class="mySwiper">
        <swiper-slide>
          <img src="../public/bg-1.jpg" alt="bg-1" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa1.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa1.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa1.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa1.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa1.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-2.jpg" alt="bg-2" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa2.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa2.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa2.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa2.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa2.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-3.jpg" alt="bg-3" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa3.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa3.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa3.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa3.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa3.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-4.jpg" alt="bg-4" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa4.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa4.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa4.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa4.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa4.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-5.jpg" alt="bg-5" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa5.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa5.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa5.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa5.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa5.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
        <swiper-slide>
          <img src="../public/bg-6.jpg" alt="bg-6" />
          <div class="offer__card">
            <div class="offer__top">
              <h4>{{ $t('visa6.title') }}</h4>
            </div>
            <div class="offer__icon offer__list">
              <i class="fa-solid fa-users"></i>
              <span>{{ $t('visa6.person') }}</span>
            </div>
            <h6 class="mb-3 pt-4">{{ $t('visa_benefit') }}</h6>
            <div class="offer__icon">
              <i class="fa-solid fa-tags"></i>
              <span>{{ $t('visa6.price') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-clock"></i>
              <span>{{ $t('visa6.time') }}</span>
            </div>
            <div class="offer__icon">
              <i class="fa-solid fa-check"></i>
              <span>{{ $t('visa6.check') }}</span>
            </div>
            <a href="#contacts">
              <button class="button button-opacity">{{ $t('reserve') }}</button>
            </a>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </section>
  <!-- Visa End -->

  <!-- Explore Start -->
  <section id="about" class="explore">
    <div class="container">
      <h3 class="explore__title">{{ $t('explore_title') }}</h3>
      <p class="explore__desc">
        {{ $t('explore_desc') }}
      </p>
      <div class="row">
        <div class="col-xl-10">
          <div class="box">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/train.jpg" alt="train" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('explore1.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('explore1.small') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('explore1.desc') }}
                    </p>
                  </div>
                  <div class="box__btn mt-2 mt-sm-3 d-md-none">
                    <a href="#contacts">
                      <button class="button button-opacity">
                        {{ $t('explore_more') }}
                      </button>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="box mt-4">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/plame.jpg" alt="plame" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('explore2.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('explore2.small') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('explore2.desc') }}
                    </p>
                  </div>
                  <div class="box__btn mt-2 mt-sm-3 d-md-none">
                    <a href="#contacts">
                      <button class="button button-opacity">
                        {{ $t('explore_more') }}
                      </button>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        
        </div>
      </div>
    </div>
  </section>
  <!-- Explore End -->

  <!-- Country Start -->
  <section class="country mt-4 pb-5">
    <div class="container">
      <h3 class="explore__title">{{ $t('country_title') }}</h3>
      <p class="explore__desc">
        {{ $t('country_desc') }}
      </p>
      <div class="row">
        <div class="col-xl-10">
          <div class="box">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/dubay.jpg" alt="train" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('country1.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('country1.country') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('country1.desc') }}
                    </p>
                  </div>
                  <ul class="box__list mx-0 mx-sm-3 px-3 px-sm-0">
                    <li>
                      <i class="fa-solid fa-user"></i>
                      <span> 8.66 {{ $t('country_people') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-globe"></i>
                      <span> 41.290 {{ $t('country_km') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-house"></i>
                      <span> $1.100.200</span>
                    </li>
                  </ul>
                  <div class="box__link">
                    <a href="#contacts">{{ $t('country_link') }}</a>
                    <i class="fa-solid fa-arrow-right"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="box mt-5">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/antalya.jpg" alt="antalya" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('country1.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('country2.country') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('country2.desc') }}
                    </p>
                  </div>
                  <ul class="box__list mx-0 mx-sm-3 px-3 px-sm-0">
                    <li>
                      <i class="fa-solid fa-user"></i>
                      <span> 8.66 {{ $t('country_people') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-globe"></i>
                      <span> 41.290 {{ $t('country_km') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-house"></i>
                      <span> $1.100.200</span>
                    </li>
                  </ul>
                  <div class="box__link">
                    <a href="#contacts">{{ $t('country_link') }}</a>
                    <i class="fa-solid fa-arrow-right"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="box mt-5">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/egypt.jpg" alt="egypt" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('country3.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('country3.country') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('country3.desc') }}
                    </p>
                  </div>
                  <ul class="box__list mx-0 mx-sm-3 px-3 px-sm-0">
                    <li>
                      <i class="fa-solid fa-user"></i>
                      <span> 8.66 {{ $t('country_people') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-globe"></i>
                      <span> 41.290 {{ $t('country_km') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-house"></i>
                      <span> $1.100.200</span>
                    </li>
                  </ul>
                  <div class="box__link">
                    <a href="#contacts">{{ $t('country_link') }}</a>
                    <i class="fa-solid fa-arrow-right"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="box mt-5">
            <div class="row">
              <div class="col-lg-4 mb-4 mb-lg-0">
                <div class="box__image">
                  <img src="../public/istanbul.jpg" alt="istanbul" />
                </div>
              </div>
              <div class="col-lg-8">
                <div class="row">
                  <div class="col-md-8">
                    <div class="box__title">
                      <h5>{{ $t('country4.title') }}</h5>
                    </div>
                    <div class="box__desc">
                      <p>{{ $t('country4.country') }}</p>
                    </div>
                  </div>
                  <div class="col-md-4 d-none d-md-flex justify-content-end">
                    <div class="box__btn">
                      <a href="#contacts">
                        <button class="button button-opacity">
                          {{ $t('explore_more') }}
                        </button>
                      </a>
                    </div>
                  </div>
                  <div class="box__info">
                    <p>
                      {{ $t('country4.desc') }}
                    </p>
                  </div>
                  <ul class="box__list mx-0 mx-sm-3 px-3 px-sm-0">
                    <li>
                      <i class="fa-solid fa-user"></i>
                      <span> 8.66 {{ $t('country_people') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-globe"></i>
                      <span> 41.290 {{ $t('country_km') }}</span>
                    </li>
                    <li>
                      <i class="fa-solid fa-house"></i>
                      <span> $1.100.200</span>
                    </li>
                  </ul>
                  <div class="box__link">
                    <a href="#contacts">{{ $t('country_link') }}</a>
                    <i class="fa-solid fa-arrow-right"></i>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Country End -->

  <!-- Best Start -->
  <section class="best">
    <div class="container">
      <div class="text-center">
        <h3 class="best__title">{{ $t('location_title') }}</h3>
      <p class="best__desc" style="margin: 0px auto;">
        {{ $t('location_desc') }}
      </p>
      </div>
      <div class="best__flex">
        <div class="best__item" @click="activeItem = 'first'" :class="{'best__item-active' : activeItem == 'first'}" style="background-image: url(../public/1.jpg); background-size: cover;">
          <div class="best__box">
            <i class="fa-solid fa-expand"></i>
          </div>
          <div class="best__text">
            <h5>{{ $t('location.card1.title') }}</h5>
            <p>{{ $t('people') }}: 3M</p>
          </div>
        </div>
        <div class="best__item" @click="activeItem = 'second'" :class="{'best__item-active' : activeItem == 'second'}" style="background-image: url(../public/istan.jpg); background-size: cover;">
          <div class="best__box">
            <i class="fa-solid fa-expand"></i>
          </div>
          <div class="best__text">
            <h5>{{ $t('location.card2.title') }}</h5>
            <p>{{ $t('people') }}: 3M</p>
          </div>
        </div>
        <div class="best__item" @click="activeItem = 'third'" :class="{'best__item-active' : activeItem == 'third'}" style="background-image: url(../public/3.jpg); background-size: cover;">
          <div class="best__box">
            <i class="fa-solid fa-expand"></i>
          </div>
          <div class="best__text">
            <h5>{{ $t('location.card3.title') }}</h5>
            <p>{{ $t('people') }}: 3M</p>
          </div>
        </div>
        <div class="best__item d-none d-md-block" @click="activeItem = 'fourth'" :class="{'best__item-active' : activeItem == 'fourth'}" style="background-image: url(../public/dubay.jpg); background-size: cover;">
          <div class="best__box">
            <i class="fa-solid fa-expand"></i>
          </div>
          <div class="best__text">
            <h5>{{ $t('location.card4.title') }}</h5>
            <p>{{ $t('people') }}: 3M</p>
          </div>
        </div>
        <div class="best__item d-none d-md-block" @click="activeItem = 'fifth'" :class="{'best__item-active' : activeItem == 'fifth'}" style="background-image: url(../public/5.jpg); background-size: cover;">
          <div class="best__box">
            <i class="fa-solid fa-expand"></i>
          </div>
          <div class="best__text">
            <h5>{{ $t('location.card5.title') }}</h5>
            <p>{{ $t('people') }}: 3M</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Best End -->

  <!-- Reservation Start -->
  <section class="reservation">
    <div class="container">
      <h4>{{ $t('book_desc') }}</h4>
      <div class="hr"></div>
      <h2>{{ $t('book_title') }}</h2>
      <div class="reservation__btn" style="padding-bottom: 30px">
        <a href="#contacts">
          <button class="button button-white">{{ $t('book_discover') }}</button>
        </a>
      </div>
      <div class="row reservation__row">
        <div class="col-12 col-md-6 col-lg-4 mb-4 mb-lg-0">
          <div class="iconbox">
            <div class="iconbox__icon">
              <i class="fa-solid fa-phone"></i>
            </div>
            <h4>{{ $t('book_phone') }}</h4>
            <a href="tel:+998943939999">+998 99 299 99 96</a>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4">
          <div class="iconbox">
            <div class="iconbox__icon">
              <i class="fa-solid fa-envelope"></i>
            </div>
            <h4>{{ $t('book_email') }}</h4>
            <a href="mailto:zamonbiznestour@mail.ru">zamonbiznestour@mail.ru</a>
          </div>
        </div>
        <div class="col-12 col-md-6 col-lg-4 mt-4 mt-lg-0">
          <div class="iconbox">
            <div class="iconbox__icon">
              <i class="fa-solid fa-location-dot"></i>
            </div>
            <h4>{{ $t('book_office') }}</h4>
            <a href="#">{{ $t('book_map') }}</a>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Reservation End -->

  <!-- Contact Start -->
  <section class="contact" id="contacts" style="padding-top: 100px; padding-bottom: 100px">
    <div class="container">
      <div class="contact__map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d5425.747982123416!2d69.201104!3d41.290949!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae89a274fdb9b7%3A0x2b8bc58608ca7fb2!2sChilanzar-25%2C%20100152%2C%20Tashkent%2C%20Tashkent%20Region%2C%20Uzbekistan!5e1!3m2!1sen!2sus!4v1716135766484!5m2!1sen!2sus"
          width="600" height="450" style="border: 0" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"></iframe>
        <div class="contact__box">
          <h2 class="text-center mb-3">
            {{ $t('form_title1') }} <span style="color: #22b3c1">{{ $t('form_title2') }}</span> {{ $t('form_title3') }} <span style="color: #22b3c1">{{ $t('form_title4') }}</span>
          </h2>
          <form @submit.prevent="submitForm">
            <div class="row">
              <div class="col-12 col-md-6 mb-4">
                <label for="exampleFormControlInput1" class="form-label">{{ $t('form.name') }}</label>
                <input type="text" v-model="name" class="form-control form-control-lg" id="exampleFormControlInput1"
                  placeholder="Ex. Johm Smithee" required />
              </div>
              <div class="col-12 col-md-6 mb-4">
                <label for="exampleFormControlInput2" class="form-label">{{ $t('form.number') }}</label>
                <input type="text" v-model="phone_number" class="form-control form-control-lg"
                  id="exampleFormControlInput2" placeholder="Ex. +998 91 456 37 73" required />
              </div>
              <div class="col-12 col-md-6 mt-1 mb-4">
                <label for="exampleFormControlInput3" class="form-label">{{ $t('form.guest') }}</label>
                <select class="form-select" v-model="guests" aria-label="Default select example"
                  id="exampleFormControlInput3" required>
                  <option selected disabled value="">ex. 3 or 4 or 5</option>
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="3">4+</option>
                </select>
              </div>
              <div class="col-12 col-md-6 mt-1 mb-4">
                <label for="exampleFormControlInput4" class="form-label">{{ $t('form.date') }}</label>
                <input type="date" v-model="date" required class="form-control form-control-lg" />
              </div>
              <div class="col-12 mt-1 mb-4">
                <label for="exampleFormControlInput5" class="form-label">{{ $t('form.destination') }}</label>
                <select class="form-select form-select-lg" v-model="destination" aria-label="Default select example"
                  id="exampleFormControlInput5" required>
                  <option value="Antalya" selected>Antalya</option>
                  <option value="Istanbul">Istanbul</option>
                  <option value="Dubai">Dubai</option>
                  <option value="Sharm El-Sheikh">Sharm El-Sheikh</option>
                  <option value="Kuala Lumpur">Kuala Lumpur</option>
                  <option value="Canada">Canada</option>
                  <option value="England">England</option>
                </select>
              </div>
              <div class="col-12 mt-1 mb-4">
                <label for="exampleFormControlInput6" class="form-label">{{ $t('form.visa') }}</label>
                <select class="form-select form-select-lg" v-model="visa" aria-label="Default select example"
                  id="exampleFormControlInput6" required>
                  <option value="" selected disabled>Country</option>
                  <option value="USA">USA</option>
                  <option value="Europe">Europe</option>
                  <option value="England">England</option>
                  <option value="Japan">Japan</option>
                  <option value="Oman">Oman</option>
                  <option value="Saudi Arabia">Saudi Arabia</option>
                  <option value="India">India</option>
                  <option value="Hong Kong">Hong Kong</option>
                </select>
              </div>
              <div class="d-grid mt-3">
                <button class="button button-opacity">
                  {{ $t('form.submit') }}
                </button>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
  <!-- Contact End -->

  <!-- Footer Start -->
  <footer class="footer" style="background-image: url(../public/footerBg.jpg)">
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-8 text-center text-md-start">
          <h2>{{ $t('footer_title') }}</h2>
          <h5>{{ $t('footer_desc') }}</h5>
        </div>
        <div
          class="col-12 col-md-4 mt-4 mt-md-0 d-flex justify-content-center justify-content-md-end align-items-center">
          <a href="#contacts">
            <button class="button button-border">{{ $t('footer_btn') }}</button>
          </a>
        </div>
      </div>
    </div>
  </footer>

  <div class="copy" style="padding-top: 25px; padding-bottom: 25px; background-color: #22b3c1">
    <div class="container text-center">
      <p style="padding: 0; margin: 0">
        {{ $t('footer_copy') }}
      </p>
    </div>
  </div>
  <!-- Footer End -->
</template>

<script setup>
import { ref } from "vue";
import axios from "axios";
import { toast } from "vue3-toastify";
import "vue3-toastify/dist/index.css";

const isOpen = ref(false);
const name = ref("");
const phone_number = ref("");
const guests = ref("");
const date = ref("");
const destination = ref("Antalya");
const visa = ref("");
const token = ref("7069003625:AAGAQJns8zC96OqRSQIwC8Ewj1efbWCnIW0");
const chat_id = ref("237282713");

const activeItem = ref("first")

function openMenu() {
  document.querySelector(".header__bars").classList.toggle("header__rotate");
  isOpen.value = !isOpen.value;
}

async function submitForm() {
  try {
    const response = await axios.post(
      `https://api.telegram.org/bot${token.value}/sendMessage`,
      {
        chat_id: chat_id.value,
        text: `Name: ${name.value}\nPhone Number: ${phone_number.value}\nNumber of Guests: ${guests.value}\nDate: ${date.value}\nDestination: ${destination.value}\nVisa Support: ${visa.value}`,
      }
    );
    toast.success("Your Reservation is successfully made!", {
      autoClose: 1000,
      theme: "colored",
    });
    name.value = "";
    phone_number.value = "";
    guests.value = "";
    date.value = "";
    destination.value = "Antalya";
    visa.value = "";
  } catch (error) {
    toast.error(`Your reservation is not made! ${error}`, {
      autoClose: 1000,
      theme: "colored",
    });
  }
}

function changeLang(lang) {
  localStorage.setItem("lang", lang)
}

</script>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

// import required modules
import { Navigation } from "swiper/modules";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>


<style lang="scss">
/* Global Styles */

* {
  margin: 0;
  padding: 0px;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
  scroll-behavior: smooth;
}

body {
  margin: 0;
  padding: 0;
}

a {
  text-decoration: none;
}

ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}

img {
  max-width: 100%;
}

.button {
  background-color: #22b3c1;
  color: #fff;
  border: none;
  border-radius: 50px;
  padding: 12px 35px;
  font-weight: 500;
  transition: all 0.3s ease;

  &:hover {
    color: #22b3c1 !important;
    background-color: #fff !important;
  }
}

.button-opacity {
  &:hover {
    background-color: #22b4c1ca !important;
    color: #fff !important;
  }
}

.button-white {
  background-color: #fff;
  color: #22b3c1;
  transition: all 0.3s ease;

  &:hover {
    background-color: #22b3c1 !important;
    color: #fff !important;
  }
}

.button-border {
  border: 1px solid #fff;
}

/* Header Styles */
.header {
  background-color: #22b3c1;
  padding-top: 15px;
  padding-bottom: 15px;
  position: absolute;
  z-index: 9999;
  width: 100%;
  top: 0px;
  left: 0px;
  position: sticky;

  &__logo {
    width: 159px;
  }

  &__list {
    display: flex;
    justify-content: end;
    align-items: center;
    gap: 50px;
  }

  &__item {
    transition: all 0.2s ease;

    &-active {
      position: relative;

      &::before {
        background-color: #fff;
        left: 0px;
        top: -6px;
        content: "";
        position: absolute;
        width: 20px;
        height: 2px;
        transition: all 0.2s ease;
      }

      &:hover &::before {
        opacity: 0.7;
      }
    }

    &:hover {
      opacity: 0.7;
    }

    a {
      color: #fff;
    }
  }

  &__lang,
  &__social {
    display: flex;
    align-items: center;
    gap: 20px;

    a {
      color: #fff;
    }
  }

  &__lang {
    li {
      a {
        transition: all 0.3s ease;
      }

      &:hover a {
        color: #000;
      }
    }
  }

  &__social {
    i {
      font-size: 18px;
    }
  }

  &__bars {
    display: inline-block;
    cursor: pointer;
  }

  &__bar {
    width: 35px;
    height: 2.5px;
    background-color: #fff;
    margin: 7px 0;
    transition: 0.4s;

    &-first,
    &-third {
      width: 25px;
    }
  }

  &__rotate {
    .header__bar {
      &-first {
        width: 30px;
        transform: translate(0px, 9px) rotate(-45deg);
      }

      &-second {
        opacity: 0;
      }

      &-third {
        width: 30px;
        transform: translate(0px, -10px) rotate(45deg);
      }
    }
  }

  &__mobile {
    position: absolute;
    z-index: 999999;
    top: 66px;
    padding: 20px 0;
    left: 0;
    width: 100%;
    background-color: #f7f7f7;
    margin: 0 auto;
  }

  &__menu {
    li {
      padding: 10px 0;
      width: 100%;
      text-align: center;
      border-bottom: 1px solid #eee;

      i {
        font-size: 18px;
      }

      &:last-child {
        border-bottom: none;
        padding-bottom: 0px;
      }

      a {
        color: #000;
      }

      &:first-child {
        a {
          color: #22b3c1;
        }
      }
    }
  }
}

/* Hero Styles */

.hero {
  &__card {
    background-color: #fff;
    border-radius: 50px;
    width: 100%;
    padding: 25px;
    margin-bottom: 110px;
  }

  &__box {
    text-align: left;

    p {
      color: #afafaf !important;
      margin-bottom: 10px;
    }

    h4 {
      color: #22b3c1 !important;
      font-size: 21px;
      font-weight: 700;
    }
  }

  &__icon {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #22b3c1;
    border-radius: 50px;
    width: 60px;
    height: 60px;

    i {
      font-size: 24px;
      color: #22b3c1 !important;
    }
  }

  &__indicate {
    display: flex;
    flex-direction: column;
    align-items: center;

    p {
      font-size: 20px;
      font-weight: 500;
      color: #fff;
    }
  }

  .carousel-dark .carousel-indicators [data-bs-target] {
    background-color: #fff;
  }

  .carousel-item {
    padding-top: 70px;
    position: relative;
    height: 620px;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    position: relative;

    * {
      z-index: 999;
      color: #fff;
    }

    &::after {
      content: "";
      height: 100%;
      width: 100%;
      background-color: rgba(0, 0, 0, 0.2);
      top: 0px;
      left: 0px;
      position: absolute;
    }

    h2 {
      font-size: 20px;
      margin-bottom: 20px;
    }

    h1 {
      font-weight: 600;
      font-size: 55px;
    }

    &>div {
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }
  }

  .carousel-indicators {
    gap: 20px;

    button {
      width: 180px;
      background-color: #fff;
    }
  }

  &__btn {
    margin-top: 30px;
    margin-bottom: 70px;
  }
}

/* Offer Styles */

.offer {
  padding-top: 80px;
  text-align: center;
  border-bottom: 1px solid #eee;

  .swiper-wrapper {
    padding-bottom: 180px;
  }

  .swiper-button-next,
  .swiper-button-prev {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #22b3c1;
    color: #22b3c1;
    transition: all 0.3s ease;

    &:hover {
      background-color: #22b3c1;
      color: #fff;
    }
  }

  .swiper-button-next {
    transform: translateY(200px) translateX(-580px);
  }

  .swiper-button-prev {
    transform: translateY(200px) translateX(560px);
  }

  .swiper-button-next:after,
  .swiper-button-prev:after {
    font-size: 25px;
  }

  .swiper-slide {
    height: 420px;
    position: relative;
    overflow: hidden;
    display: flex;
    justify-content: start;

    button {
      width: 100%;
      margin-top: 20px;
      font-size: 15px;
    }

    img {
      width: 70%;
      height: 350px;
      object-fit: cover;
      object-position: center;
      border-top-left-radius: 23px;
      border-bottom-left-radius: 23px;
    }
  }

  h2 {
    font-weight: 700;
    margin-bottom: 20px;
  }

  p {
    font-size: 15px;
    line-height: 30px;
    color: #afafaf;
    max-width: 630px;
    margin: 0 auto;
    margin-bottom: 70px;
  }

  &__card {
    text-align: left;
    position: absolute;
    background-color: #fff;
    border-radius: 23px;
    right: 0;
    top: 50%;
    transform: translateY(-45%);
    border: 1px solid #eee;
    padding: 25px;
    width: 280px;

    h4 {
      font-weight: 700;
      font-size: 23px;
    }

    h6 {
      padding-top: 20px;
      border-top: 1px solid #ccc;
      font-weight: 500;
    }
  }

  &__list {
    padding-bottom: 10px;
  }

  &__top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 6px;

    h3 {
      font-weight: 700;
      color: #22b3c1;
      font-size: 20px;
    }
  }

  &__icon {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;

    span,
    i {
      font-size: 15px;
      color: #afafaf;
    }
  }
}

/* Vosa Styles */
.visa {
  padding-top: 80px;
  text-align: center;
  border-bottom: 1px solid #eee;

  .swiper-wrapper {
    padding-bottom: 180px;
  }

  .swiper-button-next,
  .swiper-button-prev {
    width: 50px;
    height: 50px;
    border-radius: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #22b3c1;
    color: #22b3c1;
    transition: all 0.3s ease;

    &:hover {
      background-color: #22b3c1;
      color: #fff;
    }
  }

  .swiper-button-next {
    transform: translateY(200px) translateX(-580px);
  }

  .swiper-button-prev {
    transform: translateY(200px) translateX(560px);
  }

  .swiper-button-next:after,
  .swiper-button-prev:after {
    font-size: 25px;
  }

  .swiper-slide {
    height: 420px;
    position: relative;
    overflow: hidden;
    display: flex;
    justify-content: start;

    button {
      width: 100%;
      margin-top: 20px;
      font-size: 15px;
    }

    img {
      width: 70%;
      height: 350px;
      object-fit: cover;
      object-position: center;
      border-top-left-radius: 23px;
      border-bottom-left-radius: 23px;
    }
  }

  h2 {
    font-weight: 700;
    margin-bottom: 20px;
  }

  p {
    font-size: 15px;
    line-height: 30px;
    color: #afafaf;
    max-width: 630px;
    margin: 0 auto;
    margin-bottom: 70px;
  }

  &__card {
    text-align: left;
    position: absolute;
    background-color: #fff;
    border-radius: 23px;
    right: 0;
    top: 50%;
    transform: translateY(-45%);
    border: 1px solid #eee;
    padding: 25px;
    width: 280px;

    h4 {
      font-weight: 700;
      font-size: 23px;
    }

    h6 {
      padding-top: 20px;
      border-top: 1px solid #ccc;
      font-weight: 500;
    }
  }

  &__list {
    padding-bottom: 10px;
  }

  &__top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 6px;

    h3 {
      font-weight: 700;
      color: #22b3c1;
      font-size: 20px;
    }
  }

  &__icon {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;

    span,
    i {
      font-size: 15px;
      color: #afafaf;
    }
  }
}

/* Explore Styles */

.explore {
  padding-top: 50px;
  padding-bottom: 50px;

  &__title {
    font-weight: 700;
    margin-bottom: 25px;
  }

  &__desc {
    color: #afafaf;
    max-width: 560px;
    margin-bottom: 60px;
    line-height: 2;
  }
}

/* Best Styles */
.best {
  padding-top: 30px;
  padding-bottom: 80px;
  &__flex {
    max-width: 800px;
    display: flex;
    gap: 10px;
    flex-direction: row;
    align-items: stretch;
    overflow: hidden;
    margin: 0 auto;
    margin-top: 60px;
    height: 380px;
  }
  &__item {
    transition: all .3s ease;
    cursor: pointer;
    display: flex;
    justify-content: start;
    align-items: end;
    padding: 15px;
    overflow: hidden;
    border-radius: 30px;
    background-repeat: no-repeat;
    width: 8%;
    position: relative;
    &-active {
      width: 70%;
    }
  }
  &__box {
    width: 40px;
    height: 40px;
    background-color: #fff;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    bottom: 12px;
    left: 12px;
    i {
      color: #22b3c1;
    }
  }
  &__text {
    width: 300px;
    position: absolute;
    left: 65px;
    bottom: 10px;
    * {
      color: #fff;
    }

    h5 {
      font-weight: 600;
      margin-bottom: 3px;
      font-size: 18px;
    }
    p{
      font-size: 14px;
      margin-bottom: 0;
    }
  }
  &__title {
    font-weight: 700;
    margin-bottom: 20px;
  }
  &__desc {
    color: #afafaf;
    max-width: 600px;
    font-size: 14px;
    line-height: 2;
    margin-bottom: 30px;
  }
}

/* Contact Styles */
.contact {
  &__map {
    margin-top: 80px;
    background-color: #f9f9f9;
    border-radius: 23px;
    overflow: hidden;

    iframe {
      width: 100%;
    }
  }

  &__box {
    padding: 50px 100px;

    h2 {
      font-weight: 700;
    }
  }

  form {
    padding-top: 40px;

    label {
      color: #afafaf;
      margin-bottom: 15px;
    }

    input {
      border-radius: 50px;
      font-size: 17px;
    }

    select {
      border-radius: 50px;
      font-size: 17px;
    }
  }
}

/* Box Styles */

.box {
  padding-bottom: 30px;
  border-bottom: 1px solid #eee;

  &:last-child {
    border-bottom: none;
  }

  &__image {
    img {
      border-radius: 23px;
    }
  }

  &__title {
    h5 {
      font-weight: 700;
    }
  }

  &__desc,
  &__info {
    p {
      color: #afafaf;
      font-size: 15px;
      line-height: 30px;
    }
  }

  &__list {
    padding: 15px 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;

    li {
      color: #afafaf;
      display: flex;
      gap: 15px;
      align-items: center;
    }
  }

  &__link {
    display: flex;
    align-items: center;
    margin-top: 18px;
    gap: 10px;

    a {
      font-weight: 500;
      color: #22b3c1;
      transition: all 0.3s ease;
    }

    i {
      color: #22b3c1;
      transition: all 0.3s ease;
    }

    &:hover i {
      margin-left: 10px;
    }
  }
}

/* Reservation Styles */
.reservation {
  padding-top: 250px;
  background-image: url(../public/reservation.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  text-align: center;

  h4,
  h2 {
    color: #fff;
  }

  .hr {
    margin: 0 auto;
    margin-top: 25px;
    margin-bottom: 20px;
    width: 100px;
    border: 1px solid rgba(250, 250, 250, 0.3);
  }

  h2 {
    font-weight: 700;
    font-size: 50px;
    margin-bottom: 30px;
  }

  &__row {
    @media (min-width: 992px) {
      transform: translateY(50%);
    }
  }
}

/* iconbox styles */
.iconbox {
  background-color: #fff;
  border-radius: 23px;
  box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.15);
  text-align: center;
  padding: 30px;

  &__icon {
    margin: 0 auto;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background-color: #f0f0f0;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;

    i {
      font-size: 20px;
      color: #22b3c1;
    }
  }

  h4 {
    color: #000;
    font-weight: 700;
    font-size: 20px;
    margin-bottom: 15px;
  }

  a {
    color: #22b3c1;
  }
}

/* Footer Styles */

.footer {
  padding-top: 70px;
  padding-bottom: 60px;

  h2 {
    font-weight: 700;
    font-size: 35px;
    color: #fff;
    margin-bottom: 15px;
  }

  h5 {
    font-weight: 500;
    color: #fff;
    font-size: 20px;
  }
}

.copy {
  p {
    color: #fff;
    font-size: 15px;
  }
}

/* Media Styles */

@media (max-width: 1400px) {
  .offer {
    .swiper-button-prev {
      transform: translateY(200px) translateX(466px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-500px) !important;
    }
  }

  .visa {
    .swiper-button-prev {
      transform: translateY(200px) translateX(466px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-500px) !important;
    }
  }
}

@media (max-width: 1200px) {
  .offer {
    .swiper-button-prev {
      transform: translateY(200px) translateX(400px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-366px) !important;
    }
  }

  .visa {
    .swiper-button-prev {
      transform: translateY(200px) translateX(400px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-366px) !important;
    }
  }
}

@media (max-width: 992px) {
  .reservation {
    padding-top: 150px;
    padding-bottom: 90px;

    button {
      margin-top: 20px;
      margin-bottom: 60px;
    }
  }

  .contact {
    &__box {
      padding-left: 20px;
      padding-right: 20px;
    }
  }

  .offer {
    .swiper-slide {
      width: 46% !important;
    }

    .swiper-button-prev {
      transform: translateY(200px) translateX(270px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-276px) !important;
    }
  }

  .visa {
    .swiper-slide {
      width: 46% !important;
    }

    .swiper-button-prev {
      transform: translateY(200px) translateX(270px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-276px) !important;
    }
  }
}

@media (max-width: 700px) {
  .hero {
    .carousel-indicators {
      button {
        width: 100px;
      }
    }

    .carousel-item {
      height: auto;
    }
  }

  .carousel-indicators {
    bottom: -20px;
  }
}

@media (max-width: 770px) {
  .offer {
    padding-bottom: 0;

    .swiper-slide {
      width: 100% !important;
    }

    .swiper-button-prev {
      transform: translateY(200px) translateX(170px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-190px) !important;
    }
  }

  .visa {
    padding-bottom: 0;

    .swiper-slide {
      width: 100% !important;
    }

    .swiper-button-prev {
      transform: translateY(200px) translateX(170px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-190px) !important;
    }
  }
  .best {
    &__flex {
      max-width: 100%;
    }
    &__item {
      width: 12%;
      &-active {
        width: calc(100% - 24%);
      }
    }
  }
}

@media (max-width: 560px) {
  .reservation {
    padding-top: 80px;

    h2 {
      font-size: 30px;
    }

    h4 {
      font-size: 18px;
    }
  }

  .button {
    font-size: 14px;
    padding: 12px 20px;
  }

  .hero {
    .carousel-indicators {
      button {
        width: 60px;
      }
    }

    .col-6 {
      gap: 10px !important;
    }

    &__icon {
      width: 40px;
      height: 40px;
    }

    .carousel-item {
      h2 {
        font-size: 16px;
      }

      h1 {
        font-size: 40px;
      }
    }

    &__icon {
      i {
        font-size: 20px;
      }

      padding: 0;
      border: none;
    }

    &__box {
      h4 {
        font-size: 16px;
      }

      p {
        font-size: 14px;
      }
    }
  }

  .box {
    &__list {
      flex-direction: column;
      align-items: baseline;
      gap: 10px;
      margin: 0px;
    }
  }

  .contact {
    padding-top: 0px !important;

    iframe {
      height: 300px;
    }
  }

  .footer {
    h2 {
      font-size: 25px;
    }

    h5 {
      font-size: 14px;
    }
  }
}

@media (max-width: 530px) {
  .offer {
    .swiper-button-prev {
      transform: translateY(200px) translateX(80px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-90px) !important;
    }
  }

  .visa {
    .swiper-button-prev {
      transform: translateY(200px) translateX(80px) !important;
    }

    .swiper-button-next {
      transform: translateY(200px) translateX(-90px) !important;
    }
  }

  .best {
    &__item {
      width: 20%;
      &-active {
        width: calc(100% - 40%);
      }
    }
  }

}
</style>