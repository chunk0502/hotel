<template>
  <div>
    <!-- Header -->
    <header class="header_area" style="position: fixed; width: 100%; top: 0; z-index: 1000;">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <!-- Brand and toggle get grouped for better mobile display -->
          <a class="navbar-brand logo_h" href="/"><img src="image/Logo.png" alt=""></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse"
            data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
            aria-label="Toggle navigation">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <!-- Collect the nav links, forms, and other content for toggling -->
          <div class="collapse navbar-collapse offset" id="navbarSupportedContent">
            <ul class="nav navbar-nav menu_nav desktop-only">
              <li class="nav-item active"><router-link to="/Home" class="nav-link">Home</router-link></li>
              <li class="nav-item"><router-link to="/" class="nav-link">RoomBooking</router-link></li>
              <li class="nav-item"><router-link to="/check" class="nav-link">Check Booking</router-link></li>
              <li class="nav-item"><router-link to="/feedback" class="nav-link">Feedback</router-link></li>
              <li class="nav-item" v-if="role === 'tamu'" @click="keluar"><router-link to="" class="nav-link">Login</router-link></li>
              <li class="nav-item" v-else><router-link to="/login" class="nav-link">Login</router-link></li>
              <li class="nav-item" @click="checkHistory"><router-link to="" class="nav-link">History</router-link></li>
            </ul>
          </div>
        </nav>
      </div>
    </header>

    <!-- Content Home Page -->
    <div class="content-container">
      <div class="text-content">
        <h1>5-STAR DESTINATION RIGHT IN THE CENTER</h1>
        <h2>ENJOY AN INTERNATIONAL CLASS VACATION WITH ROYAL HOTEL</h2>
        <p>
          Located in a prime location on Dong Khoi Street, just a few minutes away from famous attractions, administrative centers, office buildings and entertainment shopping areas, Royal Hotel is an ideal stopover. Helps visitors immerse themselves in the vibrant life of the city with luxurious experiences, modern facilities and professional services.
        </p>
        <p>
         Relax in 485 luxury rooms and suites with full amenities and wide views of the city and Saigon River. Each room is decorated with flowers, accented by the Royal Signature Bed Experience. In particular, the newly upgraded system of 379 rooms in the Main Tower building, designed with inspiration from Vietnamese culture, will bring visitors a close and inspiring experience.
        </p>
        <p>
          Enjoy delicious dishes at Royal's famous restaurants, from Saigon Café famous for its fresh seafood buffet and Western grilled dishes to the quintessence of Cantonese cuisine at Li Bai restaurant or meet and greet Work at The Lounge, a contemporary lounge area serving international and local cuisine all day. In particular, the Wine Bar area on the 23rd floor offers a unique experience that helps you admire the splendid city under magnificent city lights while enjoying creative drinks in the windy outdoor space.
        </p>
        <p>
          Pamper yourself at the exclusive Royal Club lounge and pamper yourself at the Lifestyle gym and outdoor swimming pool.
        </p>
        <p>
          With more than 2,200 square meters of 14 lobby rooms equipped with modern amenities and a maximum capacity of up to 1,000 guests, Royal Hotel is the perfect choice for all large and small conference and event needs in Ho Chi Minh City. .
        </p>
        <div class="cta">
          <div>
            <img src="https://imperiahotel.com/terrebonne/files/2018/07/tb_chambre_loft_int_1-600x395.jpg" />
            <p>SUITE ROOM</p>
          </div>
          <div>
            <img src="https://www.shutterstock.com/image-photo/hotel-room-interior-modern-seaside-600nw-1387008533.jpg" alt="DELUXE ROOM" />
            <p>DELUXE ROOM</p>
          </div>
          <div>
            <img src="https://img.freepik.com/premium-photo/classic-interior-design-inspiration_893610-6204.jpg" alt="VIP ROOM" />
            <p>VIP ROOM</p>
          </div>
        </div>
        <p>
          Royal Hotel belongs to Royal group, giving customers the opportunity to explore, relax and experience at more than 8,000 hotels in 139 countries and territories around the world. Come experience and receive benefits immediately.
        </p>
      </div>
      <div class="image-content">
        <img :src="imageSrc" alt="" />
      </div>
    </div>

    <!-- Contact Information Section -->
    <div class="contact-info-section">
      <div class="contact-info">
        <h2>Royal Hotel</h2>
        <div class="contact-details">
          <p><i class="fas fa-map-marker-alt"></i> Address: 18A, CONG HOA, TAN BINH </p>
          <p><i class="fas fa-phone-alt"></i> Phone: ++84 90 888 6666</p>
          <p><i class="fas fa-envelope"></i> Email: dammanhluu3241@gmail.com</p>
        </div>
        <button class="view-on-map">View on Map</button>
      </div>
    </div>

    <!-- Services & Amenities Section -->
    <div class="services-amenities">
      <div class="services-content">
        <h2>COVENIENT SERVICE</h2>
        <ul>
          <li>Royal Club Lounge</li>
          <li>Service food at room</li>
          <li>Swimming pool and bar Lifestyle</li>
          <li>Modern fitness room</li>
          <li>Free wifi</li>
          <li>Laundry Service</li>
          <li>Airport shuttle service</li>
          <li>24/7 concierge service</li>
          <li>Office services</li>
          <li>Indoor car parking </li>
        </ul>
      </div>
      <div class="services-image">
        <img src="https://vn.sheratonsaigon.com/resourcefiles/gallery-image-sec_righttop/lib22.jpg?version=5282024223756" alt="Services & Amenities" />
      </div>
    </div>

    <!-- Footer -->
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
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      imageSrc: 'path_to_your_main_image.jpg' // Update with the path to your main image
    };
  },
  methods: {
    keluar() {
      console.log("Logging out...");
    },
    checkHistory() {
      console.log("Checking history...");
    }
  }
};
</script>

<style scoped>
.header_area {
  background: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 100%;
}

.navbar {
  padding: 10px 0;
}

.navbar .navbar-brand img {
  height: 40px;
}

.navbar-toggler {
  border: none;
}

.navbar-toggler .icon-bar {
  background-color: #333;
}

.menu_nav {
  list-style: none;
  padding: 0;
  margin: 0;
}

.menu_nav .nav-item {
  display: inline-block;
  margin-right: 15px;
}

.menu_nav .nav-item .nav-link {
  color: #333;
  text-decoration: none;
  padding: 10px 15px;
  display: block;
}

.menu_nav .nav-item .nav-link:hover,
.menu_nav .nav-item .nav-link.active {
  background-color: #f0f0f0;
  border-radius: 4px;
}

.content-container {
  margin-top: 100px; /* Để đảm bảo nội dung không bị che khuất bởi header cố định */
  display: flex;
  padding: 20px;
}

.text-content {
  flex: 2;
  padding-right: 20px;
}

.image-content {
  flex: 1;
}

h1, h2 {
  color: #333;
}

p {
  line-height: 1.6;
  margin-bottom: 16px;
}

.cta {
  display: flex;
  justify-content: space-between;
  margin: 20px 0;
}

.cta div {
  display: flex;
  align-items: center;
  text-align: center;
}

.cta img {
  margin-right: 8px;
}

.contact-info-section {
  background-color: #f0f0f0;
  padding: 20px;
  margin-top: 20px;
  text-align: center;
}

.contact-info h2 {
  color: #333;
  margin-bottom: 15px;
}

.contact-details p {
  margin: 10px 0;
  color: #555;
  display: flex;
  align-items: center;
  justify-content: center;
}

.contact-details i {
  margin-right: 10px;
}

.view-on-map {
  background-color: #333;
  color: #fff;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.view-on-map:hover {
  background-color: #555;
}

.services-amenities {
  display: flex;
  padding: 40px 20px;
  background-color: #f9f9f9;
  margin-top: 40px;
}

.services-content {
  flex: 1;
  padding-right: 20px;
}

.services-content h2 {
  color: #333;
  margin-bottom: 20px;
}

.services-content ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.services-content ul li {
  margin-bottom: 10px;
  color: #555;
}

.services-image {
  flex: 1;
  text-align: center;
}

.services-image img {
  max-width: 100%;
  height: auto;
  border-radius: 8px;
}

.footer-area {
  background: #f9f9f9;
  padding: 50px 0;
  color: #777;
}

.footer-area .border_line {
  height: 1px;
  background: #e3e3e3;
  margin-bottom: 30px;
}

.footer-bottom {
  padding: 20px 0;
}

.footer-text {
  margin: 0;
}

.footer-social a {
  color: #777;
  margin-right: 10px;
  transition: color 0.3s;
}

.footer-social a:hover {
  color: #333;
}
</style>
