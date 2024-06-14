<template>
  <div>
    <header class="header_area" style="position: fixed;">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <!-- Brand and toggle get grouped for better mobile display -->
          <a class="navbar-brand logo_h" href="/"><img src="image/Logo.png" alt=""></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <!-- Collect the nav links, forms, and other content for toggling -->
          <div class="collapse navbar-collapse offset" id="navbarSupportedContent">
            <ul class="nav navbar-nav menu_nav desktop-only">
              <li class="nav-item"><router-link to="/" class="nav-link">Home</router-link></li>
              <li class="nav-item"><router-link to="/" class="nav-link">RoomBooking</router-link></li>
              <li class="nav-item"><router-link to="/check" class="nav-link">Check Booking</router-link></li>
              <li class="nav-item"><router-link to="/feedback" class="nav-link">Feedback</router-link></li>
              <li class="nav-item" @click="logout" v-if="role === 'guest'"><router-link to="" class="nav-link">LogOut</router-link></li>
              <li class="nav-item" v-else><router-link to="/login" class="nav-link">Login</router-link></li>
              <li class="nav-item" @click="checkHistory"><router-link to="" class="nav-link">History</router-link></li>
              <li class="nav-item"><router-link to="/position" class="nav-link">Position</router-link></li>
              <li class="nav-item active"><router-link to="/DetailRoom" class="nav-link">DetailRoom</router-link></li>
            </ul>
          </div>
        </nav>
      </div>
    </header>

    <div class="container main-content">
      <header>
        <div class="header-section">
          <div class="date-info">
            <p>{{ dateInfo }}</p>
          </div>
          <div class="divider"></div>
          <div class="room-info">
            <p>{{ roomInfo }}</p>
          </div>
        </div>
        <button class="edit-button">EDIT</button>
      </header>
      <main>
        <div class="room-detail">
          <h2>SUITE ROOM</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/is/image/marriotts7prod/si-sgnsi-club-studio-kitchen-13487-22034:Classic-Hor?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <p class="price-type">Flexible Member Price</p>
                <p class="price">3,410,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
              <hr class="divider-line">
              <div class="price-item">
                <p class="price-type">Flexible Price</p>
                <p class="price">3,680,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <div class="container main-content">
      <main>
        <div class="room-detail">
          <h2>DELUXE ROOM</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/content/dam/marriott-renditions/SGNSI/sgnsi-king-suitebedroom-4648-hor-clsc.jpg?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <p class="price-type">Flexible Member Price</p>
                <p class="price">4,410,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
              <hr class="divider-line">
              <div class="price-item">
                <p class="price-type">Flexible Price</p>
                <p class="price">4,680,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <div class="container main-content">
      <main>
        <div class="room-detail">
          <h2>VIP ROOM</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/is/image/marriotts7prod/si-sgnsi-studio-twin-27424:Classic-Hor?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <p class="price-type">Flexible Member Price</p>
                <p class="price">5,410,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
              <hr class="divider-line">
              <div class="price-item">
                <p class="price-type">Flexible Price</p>
                <p class="price">5,680,000 VND / night</p>
                <p class="rate-details">Rate Details</p>
                <button class="select-button">SELECT</button>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <!--================ start footer Area  =================-->
    <footer class="footer-area section_gap">
      <div class="container">
        <div class="border_line"></div>
        <div class="row footer-bottom d-flex justify-content-between align-items-center">
          <p class="col-lg-8 col-sm-12 footer-text m-0">
            <!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
            Copyright &copy;2024 All rights reserved | This template is made with <i class="fa fa-heart-o"
              aria-hidden="true"></i> by <a href="https://www.facebook.com/dammanhluu3241" target="_blank">Dam Manh Luu</a>
            <!-- Link back to Colorlib can't be removed. Template is licensed under CC BY 3.0. -->
          </p>
          <div class="col-lg-4 col-sm-12 footer-social">
            <a href="#"><i class="fa fa-facebook"></i></a>
            <a href="#"><i class="fa fa-twitter"></i></a>
            <a href="#"><i class="fa fa-dribbble"></i></a>
            <a href="#"><i class="fa fa-behance"></i></a>
          </div>
        </div>
      </div>
    </footer>
    <!--================ End footer Area  =================-->
  </div>
</template>

<script>
export default {
  name: 'DetailRoomComponent',
  data() {
    return {
      dateInfo: 'Tuesday, June 25, 2024 - Wednesday, June 26, 2024',
      roomInfo: '1 Room: 2 Adults',
      role: 'guest' // or 'tamu'
    };
  },
  methods: {
    logout() {
      // Your logout method here
    },
    checkHistory() {
      // Your check history method here
    }
  }
};
</script>

<style scoped>
.container {
  font-family: Arial, sans-serif;
}

.header_area {
  width: 100%;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  background: #fff;
  border-bottom: 1px solid #ddd;
}

.main-content {
  padding-top: 120px; /* Adjust the padding value to match the height of your fixed header */
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f3f3f3;
  border-bottom: 1px solid #ddd;
  margin-bottom: 20px; /* Add margin bottom to create space between header and main content */
}

.header-section {
  display: flex;
  align-items: center;
}

.date-info, .room-info {
  font-size: 14px;
}

.divider {
  width: 1px;
  height: 40px;
  background-color: #ddd;
  margin: 0 20px;
}

.edit-button {
  padding: 10px 20px;
  background-color: #fff;
  color: #000;
  border: 1px solid #ddd;
  border-radius: 5px;
  cursor: pointer;
}

.edit-button:hover {
  background-color: #f0f0f0;
}

main {
  padding: 20px;
  background-color: #fafafa;
}

.room-detail {
  background-color: #fff;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.room-content {
  display: flex;
  align-items: center;
}

.room-image {
  width: 50%;
  height: auto;
  margin-right: 20px;
}

.price-info {
  width: 50%;
}

.price-item {
  text-align: left;
  padding: 10px 0;
}

.price-type {
  font-weight: bold;
  margin-bottom: 5px;
}

.price {
  color: #d9534f;
  font-size: 18px;
  margin-bottom: 5px;
}

.rate-details {
  color: #5a5a5a;
  margin-bottom: 10px;
}

.select-button {
  padding: 10px 20px;
  background-color: #000;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.select-button:hover {
  background-color: #333;
}

.divider-line {
  border: 0;
  height: 1px;
  background: #ddd;
  margin: 20px 0;
}

.footer-area {
  background: #f9f9ff;
  padding: 30px 0;
  font-size: 14px;
}

.footer-bottom {
  padding: 10px 0;
  border-top: 1px solid #eee;
}

.footer-text {
  margin: 0;
}

.footer-social a {
  margin-right: 15px;
  color: #333;
}

.footer-social a:hover {
  color: #007bff;
}
</style>
