<template>
  <footer class="footer px-4">
    <b-row align-v="center" class="justify-content-lg-between">
      <b-col lg="6">
        <div class="copyright text-center text-lg-left text-light">
          © {{year}} <a href="#" class="font-weight-bold ml-1 text-light" target="_blank">Bit Team</a>
        </div>
      </b-col>
      <b-col lg="6">
        <b-nav align="center" class="nav-footer justify-content-lg-end ">
          <b-nav-item href="#" class="text-light"  target="_blank">
            Bit
          </b-nav-item>
          <b-nav-item href="#" target="_blank">
           О сайте
          </b-nav-item>
        </b-nav>
      </b-col>
    </b-row>
  </footer>
</template>
<script>
export default {
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
