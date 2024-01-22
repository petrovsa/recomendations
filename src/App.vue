<template>
  <div class="recomendations">
    <div class="recomendations__header">
      <h2 class="recomendations__title">Персональні рекомендації</h2>
      <div class="recomendations__navarrows">
        <div class="arrow arrow--left">
          <img src="./assets/Icon.png" alt="icon" />
        </div>
        <div class="arrow arrow--right">
          <img src="./assets/Icon.png" alt="icon" />
        </div>
      </div>
    </div>
    <div class="recomendations__container">
      <div class="recomended-products">
        <div
          v-for="book in booksList"
          :key="book.id"
          class="recomended-products__item product-item"
        >
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" :src="book.imgUrl" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              {{ book.name }}
            </div>
            <div class="product-item__autor">
              <a :href="book.autor.autorUrl">
                {{ book.autor.autor }}
              </a>
            </div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">{{ book.ratingLabel }}</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div v-if="book.oldPrice" class="product-item__price">
              {{ book.oldPrice }} <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__price">
              {{ book.price }} <span class="product-item__curency">₴</span>
            </div>
            <div v-if="book.inStock" class="product-item__status">
              В наявності
            </div>
            <div
              v-else
              class="product-item__status product-item__status--outstock"
            >
              Немає В наявності
            </div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
        <div class="recomended-products__item product-item">
          <img class="product-item__label" src="./assets/label.png" alt="" />
          <button class="btn product-item__wishlist">
            <img src="./assets/wishlist.png" alt="" />
          </button>
          <button class="btn product-item__cart">
            <img src="./assets/cart.png" alt="" />
          </button>
          <div class="product-item__imgblock">
            <img class="product-item__img" src="./assets/book.jpg" alt="" />
          </div>
          <div class="product-item__text">
            <div class="product-item__name">
              Вавилон. Прихована історія, історія людства. Частина 1
            </div>
            <div class="product-item__autor">Ребекка Кван</div>
            <div class="product-item__rating rating">
              <div class="rating-starslist">
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
                <div class="rating-star">
                  <img src="./assets/star.jpg" alt="star" />
                </div>
              </div>
              <div class="rating-value">493</div>
            </div>
          </div>
          <div class="product-item__avialability">
            <div class="product-item__price">
              489 <span class="product-item__curency">₴</span>
            </div>
            <div class="product-item__status">В наявності</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",

  data () {
    return {
      booksList: [
        {
          id: 1,
          name: "Вавилон. Прихована історія, історія людства. Частина 1",
          imgUrl: "./assets/book.jpg",
          autor: {
            autor: "Ребекка Кван",
            autorUrl: "#",
          },
          price: 489,
          oldPrice: null,
          ratingLabel: 453,
          wishlistStatus: false,
          inStock: true,
        },
        {
          id: 2,
          name: "Довбуш. Гідність або забуття",
          imgUrl: "./assets/book.jpg",
          autor: {
            autor: "Аґата Крісті",
            autorUrl: "#",
          },
          price: 238,
          oldPrice: null,
          ratingLabel: 43,
          wishlistStatus: false,
          inStock: true,
  },
  {
   'id': 3,
   'name': 'Фриланс здорової людини. Як працювати з задоволенням',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Т. Гонченко',
      'autorUrl': '# '
    },
   'price': 220,
   'oldPrice': null,
   'ratingLabel': 5,
   'wishlistStatus': fasle,
   'inStock': true
  },
  {
    'id': 4,
   'name': 'Забуте вбивство',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Аґата Крісті',
      'autorUrl': '# '
    },
   'price': 230,
   'oldPrice': null,
   'ratingLabel': 545,
   'wishlistStatus': fasle,
   'inStock': true
  },
  {
    'id': 5,
   'name': 'Чому нації занепадають. Походження влади, багатства і бідності',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Д. Аджемоґлу, Дж. Робінсон',
      'autorUrl': '# '
    },
   'price': 350,
   'oldPrice': 420,
   'ratingLabel': 41,
   'wishlistStatus': fasle,
   'inStock': true
  },
  {
    'id': 6,
   'name': 'Rework. Ця книжка змінить ваш погляд на бізнес',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Джейсон Фрайд, Девід Хайне',
      'autorUrl': '# '
    },
   'price': 290,
   'oldPrice': null,
   'ratingLabel': 578,
   'wishlistStatus': true,
   'inStock': true
  },
  {
    'id': 7,
   'name': 'Вавилон. Прихована історія, історія людства. Частина 1',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Ребекка Кван',
      'autorUrl': '# '
    },
   'price': 489,
   'oldPrice': null,
   'ratingLabel': 453,
   'wishlistStatus': fasle,
   'inStock': false
  },
  {
    'id': 0,
   'name': 'Вавилон. Прихована історія, історія людства. Частина 1',
   'imgUrl': './assets/book.jpg',
   'autor': {
      'autor': 'Ребекка Кван',
      'autorUrl': '# '
    },
   'price': 489,
   'oldPrice': null,
   'ratingLabel': 453,
   'wishlistStatus': fasle,
   'inStock': true
  }
]
    };
  }
};
</script>

<style lang="scss">
.recomendations {
  display: flex;
  flex-direction: column;
  margin: 0 auto;
  min-width: 270px;
  max-width: 1700px;
  padding: 0 20px;

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0;

    @media screen and (min-width: 768px) {
      font-size: 28px;
      line-height: 38px;
    }
  }

  &__title {
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
    font-size: 22px;
    line-height: 30px;
    font-weight: 500;

    @media screen and (min-width: 768px) {
      font-size: 28px;
      line-height: 38px;
    }
  }

  .recomended-products {
    display: flex;
    gap: 40px;

    &__item.product-item {
      display: flex;
      flex-direction: column;
      gap: 13px;
    }

    .product-item {
      position: relative;
      width: 100%;

      @media screen and (min-width: 768px) {
        min-width: 254px;
      }

      &:last-child {
        &::after {
          display: none;
        }
      }

      &::after {
        position: absolute;
        content: "";
        width: 1px;
        height: 100%;
        background-color: #d6d6d6;
        top: 0;
        right: -20px;
      }

      &__imgblock {
        align-self: center;
        padding: 13px 0;

        img {
          width: 140px;
          height: 215px;

          @media screen and (min-width: 768px) {
            width: 176px;
            height: 269px;
          }
        }

        &:last-child {
          border-right: none;
        }
      }

      &__text {
        display: flex;
        flex-direction: column;
        gap: 10px;
      }

      &__name,
      &__autor {
        font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
        font-size: 14px;
        line-height: 22px;
        font-weight: 500;

        @media screen and (min-width: 768px) {
          font-size: 16px;
          line-height: 26px;
        }
      }

      &__autor {
        color: #707070;
      }

      &__rating.rating {
        display: flex;
        align-items: center;
        gap: 10px;

        .rating-starslist {
          display: flex;
        }

        .rating-value {
          font-size: 14px;
          line-height: 16px;
          color: #d6d6d6;
        }
      }

      &__avialability {
        height: 92px;
        display: flex;
        flex-direction: column;
        justify-content: end;
      }

      &__price {
        font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
        font-size: 26px;
        line-height: 28px;
      }

      &__curency {
        font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
        font-size: 20px;
        line-height: 25px;
      }

      &__status {
        font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
        font-size: 14px;
        line-height: 16px;
        color: #4c4c4d;
      }

      &__label {
        display: none;
        position: absolute;
        z-index: 10;
        top: 0;
        left: 0;

        @media (min-width: 769px) and (max-width: 1025px) {
          display: block;
        }
      }

      .btn {
        background: none;
        border: none;
      }

      &__wishlist,
      &__cart {
        position: absolute;
        cursor: pointer;
        right: 0;

        @media (min-width: 468px) {
          display: none;
        }
      }

      &__wishlist {
        padding: 13px 0 0 0;
        top: 0;
      }

      &__cart {
        padding: 0;
        bottom: 0;
      }
    }
  }

  &__container {
    overflow-x: scroll;
    margin: 0 auto;
    width: 100%;
    padding-bottom: 13px;
  }

  &__navarrows {
    display: none;
    align-items: center;
    justify-content: center;
    gap: 15px;

    @media screen and (min-width: 768px) {
      display: flex;
    }

    .arrow {
      display: flex;

      &--right {
        transform: rotate(180deg);
      }
    }
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
