<template>
<div class="jurusan mt-5">
    <h3 class="m-5">PRESTASI SMKN 4 TASIKMALAYA</h3>
    <div class="scroll-container">
        <div class="card  mx-5" style="width: 20rem;">
            <img src="~/assets/pst.png" class="card-img-top" alt="...">
            <div class="card-body">
                <h5 class="card-title">PENCAK SILAT</h5>
            </div>
        </div>
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
</style>
<script setup>
useHead({ title: "PRESTASI" })
</script>