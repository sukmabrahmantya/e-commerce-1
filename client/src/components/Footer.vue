<template>
  <div class="footer">
    <div class="row foot">
      <div class="col">
        <div class="row">
          <div class="col">
            <h5>Products and Services</h5>
            <a to="/">Home</a><br>
            <a to="/">Custome Product</a><br>
            <a to="/">Service</a>
          </div>
          <div class="col mt-4">
            <a to="/purchase/gold">Buy Gold</a><br>
            <a to="/">Gold Series Indonesia</a>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="row">
          <div class="col">
            <h5>Information</h5>
            <a to="/">My Account</a><br>
            <a to="/">Logam Mulia Profile</a><br>
          </div>
          <div class="col">
            <h5>Support</h5>
            <a to="/">Contact Us</a><br>
          </div>
        </div>
      </div>
      <div class="col">
        <div>
          <h5>Accreditation</h5>
          <img src="../assets/accreditation-1.png">
          <img src="../assets/accreditation-2.png">
          <img src="../assets/accreditation-3.png">
        </div>
        <div class="mt-4">
          <h5>Security</h5>
          <img src="../assets/security.png">
        </div>
        <div class="mt-4">
          <img src="../assets/logam-mulia.png">
          <img src="../assets/antam-2.png">
        </div>
      </div>
    </div>
    <div class="copyright pt-4 text-center">
      © Brahmantya Sukma, 2020 All Rights Reserved
    </div>
  </div>
</template>

<script>
export default {
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Hind+Siliguri&display=swap');

.footer {
  color: white;
  width: 100%;
  font-family: 'Hind Siliguri', sans-serif;
}

.foot {
  border-top: 10px solid  #cb9b2d !important;
  text-align: left;
  padding-top: 30px;
  padding-left: 20px;
  width: 100vw;
  background-color: #23427e;
}

h5 {
  font-size: 14px;
  font-weight: bold;
  color: #cb9b2d
}

a {
  color: white;
  font-size: 12px;
}

.copyright {
  width: 100%;
  background-color: #23427e;
  color: white;
  font-size: 12px;
  padding-bottom: 20px
}

img {
  height: 30px;
  margin-right: 20px
}

.row {
  margin-left: 0px !important
}
</style>
