<script>
import Header from "../../lib/components/Header.svelte";
import Help from "../../lib/components/Help.svelte";
import Footer from "../../lib/components/Footer.svelte";
import SimilarProperties from "../../lib/resale/SimilarProperties.svelte";
import Payment from "../../lib/resale/Payment.svelte";
import UnitDetails from "../../lib/resale/UnitDetails.svelte";
import ImageGallery from "../../lib/resale/ImageGallery.svelte";
import Contact from "../../lib/resale/Contact.svelte";

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
  <main class="main">
    <div class="wrapper">
      <UnitDetails/>
      <Payment price = {unit.price}/>
    </div>
    <Contact />
  </main>
  <SimilarProperties />
  <Help />
</div>

<Footer/>


<style>
  .container{
    max-width: var(--max-width);
    margin: 0 auto;
  }
  .main{
    margin-top: 40px;
  }
  @media screen and (min-width: 1024px){
    .main{
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 24px;
    }

  }
  
</style>