
<template>
  <div class="cardbody">
      <img src="../assets/froggy.png" alt="">
      <h1>{{ name }}</h1>
      <h2>{{ department }}</h2>
      <h3>{{ company }}</h3>
      <div class="socials">
          <i class="fa-brands fa-facebook-f fa-2xl"></i>
          <i class="fa-brands fa-linkedin-in fa-2xl"></i>
          <i class="fa-brands fa-twitter fa-2xl"></i>
      </div>
      <div class="more-info" >
          <p id="more-info" hidden >
              more Info
          </p>
      </div>
      <button v-on:click="hello">
          <span>  More Info </span>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.1.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M256 0C114.6 0 0 114.6 0 256s114.6 256 256 256s256-114.6 256-256S397.4 0 256 0zM256 128c17.67 0 32 14.33 32 32c0 17.67-14.33 32-32 32S224 177.7 224 160C224 142.3 238.3 128 256 128zM296 384h-80C202.8 384 192 373.3 192 360s10.75-24 24-24h16v-64H224c-13.25 0-24-10.75-24-24S210.8 224 224 224h32c13.25 0 24 10.75 24 24v88h16c13.25 0 24 10.75 24 24S309.3 384 296 384z" fill="white"/></svg>
      </button>
  </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
       name: String,
       department: String,
       company: String
    },
    methods: {
        hello(){
            let moreInfo = document.getElementById('more-info');
            // let info = moreInfo.getAttribute('hidden');
            // console.log(info);
            if(moreInfo.hidden == true ){
                moreInfo.hidden = false;
            } else {
                moreInfo.hidden = true;
            }             
                       
        }
    }       
}
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,400;0,500;0,700;0,900;1,100;1,200;1,400;1,500;1,700;1,900&family=Rouge+Script&display=swap');
    

    h1,
    h2,
    h3 {
        font-family: 'Poppins', sans-serif;
    }

    h1,
    h3 {
        color: rgb(204,243,250);
        font-weight: 500;
    }

    h2 {
        color: rgb(141,200,208);
    }

    .cardbody {
        border-radius: 20px;
        width: 25rem;
        height: 40rem;
        padding: 10%;
        display: grid;
        justify-content: center;
        text-align: center;
        background: linear-gradient(rgb(31,201,208), rgb(17,102,108));
    }

    .cardbody img {
        margin: 50px auto 50px auto;
        height: auto;
        width: 200px;
    }

    .socials {
        margin: 0 auto;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        width: 15rem;
        margin-bottom: 1rem;  
    }

    .socials i {
        color: rgb(204,243,250);
    }

    button {
        display: flex;
        justify-content: center;
        align-items: center;
        border: 3px solid rgb(204,243,250);
        border-radius: 50px;
        height: 3rem;
        width: 23rem;
        background: transparent;
        position: relative;
    }

    button:hover {
        background: rgb(17,102,108);
    }

    button span {
        color: rgb(204,243,250);;
        font-size: 2rem;
        margin-right: 5px;
    }

    button svg {
        position: absolute;
        right: 10px;
        height: 20px;
    }
</style>
