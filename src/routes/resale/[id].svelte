<script>
import Header from "../../lib/components/Header.svelte";
import Help from "../../lib/components/Help.svelte";
import Footer from "../../lib/components/Footer.svelte";
import SimilarProperties from "../../lib/resale/SimilarProperties.svelte";
import Payment from "../../lib/resale/Payment.svelte";
import UnitDetails from "../../lib/resale/UnitDetails.svelte";
import ImageGallery from "../../lib/resale/ImageGallery.svelte";

let unit = {
  img:'/p1.png',
  location: 'mivida - new cairo',
  type: 'villa - standalone',
  price: 5000000,
  area: 420,
  beds: 5,
  baths: 4
}
  
</script>

<Header/>
<ImageGallery />
<div class="container">
  <UnitDetails/>
  <Payment price = {unit.price}/>
  <SimilarProperties />
  <Help />
</div>

<Footer/>


<style>
  .container{
  }
  
</style>