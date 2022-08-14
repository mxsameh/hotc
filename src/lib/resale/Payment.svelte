<script>
  export let price;

  let activePlan = 5;
  const noOfInstPerYear = 4;
  let dpp; 

  $: {
    switch (activePlan){
      case 5:
        dpp = 20;
        break;
      case 6:
        dpp = 25;
        break;
      case 7:
        dpp = 30;
        break;
      default:
        dpp = 20;
    }
  }

  $: dp = Math.round( price * (dpp/100) );
  $: totalNoOfInst = noOfInstPerYear * activePlan;
  $: instPerQuar = Math.round( (price - dp) / totalNoOfInst );


  const plan = (year) =>{
    activePlan = year;
  }



  
</script>

<section class="payment">
  <h2 class="payment__heading">NO Cash <br> NO Problem</h2>

  <nav class="payment__yearsList">
    <span class={activePlan == 5? "payment__year payment__year--active" : "payment__year"} on:click={()=>plan(5)}>5 years</span>
    <span class={activePlan == 6? "payment__year payment__year--active" : "payment__year"} on:click={()=>plan(6)}>6 years</span>
    <span class={activePlan == 7? "payment__year payment__year--active" : "payment__year"} on:click={()=>plan(7)}>7 years</span>
  </nav>

  <div class="payment__plan">

    <div class="details__left">
      <div class="plan__details">
        <li class="plan__heading">Down payment ({dpp}%)</li>
        <p class="plan__text">{dp.toLocaleString()} EGP</p>
      </div>
      <div class="plan__details">
        <li class="plan__heading">Installments (per Quarter)</li>
        <p class="plan__text">{instPerQuar.toLocaleString()} EGP</p>
      </div>
    </div>

    <div class="details__right">
      <div class="plan__details">
        <li class="plan__heading">Number of installments per year</li>
        <p class="plan__text">{noOfInstPerYear} Installments</p>
      </div>
      <div class="plan__details">
        <li class="plan__heading">Total number of installments</li>
        <p class="plan__text">{totalNoOfInst} Installments</p>
      </div>
    </div>

  </div>

  <h2 class="cust__text">for different payment plan</h2>
  <button class="cust__btn">customize payment plan</button>


</section>

<style lang="scss">
  .payment{
    padding: 24px 16px;
    background-color: var(--gray800);
    border-radius: 12px;
    margin-top: 32px;

    &__heading{
      color: white;
      font-size: 24px;
      line-height: 28px;
    }
    &__yearsList{
      display: flex;
      align-items: center;
      // justify-content: space-between;
      margin-top: 32px;
      gap: 24px;
    }
    &__year{
      border-radius: 8px;
      font-size: 14px;
      padding: 6px 16px;
      background-color: var(--gray300);
      &--active{
        background-color: var(--gray500);
        color: white;
      }
    }
    &__plan{
      margin-top: 24px;
    }

  }

  .plan{

    &__details{
      margin-top: 24px;
    }
    &__heading{
      color: var(--gray300);
      font-size: 16px;
      // list-style: disc;
    }
    &__text{
      color: white;
      font-size: 16px;
      font-weight: 500;
      margin-left: 12px;
      margin-top: 16px;
    }


  }

  .cust{
    &__text{
      margin-top: 32px;
      color: white;
      text-transform: capitalize;
      font-size: 20px;
      text-align: center;
    }
    &__btn{
      background-color: var(--blue);
      color: white;
      text-transform: capitalize;
      padding: 12px 24px;
      font-size: 16px;
      font-weight: 500;
      border-radius: 12px;
      display: block;
      margin: 24px auto 0;

    }
  }

  @media screen and (min-width: 767px){
    .payment{
      padding: 32px 24px 40px;

      &__heading{
        font-size: 40px;
        line-height: 44px;
        text-align: center;
      }
      &__yearsList{
        width: fit-content;
        margin: 32px auto 0;
        gap: 32px;
      }
      &__year{
        font-size: 16px;
        padding: 8px 24px;
        font-weight: 500;
        border-radius: 16px;
      }
      &__plan{
        display: flex;
        justify-content: space-between;
        margin: 40px auto 0;
        row-gap: 24px;
        max-width: 750px;
      }
    }

    .plan{
      &__details{
        flex-basis: 50%;
        margin-top: 0;
      }
      &__heading{
        font-size: 24px;
        white-space: nowrap;
      }
      &__text{
        font-size: 24px;
      }

    }

    .cust{
      &__text{
        font-size: 32px;
        margin-top: 40px;
      }
      &__btn{
        font-size: 20px;
        margin: 32px auto 0;

      }
    }

    .details__right, .details__left{
      display: flex;
      flex-direction: column;
      gap: 24px;
    }

  }
  
</style>