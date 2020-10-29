<template>
  <div>
    <h2 class="heading">About</h2>
    <container id="flexcard">
       <img src="../assets/KathyS.jpg" alt="" />
      
      <div class="bioData">
         <div class="bio">
         
        Hi! I’m <strong>Kathy Neil</strong>, a <i>personal chef</i> , with 5 years of experince in the
        food industry. Part of being a great personal chef comes with
        understanding and working around peoples tastes. I’d be happy to share
        some tips and tricks to get you up and rolling in the industry.
      </div>
      <label for="input">
<input type="text" placeholder="janedoe@gmail.com" name="input"/>
        <Button> Tip me </Button>
      </label>
        
      </div>
    </container>

  </div>
</template>

<script>
import container from "./container";
import Button from "./button";

export default {
  name: "about",
  components: {
    container,
    Button,
  },
};
</script>

<style scoped>
#flexcard{
  line-height: 2;
}

img {
  border-radius: 20px;
  flex: 1;
  width: 100%;
}

.bioData {
  white-space: normal;
  flex: 1;
  padding: 4em;
  margin: auto;
}
label {
  margin-top: 2em;
  border-radius: 50px;
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  padding-left: 20px ;
  width: 90%;
  display: flex;
  justify-content: space-between;
}
input {
  border: none;
  background-color: #f1f6f7;
  color: rgba(0, 0, 0, 0.7);
  width: unset;
  font-size: 0.8em;
}
input::placeholder {
 color: rgba(0, 0, 0, 0.43);
}


strong {
  color: #d36200;
  font-size: 1.3em;
  font-weight: bold;
}
@media only screen and (max-width: 768px) {
 
}

@media only screen and (max-width: 600px) {
 #flexcard {
    flex-direction: column;
  }
  .bioData{
    padding: 4em 0;
  }
   
 .aboutInfo {
  margin: 13px 50px;
 }


}

</style>