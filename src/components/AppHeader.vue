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
            <li v-for="(item, index) in menuBar" :key="index" @click="clickedItem(index)" :class="{active : index === currentItem}"> {{item.name}} </li>
          </ul>
        </div>
      </section>

      <section class="ms-h-bottom">

      </section>
  </div>
</template>

<script>

export default {
  name: 'AppHeader',
  data: function() {
    return {
      currentItem: 0,
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
        },
        {
          name: "My Account",
          active: false,
        },
        {
          name: "CART",
          active: false,
        },
      ],
    }
  },
  methods: {
      clickedItem : function(index) {
        this.currentItem = index;
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
    }

    .active {
      background-color: #fafafa;
    }
  }


}


</style>