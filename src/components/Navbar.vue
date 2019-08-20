<template>
  <div>
    <div class="container">
      <b-navbar toggleable="lg" type="light" style="background-color: white;">
        <!-- <div class="container"> -->
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-navbar variant="faded" type="light">
          <b-navbar-brand href="#">
            <router-link to="/">
              <img
                src="https://www.cronos.id/wp-content/uploads/2019/06/logo_cronos.png"
                alt="Kitten"
                height="40"
              />
            </router-link>
          </b-navbar-brand>
        </b-navbar>

        <b-collapse id="nav-collapse" is-nav class="text-left">
          <b-navbar-nav>
            <b-nav-item>
              <b>
                <router-link to="/" style="color: grey;">HOME</router-link>
              </b>
            </b-nav-item>
          </b-navbar-nav>
          <b-navbar-nav>
            <b-nav-item style="display: inline;">
              <a-dropdown style="color: grey;">
                <a class="ant-dropdown-link" href="#">
                  <b>TENTANG KAMI</b>
                  <a-icon type="down" />
                </a>
                <a-menu slot="overlay">
                  <a-menu-item>
                    <a>
                      <router-link to="/about">Tentang Kami</router-link>
                    </a>
                  </a-menu-item>
                  <a-menu-item>
                    <a href="javascript:;">Karier</a>
                  </a-menu-item>
                  <a-menu-item>
                    <a href="javascript:;">Magang</a>
                  </a-menu-item>
                </a-menu>
              </a-dropdown>&nbsp; &nbsp;
              <a-dropdown style="color: grey;">
                <a class="ant-dropdown-link" href="#">
                  <b>PRODUK & LAYANAN</b>
                  <a-icon type="down" />
                </a>
                <a-menu slot="overlay">
                  <a-menu-item>
                    <router-link to="/crm" style="color: grey;">Costumer Relationship Management</router-link>
                  </a-menu-item>
                  <a-menu-item>
                    <a href="javascript:;">Sistem Informasi Management Rumah Sakit Cronos Health</a>
                  </a-menu-item>
                  <a-menu-item>
                    <a href="javascript:;">Loyalty System</a>
                  </a-menu-item>
                </a-menu>
              </a-dropdown>&nbsp; &nbsp;
              <a-dropdown style="color: grey;">
                <a class="ant-dropdown-link" href="#">
                  <b>ARTIKEL</b>
                  <a-icon type="down" />
                </a>
                <a-menu slot="overlay">
                  <a-menu-item>
                    <a href="javascript:;">Blog</a>
                  </a-menu-item>
                  <a-menu-item>
                    <a href="javascript:;">Siaran Pers</a>
                  </a-menu-item>
                </a-menu>
              </a-dropdown>
            </b-nav-item>
          </b-navbar-nav>
          <b-navbar-nav>
            <b-nav-item href="#">
              <b>
                <router-link to="/kontak" style="color: grey;">KONTAK</router-link>
              </b>
            </b-nav-item>
          </b-navbar-nav>

          <!-- Right aligned nav items -->

          <b-navbar-nav class="ml-auto">
            <a-dropdown class="d-none d-sm-block mt-2">
              <a-icon type="search" style="font-size: 15px;" />
              <a-menu slot="overlay">
                <a-menu-item key="0">
                  <a-input placeholder="Search.." class="sos">
                    <a-icon slot="prefix" type="search" />
                  </a-input>
                </a-menu-item>
              </a-menu>
            </a-dropdown>&nbsp; &nbsp;
            <a-button type="primary" icon="mail">KONSULTASI GRATIS</a-button>
          </b-navbar-nav>
        </b-collapse>
        <br />
        <a-dropdown class=".hidden-sm-up d-block d-sm-none">
          <a-icon type="search" style="font-size: 15px;" />
          <a-menu slot="overlay">
            <a-menu-item key="0">
              <a-input placeholder="Search.." class="sos">
                <a-icon slot="prefix" type="search" />
              </a-input>
            </a-menu-item>
          </a-menu>
        </a-dropdown>
        <!-- </div> -->
      </b-navbar>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      current: ["mail"]
    };
  }
};
</script>

<style scoped>
.search {
  position: relative;
  color: #aaa;
  font-size: 16px;
}
.search input {
  width: 250px;
  height: 32px;
  background: #fcfcfc;
  border: 1px solid #aaa;
  border-radius: 5px;
  box-shadow: 0 0 3px #ccc, 0 10px 15px #ebebeb inset;
}
.search input {
  text-indent: 32px;
}
.search .fa-search {
  position: absolute;
  top: 10px;
  left: 10px;
}
input.sos,
textarea {
  background: cyan;
}
</style>