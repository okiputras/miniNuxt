<template>
  <section>
    <b-row>
      <b-col cols="4">
        <div class="clearfix">
          <b-img right src="http://www.popmie.com/uploads/product/rasa-ayam-bawang-spesial_text.png" style="height:75px; width:75px" alt="left image" />
        </div>
      </b-col>
      <b-col cols="8">
        <h4 style="font-size:15px;font-weight:bold">
          {{toko}}
        </h4>
        <p style="margin-bottom:0px;font-size:12px;color:grey">
         {{nama}}  
        </p>
        <p style="margin-bottom:0px;font-size:12px;margin-top:0px;color:grey">
          {{alamat}}
        </p>
        <p style="margin-bottom:0px;font-size:12px;margin-top:0px;color:grey">
          {{nohp}}
        </p>
        <p style="margin-bottom:10px;font-size:12px;margin-top:0px;color:grey">
          {{bergabung}}
        </p>
      </b-col>
    </b-row>
  </section>
</template>
<script>
export default {
  props: {
    toko: {
      type: String,
      required: true
    },
    nama: {
      type: String,
      required: true
    },
    alamat: {
      type: String,
      required: true
    },
    nohp: {
      type: String,
      required: true
    },
    bergabung: {
      type: String,
      required: true
    }
  }
}
</script>
