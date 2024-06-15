<template>
  <div>
    <header class="header_area" style="position: fixed;">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <a class="navbar-brand logo_h" href="/"><img src="image/Logo.png" alt=""></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <div class="collapse navbar-collapse offset" id="navbarSupportedContent">
            <ul class="nav navbar-nav menu_nav desktop-only">
              <li class="nav-item"><router-link to="/" class="nav-link">Home</router-link></li>
              <li class="nav-item"><router-link to="/" class="nav-link">RoomBooking</router-link></li>
              <li class="nav-item"><router-link to="/check" class="nav-link">Check Booking</router-link></li>
              <li class="nav-item"><router-link to="/feedback" class="nav-link">Feedback</router-link></li>
              <li class="nav-item" @click="keluar" v-if="role === 'guest'"><router-link to="" class="nav-link">LogOut</router-link></li>
              <li class="nav-item" v-else><router-link to="/login" class="nav-link">Login</router-link></li>
              <li class="nav-item" @click="checkHistory"><router-link to="" class="nav-link">History</router-link></li>
              <li class="nav-item"><router-link to="/position" class="nav-link">position</router-link></li>
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
        <button class="edit-button">Edit</button>
      </header>
      <main>
        <div class="room-detail">
          <h2>Suite Room</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/is/image/marriotts7prod/si-sgnsi-club-studio-kitchen-13487-22034:Classic-Hor?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <div class="price-text">
                  <p class="price-type">Flexible Member Price</p>
                  <p class="rate-details">Rate Details</p>
                </div>
                <div class="price-and-button">
                  <p class="price">4,410,000 VND / night</p>
                  <button class="select-button">Select</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <div class="container main-content">
      <main>
        <div class="room-detail">
          <h2>Deluxe Room</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/content/dam/marriott-renditions/SGNSI/sgnsi-king-suitebedroom-4648-hor-clsc.jpg?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <div class="price-text">
                  <p class="price-type">Flexible Member Price</p>
                  <p class="rate-details">Rate Details</p>
                </div>
                <div class="price-and-button">
                  <p class="price">4,410,000 VND / night</p>
                  <button class="select-button">Select</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <div class="container main-content">
      <main>
        <div class="room-detail">
          <h2>VIP Room</h2>
          <div class="room-content">
            <img src="https://cache.marriott.com/is/image/marriotts7prod/si-sgnsi-studio-twin-27424:Classic-Hor?output-quality=70&interpolation=progressive-bilinear&downsize=512px:342px" alt="Room Image" class="room-image">
            <div class="price-info">
              <div class="price-item">
                <div class="price-text">
                  <p class="price-type">Flexible Member Price</p>
                  <p class="rate-details">Rate Details</p>
                </div>
                <div class="price-and-button">
                  <p class="price">4,410,000 VND / night</p>
                  <button class="select-button">Select</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </main>
    </div>

    <footer class="footer-area section_gap">
      <div class="container">
        <div class="border_line"></div>
        <div class="row footer-bottom d-flex justify-content-between align-items-center">
          <p class="col-lg-8 col-sm-12 footer-text m-0">
            Copyright &copy;2024 All rights reserved | This template is made with <i class="fa fa-heart-o"
              aria-hidden="true"></i> by <a href="https://www.facebook.com/dammanhluu3241" target="_blank">Dam Manh Luu</a>
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
  </div>
</template>

<script>
export default {
  name: 'DetailRoomComponent',
  data() {
    return {
      dateInfo: 'Tuesday, June 25, 2024 - Wednesday, June 26, 2024',
      roomInfo: '1 Room : 2 Adults',
      role: 'guest' // hoặc 'tamu'
    };
  },
  methods: {
    keluar() {
      // Phương thức đăng xuất của bạn ở đây
    },
    checkHistory() {
      // Phương thức kiểm tra lịch sử của bạn ở đây
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
  padding-top: 120px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f3f3f3;
  border-bottom: 1px solid #ddd;
  margin-bottom: 20px;
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
  margin-bottom: 20px;
}

.room-content {
  display: flex;
  align-items: center;
}

.room-image {
  width: 50%;
  height: auto;
  margin-right: 20px;
  max-width: 200px;
}

.price-info {
  width: 50%;
}

.price-item {
  display: flex;
  justify-content: space-between;
  width: 100%;
  align-items: center;
}

.price-text {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.price-type {
  color: black;
  font-weight: bold;
  margin-bottom: 5px;
}

.rate-details {
  color: red;
  margin-bottom: 10px;
}

.price-and-button {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.price {
  color: black;
  font-size: 24px;
  font-weight: bold;
  text-align: center;
  flex-grow: 1;
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

.footer-area {
  background: #000;
  padding: 30px 0;
  font-size: 14px;
}

.footer-bottom {
  padding: 10px 0;
  border-top: 1px solid #eee;
}

.footer-text {
  margin: 0;
  color: #fff;
}

.footer-social a {
  margin-right: 15px;
  color: #fff;
}

.footer-social a:hover {
  color: #007bff;
}
</style>
