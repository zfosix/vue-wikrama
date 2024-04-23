<template>
  <div>
    <h1>CRUD SEDERHANA
    </h1>
    <input type="text" placeholder="Masukan Nama" v-model="formatDataKelas.nama">
    <br>
    <input type="text" placeholder="Masukan Kelas" v-model="formatDataKelas.kelas">
    <br>
    <input type="text" placeholder="Masukan Rombel" v-model="formatDataKelas.rombel">
    <button @click="tambahKelas">Tambah siswa</button>
    <table>
      <tr>
        <th>Id</th>
        <th>Nama</th>
        <th>Kelas</th>
        <th>Rombel</th>
        <th>Aksi</th>
      </tr>
      <tr v-for="(murid, index) in dataKelas" :key="index">
        <td>{{ index + 1 }}</td>
        <td>{{ murid.nama }}</td>
        <td>{{ murid.kelas }}</td>
        <td>{{ murid.rombel }}</td>
        <td><button @click="hapusDataKelas(murid.id)">Hapus</button></td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dataKelas: [{
        id: Date.now(),
        nama: 'Fajar',
        kelas: 11,
        rombel: 'PPLG XI-3'
      }],
      formatDataKelas: {
        nama: '',
        kelas: '',
        rombel: '',
      }
    }
  },
  methods: {
    tambahKelas() {
      this.formatDataKelas.id = Date.now
      this.dataKelas.push(this.formatDataKelas);
      this.formatDataKelas = {
        nama: '',
        kelas: '',
        rombel: '',
      }
    },
    hapusDataKelas(id) {
      this.dataKelas = this.dataKelas.filter(item => item.id != id)
    }
  }
}
</script>

<style>
input
{
  margin: 5px;
  border-radius: 5px;
  padding: 5px;
}


table
{
  width: 100%;
  border-collapse: collapse;
}

th,
td
{
  border: 1px solid #ddd;
  padding: 8px;
  text-align: left;
}

tr:nth-child(even)
{
  background-color: #f2f2f2;
}

button
{
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 10px 10px;
  cursor: pointer;
  display: block;
  border-radius: 5px;
  margin: 6px;
}

button:hover
{
  background-color: #459aa0;
}
</style>


