<template>
  <div class="secondslide">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path
        fill="#E56768"
        fill-opacity="1"
        d="M0,160L288,96L576,192L864,256L1152,96L1440,224L1440,320L1152,320L864,320L576,320L288,320L0,320Z"
      ></path>
    </svg>
    <div class="tabs">
      <div class="universitytab">
        <img src="..\assets\img\Clock-and-Bell.png" alt="" />
        <h1>University Year</h1>
      </div>
      <div class="diagram">
        <div class="text primo d-flex justify-content-center">
          <div class="firsttext">
            <h5>Demo Classes</h5>

            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Soluta,
              at!
            </p>
          </div>
          <div class="secondtext">
            <h5>Graduation Day</h5>

            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Soluta,
              at!
            </p>
          </div>
        </div>
        <img src="..\assets\img\Timeline-Item.png" alt="" />
        <div class="text secondo d-flex justify-content-center">
          <div class="firsttext">
            <h5>Orientation</h5>

            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Soluta,
              at!
            </p>
          </div>
          <div class="secondtext">
            <h5>Evaluation</h5>

            <p>
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Soluta,
              at!
            </p>
          </div>
        </div>
      </div>
      <div class="eventstab">
        <img src="..\assets\img\upcoming-events-calendar-icon.png" alt="" />
        <h1>Upcoming Events</h1>
        <div class="cell">
          <div class="card">
            <div class="card-body">
              <h5 class="card-title">Coaching Session</h5>
              <div class="card-date">
                <i class="bi bi-calendar3"></i>24 Mar 18:00 PM
              </div>
              <p class="card-text">
                With supporting text below as a natural lead-in to additional
                content.
              </p>
              <a href="#" class="btn btn-primary"
                ><i class="bi bi-plus-lg"></i>Find More</a
              >
            </div>
          </div>
          <div class="card">
            <div class="card-body">
              <h5 class="card-title">Coaching Session</h5>
              <div class="card-date">
                <i class="bi bi-calendar3"></i>24 Mar 18:00 PM
              </div>
              <p class="card-text">
                With supporting text below as a natural lead-in to additional
                content.
              </p>
              <a href="#" class="btn btn-primary"
                ><i class="bi bi-plus-lg"></i>Find More</a
              >
            </div>
          </div>
          <div class="card">
            <div class="card-body">
              <h5 class="card-title">Coaching Session</h5>
              <div class="card-date">
                <i class="bi bi-calendar3"></i>24 Mar 18:00 PM
              </div>
              <p class="card-text">
                With supporting text below as a natural lead-in to additional
                content.
              </p>
              <a href="#" class="btn btn-primary"
                ><i class="bi bi-plus-lg"></i>Find More</a
              >
            </div>
          </div>
        </div>
      </div>
      <b-button class="btnsearch" pill>
        <i class="bi bi-search"></i> View all Events
      </b-button>
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
      <path
        fill="#E56768"
        fill-opacity="1"
        d="M0,160L288,96L576,192L864,256L1152,96L1440,224L1440,0L1152,0L864,0L576,0L288,0L0,0Z"
      ></path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "Secondslide",
  data() {
    return {};
  },
};
</script>

<style scoped lang="scss">
@import "@/style/common.scss";
.tabs {
  background-color: #e56768;
  height: 1400px;
  width: 100%;
}
.card-date {
  font-size: 15px;
  font-family: "Courier New", Courier, monospace;
}
.cell {
  display: flex;
  justify-content: center;
  .card {
    margin: 20px;
    border-radius: 25px;
    max-width: 350px;
    max-height: 200px;
    box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
    p {
      color: $gray-600;
    }
    .btn {
      margin-top: 40px;
      height: 50px;
      border-radius: 25px;

      vertical-align: middle;
      padding: 16px 43px !important;
      background-color: #e56768;
      box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
      border: 0px;
      &:hover {
        background-color: #e9d758;
      }
    }
  }
}
.btnsearch {
  margin-top: 150px;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
  height: 70px;
  text-align: center;
  vertical-align: middle;
  border: 0px;
  background: #e9d758;
  padding: 16px 43px !important;
  border-radius: 50px;
  text-transform: uppercase !important;
  margin-left: 20px;
  letter-spacing: 0.5px;
  color: white;
  background-color: #e9d758;
  color: #fff;
  transition: all 300ms ease;
  -webkit-transition: all 300ms ease;
  &:hover {
    background-color: #e56768;
  }
}

.universitytab,
.eventstab {
  img {
    height: 100px;
    width: 100px;
  }
  h1 {
    color: white;
    font-size: 60px;
  }
}
.diagram {
  height: 400px;
  width: 100%;
  margin-top: 150px;
  .primo {
    margin-left: 250px;
  }
  .secondo {
    margin-right: 150px;
  }
  .text {
    color: white;

    .firsttext {
      max-width: 340px;
    }
    .secondtext {
      max-width: 340px;
      margin-left: 80px;
    }
    p {
      font-size: 13px;
      color: lightgrey;
    }
  }
}
</style>