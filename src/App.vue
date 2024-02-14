<template>
  <TheHeader />
  <SideMenu />
  <CatalogProducts :productsList="booksList" class="home-page__products" />
  <TheSlider sliderName="Персональні рекомендації">
    <RecomendedProducts :recomendedList="recomendedList" />
  </TheSlider>
  <ContentText />
</template>

<script>
import TheHeader from '@/components/TheHeader/TheHeader';
import SideMenu from "@/components/SideMenu/SideMenu.vue";
import TheSlider from '@/components/TheSlider/TheSlider';
import CatalogProducts from '@/components/CatalogProducts/CatalogProducts';
import RecomendedProducts from '@/components/RecomendedBlock/RecomendedProducts';
import ContentText from "@/components/ContentText/ContentText";


export default {
  name: "App",

  components: {
    SideMenu,
    TheHeader,
    TheSlider,
    RecomendedProducts,
    CatalogProducts,
    ContentText
  },

  data() {
    return {
      booksList: [
        {
          id: 1,
          name: "Вавилон. Прихована історія, історія людства. Частина 1",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Ребекка Кван",
            autorUrl: "#",
          },
          price: 489,
          oldPrice: null,
          ratingLabel: 453,
          wishlistStatus: false,
          inStock: true,
          inWishlist: true,
          recomended: true,
          label: {
            name: 'top',
            value: 'ТОП'
          },
          stars: 4,
        },
        {
          id: 2,
          name: "Довбуш. Гідність або забуття",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Аґата Крісті",
            autorUrl: "#",
          },
          price: 238,
          oldPrice: null,
          ratingLabel: 43,
          wishlistStatus: false,
          inStock: true,
          inWishlist: false,
          recomended: true,
          stars: 2,
          label: {
            name: 'new',
            value: 'NEW'
          }
        },
        {
          id: 3,
          name: "Фриланс здорової людини. Як працювати з задоволенням",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Т. Гонченко",
            autorUrl: "#",
          },
          price: 220,
          oldPrice: null,
          ratingLabel: 5,
          wishlistStatus: false,
          inStock: true,
          inWishlist: false,
          recomended: true,
          stars: 5,
        },
        {
          id: 4,
          name: "Забуте вбивство",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Аґата Крісті",
            autorUrl: "#",
          },
          price: 230,
          oldPrice: null,
          ratingLabel: 545,
          wishlistStatus: false,
          inStock: true,
          inWishlist: false,
          recomended: true,
          stars: 3,
          label: {
            name: 'promo',
            value: 'АКЦІЯ'
          }
        },
        {
          id: 5,
          name: "Чому нації занепадають. Походження влади, багатства і бідності",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Д. Аджемоґлу, Дж. Робінсон",
            autorUrl: "#",
          },
          price: 350,
          oldPrice: 420,
          ratingLabel: 41,
          wishlistStatus: false,
          inStock: true,
          inWishlist: false,
          recomended: true,
          stars: 4,
        },
        {
          id: 6,
          name: "Rework. Ця книжка змінить ваш погляд на бізнес",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Джейсон Фрайд, Девід Хайне",
            autorUrl: "#",
          },
          price: 290,
          oldPrice: null,
          ratingLabel: 578,
          wishlistStatus: true,
          inStock: true,
          inWishlist: false,
          recomended: true,
          stars: 2,
        },
        {
          id: 7,
          name: "Вавилон. Прихована історія, історія людства. Частина 1",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Ребекка Кван",
            autorUrl: "#",
          },
          price: 489,
          oldPrice: null,
          ratingLabel: 453,
          wishlistStatus: false,
          inStock: false,
          inWishlist: false,
          recomended: true,
          stars: 1,
        },
        {
          id: 8,
          name: "Вавилон. Прихована історія, історія людства. Частина 1",
          imgUrl: require("./assets/book.jpg"),
          autor: {
            autor: "Ребекка Кван",
            autorUrl: "#",
          },
          price: 489,
          oldPrice: null,
          ratingLabel: 453,
          wishlistStatus: false,
          inStock: true,
          inWishlist: false,
          recomended: false,
          stars: 2,
        }
      ]
    };
  },

  computed: {
    recomendedList () {
      return this.booksList.filter(book => book.recomended)
    }
  }
};
</script>

<style lang="scss">

body {
  color: $black-1000;
  margin: 0;
  font: 16px/26px Arial, serif;
}

.container {
  max-width: 1600px;
  margin: 0 auto;
  padding-left: 10px;
  padding-right: 10px;
}

.home-page {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 1600px;
  margin: 0 auto;
  padding-left: 10px;
  padding-right: 10px;

  &__products {
    margin: 0 auto;
  }
}

/* width */
::-webkit-scrollbar {
  height: 4px;
}

/* Track */
::-webkit-scrollbar-track {
  background-color: #d6d6d6;
  box-shadow: inset 0 0 5px grey;
  border-radius: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background-color: #8f8f8f;
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: black;
}
</style>
