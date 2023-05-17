<template>
  <div>
    <Header />
    <Body />
    <Footer />
    <Footer2 />
  </div>
</template>

<style>

</style>

<script>
 import Header from "./components/Header";
 import Body from "./components/Body";
 import Footer from "./components/Footer";
 import Footer2 from "./components/Footer2";
 import Body2 from "./components/Body2";

 export default {
   name:"Layout",
   components:{
     Header,
     Body,
     Footer,
     Footer2,
     Body2
   }
 }


</script>