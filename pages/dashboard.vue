<template>
  <section>
    <b-navbar type="dark" variant="info" fixed="bottom">
      <!-- <b-navbar-toggle target="nav_dropdown_collapse"></b-navbar-toggle> -->
      <b-col cols="3">
        <nuxt-link to="dashboard">
          <span style="color:red">
            Home
          </span>
        </nuxt-link>
      </b-col>
      <b-col cols="3">
        <nuxt-link to="about">
          <span style="color:red">
            Profile
          </span>
        </nuxt-link>
      </b-col>
      <b-col cols="3">
        <nuxt-link to="blog">
          <span style="color:red">
            Lokasi
          </span>
        </nuxt-link>
      </b-col>
    </b-navbar>
    <!-- <b-card  -->
    <b-row>
      <b-col cols="1">
      </b-col>
      <b-col cols="3">
        <b-img
          src="https://ih1.redbubble.net/image.412709073.7698/ap,550x550,12x16,1,transparent,t.png"
          rounded="square"
          thumbnail
          style="height:75px; width:75px"
          alt="img"
          class="m-1"
        />
      </b-col>
      <b-col cols="7" style="padding-left:0px;">
        <h3 style="margin-bottom:0px;font-size:18px;margin-top:5%;color:#47cf73;">
          Hasan Almubarok jasaka
        </h3>
        <span>
          area Malang
        </span>
      </b-col>
      <b-col cols="1">
      </b-col>
    </b-row>
    <b-row>
      <b-col cols="1">
      </b-col>
      <b-col cols="4">
        <label style="margin-bottom:0px;color:#47cf73; font-weight:bold">
          Total Toko
        </label>
        <br>
        <span style="color:red">
          500
        </span>
      </b-col>
       <b-col cols="1" style="padding-right:opx; padding-left:0px">
        <div class="headerDivider" />
       </b-col>
      <b-col cols="5" >
        <b-button type="reset" variant="danger">
          Tambah Toko
        </b-button>
      </b-col>
      <b-col cols="1">
      </b-col>
    </b-row>
    <hr>
    <listData
    toko="oko oki palapa"
    nama="oki putra"
    alamat=" jalan sanan"
    nohp="0987545"
    bergabung="bergabung : 12 januri 1219"
    />
    <listData
    toko="Toko Sumber Kemakmuran"
    nama=" Aulia Rahma"
    alamat="  Jalan Tambora"
    nohp="09878888545"
    bergabung=" bergabung : 13 januri 1019"
    />
    <listData
    toko="oki cell"
    nama="oki putra"
    alamat=" jalan sanan"
    nohp="0987545"
    bergabung="bergabung : 20 januri 2019"
    />
    <!-- </b-card> -->
  </section> 
</template>
<script>
import listData from '~/components/listData.vue'
export default {
  components: {
    listData
  }
}
</script>

<style scoped>
.headerDivider {
  border-right: 1px solid gray;
  height: 40px;
  top: 10px;
  width: 0px;
}
</style>
