<template>
    <h1>Detail {{ detail.nama }}</h1>
    <h4>Harga : {{ detail.harga }}</h4>
    <h4>Keterangan : {{ detail.keterangan }}</h4>
</template>
<script>
   import { produk } from '@/assets/Produk.js';

   export default {
    props: [
        "id_produk"
    ],
    setup(props)
    {
       const detail = produk["produk"].find(function(item) {
         return item.id == props.id_produk;
        });
        return {
        detail
      }
     } 
   }
</script>