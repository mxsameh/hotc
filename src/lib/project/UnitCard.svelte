<script>
  export let unit;

</script>

<div class="unit">

  <img src={unit.img} class="unit__img" alt="">
  <p class="unit__price">Starting price <span>{unit.start} EGP</span></p>

  <div class="details">
    <!-- Type -->
    <div class="details__info">
        <svg class="icon type-icon" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
          <path d="M33.3333 31.6667V17.5C33.3333 17.2413 33.2731 16.9861 33.1573 16.7547C33.0416 16.5233 32.8736 16.322 32.6666 16.1667L21 7.41671C20.7115 7.20034 20.3606 7.08337 20 7.08337C19.6393 7.08337 19.2885 7.20034 19 7.41671L7.33329 16.1667C7.1263 16.322 6.95829 16.5233 6.84258 16.7547C6.72687 16.9861 6.66663 17.2413 6.66663 17.5V31.6667C6.66663 32.1087 6.84222 32.5327 7.15478 32.8452C7.46734 33.1578 7.89127 33.3334 8.33329 33.3334H31.6666C32.1087 33.3334 32.5326 33.1578 32.8451 32.8452C33.1577 32.5327 33.3333 32.1087 33.3333 31.6667Z" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <span class="details__text">{unit.type}</span>
    </div>
    <!-- AREA -->
    <div class="details__info">
      <svg class="icon area-icon" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <path d="M5 8.33333V31.6667C5 33.505 6.495 35 8.33333 35H31.6667C33.505 35 35 33.505 35 31.6667V8.33333C35 6.495 33.505 5 31.6667 5H8.33333C6.495 5 5 6.495 5 8.33333ZM31.67 31.6667H8.33333V8.33333H31.6667L31.67 31.6667Z" />
        <path d="M25 20H28.3333V11.6666H20V15H25V20ZM20 25H15V20H11.6666V28.3333H20V25Z" />
      </svg>
      <span class="details__text">{unit.minArea} - {unit.maxArea} sqm</span>
    </div>
    <!-- BED -->
    <div class="details__info">
      <svg class="icon bed-icon" viewBox="0 0 40 41" xmlns="http://www.w3.org/2000/svg">
        <path d="M7.5 7.61536C5.44375 7.61536 3.75 9.30911 3.75 11.3654V19.8404C2.9875 20.5304 2.5 21.5179 2.5 22.6154V33.8654H8.75V31.3654H31.25V33.8654H37.5V22.6154C37.5 21.5179 37.0125 20.5304 36.25 19.8404V11.3654C36.25 9.30911 34.5562 7.61536 32.5 7.61536H7.5ZM7.5 10.1154H32.5C33.1938 10.1154 33.75 10.6716 33.75 11.3654V18.8654H31.25V17.6154C31.25 15.5591 29.5562 13.8654 27.5 13.8654H22.5C21.5412 13.8654 20.6662 14.2404 20 14.8404C19.3164 14.2166 18.4254 13.8691 17.5 13.8654H12.5C10.4438 13.8654 8.75 15.5591 8.75 17.6154V18.8654H6.25V11.3654C6.25 10.6716 6.80625 10.1154 7.5 10.1154ZM12.5 16.3654H17.5C18.1938 16.3654 18.75 16.9216 18.75 17.6154V18.8654H11.25V17.6154C11.25 16.9216 11.8062 16.3654 12.5 16.3654ZM22.5 16.3654H27.5C28.1938 16.3654 28.75 16.9216 28.75 17.6154V18.8654H21.25V17.6154C21.25 16.9216 21.8062 16.3654 22.5 16.3654ZM6.25 21.3654H33.75C34.4438 21.3654 35 21.9216 35 22.6154V31.3654H33.75V28.8654H6.25V31.3654H5V22.6154C5 21.9216 5.55625 21.3654 6.25 21.3654Z" />
      </svg>
      <span class="details__text">{unit.beds} Bedrooms</span>
    </div>
    <!-- BATH -->
    <div class="details__info">
      <svg class="icon bath-icon" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
        <path d="M36.25 15H32.5C32.5 14.6685 32.3683 14.3505 32.1339 14.1161C31.8995 13.8817 31.5815 13.75 31.25 13.75H21.25C20.9185 13.75 20.6005 13.8817 20.3661 14.1161C20.1317 14.3505 20 14.6685 20 15H10V8.125C10 7.62772 10.1975 7.15081 10.5492 6.79917C10.9008 6.44754 11.3777 6.25 11.875 6.25C12.3723 6.25 12.8492 6.44754 13.2008 6.79917C13.5525 7.15081 13.75 7.62772 13.75 8.125C13.75 8.45652 13.8817 8.77446 14.1161 9.00888C14.3505 9.2433 14.6685 9.375 15 9.375C15.3315 9.375 15.6495 9.2433 15.8839 9.00888C16.1183 8.77446 16.25 8.45652 16.25 8.125C16.25 6.96468 15.7891 5.85188 14.9686 5.03141C14.1481 4.21094 13.0353 3.75 11.875 3.75C10.7147 3.75 9.60188 4.21094 8.78141 5.03141C7.96094 5.85188 7.5 6.96468 7.5 8.125V15H3.75C3.08696 15 2.45107 15.2634 1.98223 15.7322C1.51339 16.2011 1.25 16.837 1.25 17.5V22.5C1.25 24.8206 2.17187 27.0462 3.81282 28.6872C5.45376 30.3281 7.67936 31.25 10 31.25V33.75C10 34.0815 10.1317 34.3995 10.3661 34.6339C10.6005 34.8683 10.9185 35 11.25 35C11.5815 35 11.8995 34.8683 12.1339 34.6339C12.3683 34.3995 12.5 34.0815 12.5 33.75V31.25H27.5V33.75C27.5 34.0815 27.6317 34.3995 27.8661 34.6339C28.1005 34.8683 28.4185 35 28.75 35C29.0815 35 29.3995 34.8683 29.6339 34.6339C29.8683 34.3995 30 34.0815 30 33.75V31.25C32.3206 31.25 34.5462 30.3281 36.1872 28.6872C37.8281 27.0462 38.75 24.8206 38.75 22.5V17.5C38.75 16.837 38.4866 16.2011 38.0178 15.7322C37.5489 15.2634 36.913 15 36.25 15ZM30 16.25V21.25H22.5V16.25H30ZM36.25 22.5C36.25 23.3208 36.0883 24.1335 35.7742 24.8918C35.4602 25.6501 34.9998 26.3391 34.4194 26.9194C33.8391 27.4998 33.1501 27.9602 32.3918 28.2742C31.6335 28.5883 30.8208 28.75 30 28.75H10C8.3424 28.75 6.75269 28.0915 5.58058 26.9194C4.40848 25.7473 3.75 24.1576 3.75 22.5V17.5H20V22.5C20 22.8315 20.1317 23.1495 20.3661 23.3839C20.6005 23.6183 20.9185 23.75 21.25 23.75H31.25C31.5815 23.75 31.8995 23.6183 32.1339 23.3839C32.3683 23.1495 32.5 22.8315 32.5 22.5V17.5H36.25V22.5Z"/>
      </svg>
      <span class="details__text">{unit.baths} bathrooms</span>
    </div>

  </div>

  <button class="unit__btn">details</button>

</div>

<style lang="scss">
  .unit{
    padding: 8px;
    border-radius: 12px;
    background-color: var(--gray100);
    width: 300px;
    flex-shrink: 0;

    &__img{
      width: 100%;
      border-radius: 12px;
    }
    &__price{
      margin-top: 16px;
      font-size: 16px;
      color: var(--gray500);
      text-align: center;
      span{
        display: block;
        font-size: 20px;
        font-weight: bold;
        color: black;
        margin-top: 8px;
      }
    }
    &__btn{
      color: var(--blue);
      font-size: 20px;
      text-transform: capitalize;
      display: block;
      padding: 8px 24px;
      margin: 24px auto 8px;
    }
  }
  .details{
    margin-top: 16px;
    display: grid;
    grid-template-columns: repeat(2,min-content);
    justify-content: space-between;
    row-gap: 16px;
    padding: 0 8px;

    &__info{
      display: flex;
      gap: 4px;
      align-items: center;
      flex-basis: 50%;
    }
    &__text{
      white-space: nowrap;
      text-transform: capitalize;
      font-size: 16px;
    }
  }

  .icon{
    width: 20px;
    fill: black;
    flex-shrink: 0;
  }
  .type-icon{
    fill: none;
    stroke: black;
  }

  @media screen and (min-width:768px){
      .unit{
        width: 360px;

        &__price{
          font-size: 20px;
          margin-top: 24px;
          span{
            font-size: 24px;
          }
        }

        &__btn{
          font-size: 24px;
          padding: 12px 32px;
          margin: 32px auto 16px;
        }
      }

      .details{
        margin-top: 24px;

        &__info{
          gap: 8px;
        }
        &__text{
          font-size: 20px;
        }
      }

      .icon{
        width: 24px;
      }
  }
  
</style>