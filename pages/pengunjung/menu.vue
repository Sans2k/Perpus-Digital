<template>
  <div class="container-fluid">
    <div class="row my-5">
      <div class="col-lg-6">
        <nuxt-link to="/pengunjung/riwayat">
          <div class="card bg-pengunjung rounded-5">
            <div class="card-body pt-5">
              <h2 class="mt-5">RIWAYAT KUNJUNGAN</h2>
            </div>
          </div>
        </nuxt-link>
      </div>

      <div class="col-lg-6">
        <nuxt-link to="/buku">
          <div class="card bg-buku rounded-5">
            <div class="card-body pt-5">
              <h2 class="mt-5">CARI BUKU</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>
<style scoped>
.card {
  opacity: 80%;
  color: white;
  align-items: center;
  height:250px;
  box-shadow: 1px 1px 10px #424242;
}
.card.bg-pengunjung {
  background-image: url('@/assets/img/bg-home-kunjungan.jpg');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
}
.card.bg-buku {
  background: url('@/assets/img/bg-home-cari-buku.jpg');
  background-size: cover;
}
</style>
