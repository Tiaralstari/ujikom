<template>
    <div class="container-fluid ">
        <img src="../assets/pp.png" style="width: 100%;" alt="">
        <div class="sambutan card p-4">
            <div class="row">
                <div class="col-3 pt-3">
                    <img src="../assets/kepala.png" style="width: 100%;" class="bg-primary rounded-5" alt="">
                </div>
                <div class="col-8 pt-3">
                    <h4>Kurniawan, S.Pd, M.Pd</h4>
                    <h4>Assalamualaikum wr.wb</h4>
                    <h6 class="scroll">
                        Selamat datang di SMKN 4 Tasikmalaya. Segala puji dan syukur kita panjatkan kehadirat Allah SWT,
                        semoga kita semua ada dalam lindungan-Nya. Dan atas perkenan-Nya pula kami dapat menghadirkan
                        website SMK Negeri 4 Tasikmalaya ini. Kami berharap dengan adanya website di SMK Negeri 4
                        Tasikmalaya ini para pengunjung dapat mengenal lebih jauh tentang sekolah kami sehingga dapat
                        mempererat tali silaturrahmi antara sekolah dengan masyarakat demi kemajuan kita bersama. Tiada
                        gading yang tak retak, website kami ini masih dalam proses pengembangan, masih banyak kekurangan
                        yang harus kami perbaiki. Kritik dan sarannya yang membangun sangat kami harapkan untuk
                        pengembangan ke depan.
                        Akhirnya, saya mengucapkan terimakasih yang sebesar-besarnya kepada semua pihak yang tidak dapat
                        disebutkan satu segala bantuan dan persatu atas fasilitasnya yang telah diberikan semoga semua
                        yang kita lakukan bermanfaat bagi masyarakat. Wassalamu'alaikum Warahmatullahi Wabarakatuh.
                    </h6>
                </div>
            </div>
        </div>

        <div class="berita my-5 pt-5 ">
            <h3 class="m-5">BERITA ARTIKEL & INFORMASI</h3>
            <div class="scroll-container py-5">
                <div v-for="(cover, i) in berita" :key="i" class="card  mx-5" style="width: 20rem; ">
                    <img :src="cover.cover" class="card-img-top" style="height:10rem;" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">{{ cover.judul }}</h5>
                        <p class="card-text">{{ cover.subjudul }}</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="jurusan mt-5 pt-5">
            <h3 class="m-5">KOMPETENSI KEAHLIAN</h3>
            <div class="scroll-container">
                <div class="card  mx-5" style="width: 20rem;">
                    <img src="../assets/tkj.jpeg" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">TEKNIK JARINGAN KOMPUTER DAN TELEKOMUNIKASI</h5>
                    </div>
                </div>
                <div class="card  mx-5" style="width: 20rem;">
                    <img src="../assets/rpl.jpeg" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title"> PENGEMBANGAN PERANGKAT LUNAK DAN GIM</h5>
                    </div>
                </div>
                <div class="card  mx-5" style="width: 20rem;">
                    <img src="../assets/tsm.jpeg" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">TEKNIK SEPEDAH MOTOR</h5>
                    </div>
                </div>
                <div class="card  mx-5" style="width: 20rem;">
                    <img src="../assets/dkv.jpeg" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">DESAIN KOMUNIKASI VISUAL</h5>
                    </div>
                </div>
                <div class="card  mx-5" style="width: 20rem;">
                    <img src="../assets/toi.jpeg" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">TEKNIK OTOMASI INDUSTRI</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
            <div class="stat text-center bg-dark text-light">
            <div>
                <h2>GURU</h2>
                <h3>56</h3>
            </div>
        </div>
                <div class="stat text-center text-light" style="background-color: gray;">
            <div>
                <h2>SISWA</h2>
                <h3>15000</h3>
            </div>
        </div>
</template>
<style>
.scroll-container {
    display: flex;
    overflow-x: auto;
    gap: 1rem;
    padding: 1rem 0;
    scrollbar-width: thin;
}

.scroll-container::-webkit-scrollbar {
    height: 8px;
}

.scroll-container::-webkit-scrollbar-thumb {
    background-color: #aaa;
    border-radius: 4px;
}

.scroll-container::-webkit-scrollbar-track {
    background-color: #f1f1f1;
}
.scroll {
    max-height: 150px;
    overflow-y: auto; 
}

.card {
    flex: 0 0 auto;
}

.sambutan {
    width: 50%;
    position: absolute;
    top: 68%;
    right: 25%;
}

.berita {
    background-color: #4870A4;
}
</style>
<script setup>
const supabase = useSupabaseClient()
const berita = ref([])
useHead({ title: "HOME" })

const getBerita = async () => {
  const { data, error } = await supabase
    .from('berita')
    .select('*')
  if (error) {
    console.error('Error Berita:', error)
  } else {
    berita.value = data
  }
}

onMounted(() => {
  getBerita()
})
</script>