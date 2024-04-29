<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <nuxt-link to="/pengunjung/menu">
        <button type="button" class="btn btn-secondary mt-4">KEMBALI</button></nuxt-link>
        <h2 class="text-center my-4">RIWAYAT KUNJUNGAN</h2>
        <div class="my-3">
          <input type="search" class="form-control form-control-lg rounded-5" placeholder="Filter...">
        </div>
        <div class="my-3 text-muted">menampilkan 1 dari 1</div>
        <table class="table table-bordered">
          <thead>
            <tr>
              <td>#</td>
              <td>NAMA</td>
              <td>KEANGGOTAAN</td>
              <td>KELAS</td>
              <td>KEPERLUAN</td>
              <td>TANGGAL</td>
              <td>JAM</td>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>1.</td>
              <td>fahrul</td>
              <td>Siswa</td>
              <td>XI PPLG 3</td>
              <td>Baca</td>
              <td>22 Februari 2024</td>
              <td>10.20.00</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>