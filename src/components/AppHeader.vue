<template>
  <div>
      <section class="ms-h-top d-flex">
        <div>
          <ul class="ms-social d-flex">
            <li class="align-items-center" v-for="(item, index) in iconSocial" :key="index"><i class="fab" :class="item.icon"></i></li>
          </ul>
        </div>
        <div>
          <ul class="ms-menubar">
            <li v-for="(item, index) in menuBar" :key="index" @click="clickedItem(index)" :class="{active : index === currentItem}"> <span v-if="item.cart === true"><i class="fas fa-shopping-cart"></i></span> {{item.name}} <span v-if="item.dropdown === true"><i class="fas fa-caret-down"></i></span> </li>
          </ul>
        </div>
      </section>

      <section class="ms-h-bottom d-flex justify-content-around">
        <div class="d-flex align-items-center">
          <img src="../assets/img/classic_shop_logo1x.png" alt="">
        </div>

        <div class="ms-navbar d-flex align-items-center">
          <ul>
            <li v-for="(item, index) in menuNav" :key="index" @click="clickedItemMenu(index)" :class="{active : index === currentNavItem}"> {{item.name}} <span v-if="item.dropdown === true"><i class="fas fa-caret-down"></i></span> </li>
          </ul>

          <button class="btn ms-btn rounded-pill mx-4" type="submit">SHOP NOW!</button>

          <span><i class="fas fa-search"></i></span>
        </div>
      </section>
  </div>
</template>

<script>

export default {
  name: 'AppHeader',
  data: function() {
    return {
      currentItem: 0,
      currentNavItem: 0,
      iconSocial: [
        {
          name: "Facebook",
          icon: "fa-facebook-f",
        },
        {
          name: "Twitter",
          icon: "fa-twitter",
        },
        {
          name: "Instragram",
          icon: "fa-instagram",
        },
        {
          name: "Youtube",
          icon: "fa-youtube",
        },
      ],

      menuBar: [
        {
          name: "Shopping Cart",
          active: false,
          dropdown: false,
          cart: false,
        },
        {
          name: "My Account",
          active: false,
          dropdown: true,
          cart: false,
        },
        {
          name: "CART",
          active: false,
          dropdown: true,
          cart: true,
        },
      ],

      menuNav: [
        {
          name: "Home",
          active: false,
          dropdown: true,
        },
        {
          name: "Shop",
          active: false,
          dropdown: true,
        },
        {
          name: "Product",
          active: false,
          dropdown: true,
        },
        {
          name: "Categories",
          active: false,
          dropdown: true,
        },
        {
          name: "News",
          active: false,
          dropdown: false,
        },
        {
          name: "Elements",
          active: false,
          dropdown: true,
        },
      ]
    }
  },
  methods: {
      clickedItem : function(index) {
        this.currentItem = index;
      },

      clickedItemMenu : function(index) {
        this.currentNavItem = index;
      },
  },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

ul {
  list-style: none;
}

li {
  display: inline-block;
  padding: 0 .5rem;
}

.ms-h-top {
  height: 60px;
  justify-content: space-around;
  border-bottom: 3px solid #fafafa;

  .ms-social {
    align-items: center;
    height: 100%;
    li {
      margin-left: .5rem;
      cursor: pointer;
    }
  }

  .ms-menubar {

    height: 100%;

    li {
      border-right: 2px solid #f1f1f1;
      height: 100%;
      line-height: 60px;
      cursor: pointer;
      
      span {
        margin: 0 .3rem;
      }
    }

    .active {
      background-color: #fafafa;
    }
  }

}

.ms-h-bottom {

  height: 100px;
  width: 100%;
  border-bottom: 3px solid #fafafa;

  .ms-navbar {

    height: 100%;

    ul {
      margin-bottom: 0rem;
      height: 100%;

      li {
      height: 100%;
      cursor: pointer;
      line-height: 97px;
      margin: 0 .5rem;
      }

      .active {
        color: #5a98d8;
        border-top: 3px solid #5a98d8;
      }
    }

    .ms-btn {
    color: #ffffff;
    background-color: $btn-header;
    border: 0px;
    height: 50%;

      &:hover {
        background-color: $btn-header-hover;
      }
    }

    span {
      cursor: pointer;
    }
  }

}


</style>