<template>
  <div class="container">
      <div class="ms-title d-flex">
        <span class="align-self-center"></span>
        <h2>From Our Blog</h2>
        <span class="align-self-center"></span>
      </div>
      <span>The latest Classic Shop news</span>

      <ul class="d-flex row row-cols-3">
            <li v-for="(item, index) in blog" :key="index">
                <ul class="ms-card d-flex">
                    <li><img :src="require(`../assets/img/${item.img}`)" alt=""></li>
                    <li><h5>{{item.title}}</h5></li>
                    <li><span>{{item.date}} | {{item.comments}} comments</span></li>
                    <li><p>{{item.description}}</p></li>
                </ul>
            </li>
      </ul>


  </div>
</template>

<script>

export default {
  name: 'AppBlog',
  data: function() {
      return {
          blog: [
                {
                  img: "post_img_12-700x441.jpg",
                  title: "Aenen lobortis sapien enim viverra",
                  date: "September 9th,2015",
                  comments: "0",
                  description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
                },
                {
                  img: "post_img_11-700x441.jpg",
                  title: "Duis ac massa semper maximus",
                  date: "September 9th,2015",
                  comments: "0",
                  description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
                },
                {
                  img: "post_img_10-700x441.jpg",
                  title: "Nunc fermint nulla eu justo sem id",
                  date: "September 9th,2015",
                  comments: "0",
                  description: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
                },
          ]
      }
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
}

div {
    text-align: center;
    margin-top: 8rem;
    padding-bottom: 2rem;

    .ms-title {
        h2 {
            width: 40%;
        }
        span {
            height: 2px;
            background-color: #f1f1f1;
            width: calc((100% - 40%)/2 );
        }
    }

    ul {
        padding: 0;
        
        .ms-card {
            flex-direction: column;
            text-align: left;
            padding-top: 3rem;

            h5 {
                padding-top: 1rem;
            }

            span {
                font-size: .8rem;
                color: gray;
            }

            p {
                color: gray;
                font-size: .9rem;
                padding-top: 1rem;
            }

            img {
                width: 100%;
            }
        }
    }


}

</style>