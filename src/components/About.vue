<template>
  <div>
    <h2 class="heading">About</h2>
    <container id="flexcard">
       <img src="../assets/KathyS.jpg" alt="" />
      
      <div class="bioData">
         <div class="bio">
        Hi, I’m Kathy Neil, a personal chef, with 5 years of experince in the
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
  display: flex;
}


img {
  border-radius: 20px 0 0 20px;
  flex: 1;
  width: 100%;
}

.bioData {
  white-space: normal;
  flex: 1;
  padding: 50px 30px;
  margin: auto;;
}
label {
  margin-top: 50px;
  border-radius: 50px;
  box-shadow: 0px 8px 24px rgba(0, 0, 0, 0.15);
  padding: 6px 0 0 15px ;
  width: 90%;
  display: inline-block;
}
input {
  border: none;
  background-color: #f1f6f7;
  color: rgba(0, 0, 0, 0.7);
  width: unset;
}
input::placeholder {
 color: rgba(0, 0, 0, 0.43);
}
Button {
  float: right;
}
@media only screen and (max-width: 768px) {
 #flexcard {
    flex-direction: column;
  }
   img{
    border-radius: 20px 20px 0 0;
 }
}

@media only screen and (max-width: 600px) {
 
 .aboutInfo {
  margin: 13px 50px;
 }


}

</style>