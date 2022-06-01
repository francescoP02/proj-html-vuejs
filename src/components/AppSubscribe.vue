<template>
  <div class="ms-subscribe">

      <div class="container d-flex">
          <div class="ms-text d-flex">
              <i class="far fa-envelope d-flex"></i>
              <h4>Subscribe now and get special offers</h4>
          </div>

          <div>

            <form class="row g-3">
                <div class="col-auto">
                    <label for="inputEmail" class="visually-hidden">Email</label>
                    <input type="email" class="form-control rounded-pill" id="inputEmail" placeholder="Insert your email">
                </div>
                <div class="col-auto">
                    <button type="submit" class="btn ms-btn mb-3 rounded-pill px-5">SEND</button>
                </div>
            </form>

          </div>
      </div>
      
  </div>
</template>

<script>

export default {
  name: 'AppSubscribe',
}
</script>

<style scoped lang="scss">
@import "../style/common.scss";
@import "../style/variables.scss";

.ms-subscribe {
    background-color: #303337;
    color: #ffffff;
    padding: 4rem 0;

    .container {
        justify-content: space-around;

        .ms-text {

            align-items: center;

            h4 {
                font-weight: 700;
            }

            i {
                padding: 1rem;
                font-size: 1.5rem;
                color: #73797e;
                border-radius: 50%;
                background-color: #2b2e32;
                margin-right: 2rem;
            }

            .fa-envelope:before {
                align-self: center;
            }
        }

        .ms-btn {
            background-color: #427ed1;
            color: #ffffff;
            font-weight: 500;

            &:hover {
                background-color: $btn-header-hover;
            }
        }
    }
}

</style>