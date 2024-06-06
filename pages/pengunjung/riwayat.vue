<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center my-4">RIWAYAT KUNJUNGAN</h2>
        <div class="my-3">menampilkan {{ visitors.length }} dari {{ visitors.length }}</div>
        <div class="table table-responsive">
          <table class="table-bordered border-white text-white">
            <thead>
              <tr>
                <td>#</td>
                <td>Tanggal</td>
                <td>Waktu</td>
                <td>Nama</td>
                <td>Keanggotaan</td>
                <td>Kelas</td>
                <td>Keperluan</td>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(visitor, i) in visitors" :key="i">
                <td>{{ i+1 }}.</td>
                <td>{{ visitor.tanggal }}</td>
                <td>{{ visitor.waktu }}</td>
                <td>{{ visitor.nama }}</td>
                <td>{{ visitor.keanggotaan.nama }}</td>
                <td>{{ visitor.tingkat}}-{{ visitor.jurusan }}{{ visitor.kelas }}</td>
                <td>{{ visitor.keperluan.nama }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
    <div class="row float-end">
        <nuxt-link to="/pengunjung/menu" class="btn btn-dark btn-lg rounded-5 px-5">menu</nuxt-link>
    </div>
  </div>
</template>
<script setup>
const supabase = useSupabaseClient()

const visitors = ref([])
const getPengunjung = async () => {
  const { data, error } = await supabase.from('pengunjung').select(`*, keanggotaan(*), keperluan(*)`)
  if(data) visitors.value = data 
}
onMounted(() => {
  getPengunjung()
})
</script>

<style scoped>
.container-fluid {
  background-image: url('@/assets/img/bg-home-kunjungan.jpg');
  background-size: cover;
  height: 100vh;
  width: 100%;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  color:rgb(255, 255, 255);
  color: white;
  opacity: 70%;
}
.btn{
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  background-color: rgb(255, 255, 255);
  color: black;
  width: 150px;
  height: 50px;
}
</style>