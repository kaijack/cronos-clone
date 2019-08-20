<template>
  <div>
    <bgambar />
    <br />
    <div>
      <ket />
      <br />
      <blogc />

      <konsultasi />
    </div>

    <sfooter />
  </div>
</template>

<script>
// @ is an alias to /src
import bgambar from "@/components/Bgambar.vue";
import ket from "@/components/Ket.vue";
import blogc from "@/components/Blogc.vue";
import konsultasi from "@/components/Konsultasi.vue";
import sfooter from "@/components/Sfooter.vue";

export default {
  components: {
    bgambar,
    ket,
    blogc,
    konsultasi,
    sfooter
  }
};
</script>


