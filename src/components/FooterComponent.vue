<template>
  <section>
    <div class="container pt-5">
      <div class="d-flex">
        <div class="col-4">
          <img src="../assets/images/mt-2236-home-logo.png" alt="">
        </div>
        <div class="d-flex col-8">
          <div class="left">
            <p class="text-white fs-5">Follow Us</p>
            <div class="d-flex gap-2">
              <a href=""><i class="fa-brands fa-facebook-f"></i></a>
              <a href=""><i class="fa-solid fa-paper-plane"></i></a>
              <a href=""><i class="fa-brands fa-instagram"></i></a>
            </div>
          </div>
          <div class="right">
            <p class="text-white">Subscribe to get the latest news, course updates, discounts, events</p>
            <form>
              <div class="mb-3">
                <input type="email" class="form-control" id="InputEmail" placeholder="Enter your e-mail here *">
              </div>
            </form>
            <button type="button" class="btn btn-warning">Subscribe</button>
          </div>
        </div>
      </div>
      <p class="text-white py-3 mb-0 copyright">Copyright &#169; 2021. All Rights Reserved.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style lang="scss" scoped>
section {
  background-color: #404040;
  width: 100%;
  height: auto;
}

a{
  color: white;
  border: 1px solid white;
  border-radius: 10%;
  width: 35px;
  height: 35px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  transition: color, background-color, border;
  &:hover{
    color: #404040;
    background-color: white;
  }
}

.left {
  padding-right: 25%;
}

.copyright {
  font-size: 12px;
}



</style>
