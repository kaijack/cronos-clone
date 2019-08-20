
<template>
  <div>
    <div class="gg">
      <div class="sad">
        <img
          src="https://www.cronos.id/wp-content/uploads/2019/06/background-konsultasi.jpg?id=1522"
          class="img-fluid"
          alt="Responsive image"
          style="-webkit-filter: contrast(10%); height: 300px; width: 100%;
  filter: contrast(20%);"
        />
        <div class="dsa">
          <!-- <img src="..." class="img-fluid" alt="Responsive image"> -->
          <p>
            <b>Hubungi Cronos</b>
          </p>
          <p>Layanan pelanggan dari kami siap untuk melayani Anda</p>
        </div>
      </div>
      <br />
    </div>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.145156696847!2d106.83071971448447!3d-6.2445937628838255!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f37150f6d8b1%3A0xbfa2c058006138aa!2sCRONOS.id!5e0!3m2!1sid!2sid!4v1566126615192!5m2!1sid!2sid"
      width="100%"
      height="350"
      frameborder="0"
      style="border:0"
      allowfullscreen
    ></iframe>
    <br />
    <br />
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-sm-5">
          <img
            src="https://www.cronos.id/wp-content/uploads/2019/06/call-center.png"
            style="justify-content: center;"
            alt
          />
          <h4>Konsultasi dengan Tim Kami</h4>
          <p>Jika Anda memiliki pertanyaan atau permasalahan tentang proyek, pembuatan sistem, pemasaran digital, atau segala hal terkait digital, bisa melalui kontak kami berikut:</p>
          <p>
            <b>ALAMAT</b>
          </p>
          <b>
            <p>PT Cronos Solusi Bisnis</p>
          </b>
          <p>Jalan Tegal Parang Utara III, No. 33, Kelurahan Tegal Parang, Kecamatan Mampang Prapatan, Kota Jakarta Selatan, Provinsi DKI Jakarta, Indonesia</p>
          <b>SUREL</b>
          <p>hello@cronos.id</p>
        </div>
        <div class="col-sm-5">
          <h3>
            <b>Kirim Pesan Langsung</b>
          </h3>
          <p>Anda juga bisa mengirimkan pesan langsung melalui formulir berikut:</p>
          <br />
          <div>
            <b-form @submit="onSubmit" @reset="onReset" v-if="show">
              <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
                <b-form-input id="input-2" v-model="form.name" required placeholder="Enter name"></b-form-input>
              </b-form-group>
              <b-form-group
                id="input-group-1"
                label="Email address:"
                label-for="input-1"
                description="We'll never share your email with anyone else."
              >
                <b-form-input
                  id="input-1"
                  v-model="form.email"
                  type="email"
                  required
                  placeholder="Enter email"
                ></b-form-input>
              </b-form-group>
              <b-form-group id="input-group-2" label="Judul Pesan" label-for="input-2">
                <b-form-input id="input-2" v-model="form.name" required placeholder="Enter judul"></b-form-input>
              </b-form-group>

              <b-form-textarea
                id="textarea"
                v-model="text"
                placeholder="Enter something..."
                rows="3"
                max-rows="6"
              ></b-form-textarea>
              <br />

              <b-button type="submit" variant="primary">Submit</b-button>
            </b-form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template><script>
export default {
  data() {
    return {
      form: {
        email: "",
        name: "",
        food: null,
        checked: []
      },
      text: "",
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      alert(JSON.stringify(this.form));
    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.name = "";
      this.form.food = null;
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    }
  }
};
</script>

<style scoped>
.sad {
  position: relative;
  color: rgb(255, 255, 255);
  background-color: rgba(0, 0, 0, 0.75) !important;
}
.sad p {
  font-size: 2vw;
}
.dsa {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.asd {
  font-size: 20px;
  height: 320px;
  width: 100%;
  color: rgb(0, 0, 0);
  text-align: center;

  /* background-color: rgba(0, 0, 0, 0.75) !important; */
}
/* img {
  height: 200px;
  width: 100%;
} */
</style>