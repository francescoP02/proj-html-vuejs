<template>
  <div class="ms-collection d-flex row row-cols-3">
    <div class="ms-card" v-for="(item, index) in collectionCard" :key="index">
        <img :src="require(`../assets/img/${item.img}`)" alt="">
        <div class="ms-text-card">
            <h2>{{item.name}}</h2>
            <span>{{item.description}}</span>
            <button type="button" class="btn btn-outline-light rounded-pill">VIEW MORE</button>
        </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'AppCollection',
  data: function() {
      return {
          collectionCard: [
              {
                img: "winter_collection_bg.jpg",
                name: "Winter Collection",
                description: "STYLISC AND WARM",
              },
                {
                img: "spring_collection_bg.jpg",
                name: "Spring Collection",
                description: "BRIGHT AND COLORFUL",
              },
                {
                img: "autumn_collection_bg.jpg",
                name: "Autumn Collection",
                description: "RICH AND COMFORTABLE",
              },
          ]
      }
  },
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-collection {

    margin-top: 10rem;

    .ms-card {
        padding: 0;
        position: relative;

        img {
        width: 100%;
        }

        .ms-text-card {
            position: absolute;
            top: 70%;
            left: 50%;
            transform: translate(-50%,-50%);
            color: #ffffff;
            text-align: center;

            span {
                display: block;
                margin: 1rem 0;
            }
        }
    }
}

</style>