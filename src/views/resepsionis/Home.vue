<template>
  <div>
    <!-- Header -->
    <header class="header_area">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <a class="navbar-brand logo_h" href="/"><img src="image/Logo.png" alt=""></a>
          <button class="navbar-toggler" type="button" data-toggle="collapse"
            data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
            aria-label="Toggle navigation">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <div class="collapse navbar-collapse offset" id="navbarSupportedContent">
            <ul class="nav navbar-nav menu_nav desktop-only">
              <li class="nav-item active"><router-link to="/Home" class="nav-link">Home</router-link></li>
              <li class="nav-item"><router-link to="/" class="nav-link">RoomBooking</router-link></li>
              <li class="nav-item"><router-link to="/check" class="nav-link">Check Booking</router-link></li>
              <li class="nav-item"><router-link to="/feedback" class="nav-link">Feedback</router-link></li>
              <li class="nav-item" v-if="role === 'tamu'" @click="keluar"><router-link to="" class="nav-link">Logout</router-link></li>
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
        <div class="heading-with-image">
          <div>
            <h1>------------------------------------</h1>
            <h2>5-STAR DESTINATION RIGHT IN THE CENTER ENJOY AN INTERNATIONAL CLASS VACATION WITH ROYAL HOTEL</h2>
          </div>
        </div>
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
            <img src="https://imperiahotel.com/terrebonne/files/2018/07/tb_chambre_loft_int_1-600x395.jpg" alt="SUITE ROOM" />
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
        <img :src="imageSrc" alt="Hotel Image" />
      </div>
    </div>

    <!-- Hotel Room Display Component -->
    <div class="hotel-room-display">
      <div class="room-info">
        <h2>Superior Studio King</h2>
        <p>The Superior Studio King room class is the ideal choice for guests who prefer spacious space with natural light, 5-star amenities and wide views of the city.</p>
        <div class="details">
          <span>Area: 55 m2</span>
          <span>Bed: King</span>
          <span>Capacity: 2</span>
        </div>
        <button @click="bookNow">Book Now</button>
      </div>
      <div class="image-slider">
        <img :src="images[currentImage]" alt="Hotel Room" />
        <div class="navigation">
          <button @click="prevImage">‹</button>
          <button @click="nextImage">›</button>
        </div>
      </div>
    </div>

    <!-- Contact Information Section -->
    <div class="contact-info-section">
      <div class="contact-info">
        <h2>Royal Hotel</h2>
        <div class="contact-details">
          <p><i class="fas fa-map-marker-alt"></i> Address: 18A, CONG HOA, TAN BINH </p>
          <p><i class="fas fa-phone-alt"></i> Phone: +84 90 888 6666</p>
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
      imageSrc: 'https://vn.sheratonsaigon.com/resourcefiles/home-content-section-image/sgnsioutside.jpg?version=5282024223756',
      images: [
        'https://vn.sheratonsaigon.com/resourcefiles/roomssmallimages/sgnsisuperiorstudio.jpg?version=5282024223756',
        'https://vn.sheratonsaigon.com/resourcefiles/roomssmallimages/sgnsisuperiorstudiotwin.jpg?version=5282024223756',
        'https://vn.sheratonsaigon.com/resourcefiles/roomssmallimages/sgnsiexecutive2.jpg?version=5282024223756',
        // Add all image URLs here
      ],
      currentImage: 0
    };
  },
  methods: {
    bookNow() {
      // Handle booking logic here
      console.log('Booking now...');
    },
    nextImage() {
      this.currentImage = (this.currentImage + 1) % this.images.length;
    },
    prevImage() {
      this.currentImage = (this.currentImage - 1 + this.images.length) % this.images.length;
    },
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
  position: fixed;
  top: 0;
  z-index: 1000;
}

.navbar {
  padding: 10px 0;
}

.navbar-brand img {
  height: 40px;
}

.navbar-toggler {
  border: none;
}

.navbar-toggler .icon-bar {
  width: 22px;
  height: 2px;
  background-color: #000;
  display: block;
  margin: 4px auto;
  transition: all 0.3s;
}

.navbar-toggler:hover .icon-bar {
  background-color: #007bff;
}

.menu_nav .nav-item .nav-link {
  color: #000;
  font-weight: 500;
  padding: 10px 15px;
  display: inline-block;
  transition: color 0.3s;
}

.menu_nav .nav-item .nav-link:hover {
  color: #007bff;
}

.content-container {
  display: flex;
  justify-content: space-between;
  margin-top: 80px;
  padding: 20px;
}

.text-content {
  width: 65%;
}

.image-content {
  width: 30%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.image-content img {
  width: 100%;
  border-radius: 8px;
}

.heading-with-image {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.heading-with-image h1,
.heading-with-image h2 {
  margin: 0;
}

.cta {
  display: flex;
  justify-content: space-between;
}

.cta div {
  text-align: center;
}

.cta img {
  width: 180px;
  height: 120px;
  border-radius: 8px;
}

.contact-info-section {
  background: #f8f9fa;
  padding: 40px 20px;
}

.contact-info {
  text-align: center;
}

.contact-details {
  margin: 20px 0;
}

.contact-details p {
  margin: 10px 0;
}

.services-amenities {
  display: flex;
  justify-content: space-between;
  padding: 40px 20px;
  background: #fff;
}

.services-content {
  width: 60%;
}

.services-image {
  width: 35%;
}

.services-image img {
  width: 100%;
  border-radius: 8px;
}

.footer-area {
  background: #000;
  padding: 20px 0;
  color: white;
}

.footer-text {
  margin: 0;
}

.footer-social a {
  color: white;
  margin-right: 15px;
  transition: color 0.3s;
}

.footer-social a:hover {
  color: #007bff;
}

.hotel-room-display {
  display: flex;
  justify-content: space-between;
  background-color: #f0f0f0;
  padding: 20px;
  position: relative;
}

.room-info {
  background-color: white;
  padding: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  z-index: 10;
}

.room-info h2 {
  margin-top: 0;
}

.details {
  margin: 10px 0;
}

.details span {
  display: block;
}

button {
  background-color: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
}

.image-slider {
  position: relative;
}

.image-slider img {
  max-width: 300px;
  border-radius: 10px;
}

.navigation {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.navigation button {
  background: rgba(0, 0, 0, 0.5);
  border: none;
  color: white;
  font-size: 20px;
  cursor: pointer;
  padding: 10px;
}

.view-on-map {
  border-radius: 20px;
  background-color: #1e272e;
  color: white;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
}
</style>
