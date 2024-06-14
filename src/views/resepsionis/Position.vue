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
              <li class="nav-item"><router-link to="/Home" class="nav-link">Home</router-link></li>
              <li class="nav-item"><router-link to="/" class="nav-link">RoomBooking</router-link></li>
              <li class="nav-item"><router-link to="/check" class="nav-link">Check Booking</router-link></li>
              <li class="nav-item"><router-link to="/feedback" class="nav-link">Feedback</router-link></li>
              <li class="nav-item" v-if="role === 'tamu'" @click="keluar"><router-link to="" class="nav-link">Logout</router-link></li>
              <li class="nav-item" v-else><router-link to="/login" class="nav-link">Login</router-link></li>
              <li class="nav-item" @click="checkHistory"><router-link to="" class="nav-link">History</router-link></li>
              <li class="nav-item active"><router-link to="/position" class="nav-link">Position</router-link></li>
              <li class="nav-item"><router-link to="/DetailRoom" class="nav-link">DetailRoom</router-link></li>
            </ul>
          </div>
        </nav>
      </div>
    </header>

    <!-- Main Content -->
    <main id="maincontent" class="page-main">
      <div class="container">
        <div class="row">
          <div class="col-xs-12">
            <ol class="breadcrumb">
              <li><a href="/" target="_self">Trang chủ</a></li>
              <li><span>/</span></li>
              <li class="active"><span>Liên hệ</span></li>
            </ol>
          </div>
        </div>
        <div class="row contact">
          <div class="col-md-6">
           <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1959.5667765678497!2d106.65991038236658!3d10.801081740185495!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3175293092c7865b%3A0x2f0a0575683fd9c4!2zMThBIMSQLiBD4buZbmcgSMOyYSwgUGjGsOG7nW5nIDQsIFTDom4gQsOsbmgsIFRow6BuaCBwaOG7kSBI4buTIENow60gTWluaCwgVmnhu4d0IE5hbQ!5e0!3m2!1svi!2s!4v1717468540913!5m2!1svi!2s" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
          <div class="col-md-6">
            <h4>Thông tin liên hệ</h4>
            <form class="form-contact" action="#" method="POST">
              <div class="form-group">
                <input type="text" class="form-control" name="fullname" placeholder="Your Name" required oninvalid="this.setCustomValidity('Vui lòng nhập tên của bạn')" oninput="this.setCustomValidity('')">
              </div>
              <div class="row">
                <div class="form-group col-sm-6">
                  <input type="email" class="form-control" name="email" placeholder="Email" required oninvalid="this.setCustomValidity('Vui lòng nhập email')" oninput="this.setCustomValidity('')">
                </div>
                <div class="form-group col-sm-6">
                  <input type="tel" class="form-control" name="mobile" placeholder="Phone number" required pattern="[0][0-9]{9,}" oninvalid="this.setCustomValidity('Vui lòng nhập số điện thoại bắt đầu bằng số 0 và ít nhất 9 con số theo sau')" oninput="this.setCustomValidity('')">
                </div>
                <div class="form-group col-sm-12">
                  <textarea class="form-control" placeholder="Content" name="content" rows="10" required></textarea>
                </div>
                <div class="form-group col-sm-12">
                  <div class="message alert alert-success" style="display: none;" ></div>
                </div>
                <div class="form-group col-sm-12">
                  <button type="submit" class="btn btn-sm btn-primary pull-right">send</button>
                </div>
              </div>
            </form>
          </div>
        </div>
      </div>
    </main>

    <!-- Footer -->
    <footer class="footer-area section_gap">
      <div class="container">
        <div class="border_line"></div>
        <div class="row footer-bottom d-flex justify-content-between align-items-center">
          <p class="col-lg-8 col-sm-12 footer-text m-0 white-text">
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
  name: 'ContactPosition' // Đổi tên từ "Position" thành "ContactPosition"
}
</script>

<style scoped>
/* Thêm các style của bạn ở đây */
.header_area {
  margin-bottom: 20px; /* Tạo khoảng cách giữa header và nội dung chính */
}

.page-main {
  padding-top: 20px; /* Tạo khoảng cách giữa header và phần nội dung chính */
}

.footer-text.white-text {
  color: white; /* Đổi màu chữ thành màu trắng */
}

/* Thêm các style khác nếu cần */
</style>
