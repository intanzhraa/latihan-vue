<template>
  <div>
    <h1>Formulir Rapot</h1>
    <hr>
  </div>

  <div>
    <form @submit.prevent="submitForm">
      <label for="">Nama</label>
      <input class="{'is-invalid':isInvalidName}" type="text"
      name="nama" v-model="siswa.name">
      <div v-if="isInvalidName" class="eror-message">
      </div>
      <br>
      <label for="">Kelas</label>
      <input class="{'is-invalid':isInvalidKelas}"
      type="kelas" name="kelas" v-model="siswa.kelas">
      <div v-if="isInvalidkelas" class="eror-message">
      </div>
      <br>
      <label for="">Alamat</label>
      <input class="{'is-invalid':isInvalidAlamat}"
      type="alamat" name="alamat" v-model="siswa.alamat">
      <div v-if="isInvalidAlamat" class="eror-message">
      </div>
      <br>
      <label for="">Nilai Matematika</label>
      <input class="{'is-invalid':isInvalidMatematika}"
      type="matematika" name="matematika" v-model="siswa.matematika">
      <div v-if="isInvalidMatematika" class="eror-message">
      </div>
      <br>
      <label for="">Nilai Bahasa Indonesia</label>
      <input class="{'is-invalid':isInvalidIndonesia}"
      type="indonesia" name="indonesia" v-model="siswa.indonesia">
      <div v-if="isInvalidIndonesia" class="eror-message">
      </div>
      <br>
      <label for="">Nilai Ipa</label>
      <input class="{'is-invalid':isInvalidIpa}"
      type="ipa" name="ipa" v-model="siswa.ipa">
      <div v-if="isInvalidIpa" class="eror-message">
      </div>
      <br>
      <button type="submit">Simpan</button>
    </form>
    <div v-if="showResult">
      nama : {{ name }} <br>
      kelas : {{ kelas }} <br>
      alamat : {{ alamat }} <br>
      nilai matematika : {{ matematika }} <br>
      nilai indonesia : {{ indonesia }} <br>
      nilai ipa : {{ ipa }} <br>
      total : {{ total }} <br>
      keterangan : {{ keterangan }}
    </div>
  </div>

</template>

<script>

import { ref } from 'vue';

export default {
  data() {
    return {
      siswa: {
        name: '',
        kelas: '',
        alamat: '',
        matematika: '',
        indonesia: '',
        ipa: '',
        total: '',
        keterangan: '',
      },
      showResult: ref(false),
      name: ref(''),
      kelas: ref(''),
      alamat: ref(''),
      matematika: ref(''),
      indonesia: ref(''),
      ipa: ref(''),
      total: 0,
      keterangan: ref(''),
    };
  },
  computed: {
    isInvalidName() {
      return this.name.length <=1;
    },
    isInvalidEmail() {
      return this.kelas.length <=1;
    },
    isInvalidAlamat() {
      return this.alamat.length <=1;
    },
    isInvalidMatematika() {
      return this.matematika.length <=1;
    },
    isInvalidIndonesia() {
      return this.indonesia.length <=1;
    },
    isInvalidIpa() {
      return this.ipa.length <=1 ;
    }
  },
  methods: {
    submitForm() {
      this.name = this.siswa.name;
      this.kelas = this.siswa.kelas;
      this.alamat = this.siswa.alamat;
      this.matematika = this.siswa.matematika;
      this.indonesia = this.siswa.indonesia;
      this.ipa = this.siswa.ipa;
      if (this.total > 240) {
        this.keterangan = "Lulus"
      } else {
        this.keterangan = "Tidak Lulus"
      }
      this.total = parseInt(this.matematika) + parseInt(this.indonesia) + parseInt(this.ipa);
      this.showResult = true;
    },
  },
};
</script>

<style>
h1 {
  color: lightskyblue;
}

.eror-message{
  color:red;
  margin-top:5px;
}

.is-invalid {
  border-color:red;
}
</style>