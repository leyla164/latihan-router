<template>
    <h1>Detail {{ detail2.nama }}</h1>
    <h4>Harga : {{ detail2.harga }}</h4>
</template>
<script>
   import { kategori } from '@/assets/Kategori.js';

   export default {
    props: [
        "id_kategori"
    ],
    setup(props)
    {
       const detail2 = kategori["kategori"].find(function(item) {
         return item.id == props.id_kategori;
        });
        return {
         detail2
       }
     } 
   }
</script>