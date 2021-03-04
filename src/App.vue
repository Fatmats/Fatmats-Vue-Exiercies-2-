<template  >
  <div class="d-flex justify-content-between " >
    <div class="a" id="item">
      <strong>A</strong> 
      <h2>Openhat</h2>
        <audio class="a" src="./sound/openhat.wav" type="audio/wav" />
        
    </div>
     <div class="s" id="item">
       <strong>S</strong> 
       <h2>Ride</h2>
        <audio class="s" src="./sound/ride.wav" type="audio/wav" />
        
    </div>
     <div class="d" id="item">
       <strong>D</strong> 
       <h2>Snare</h2>
        <audio class="d" src="./sound/snare.wav" type="audio/wav" />
         
    </div>
     <div class="e" id="item">
        <strong>E</strong>
        <h2>Tink</h2>
        <audio class="e" src="./sound/tink.wav" type="audio/wav" />
         
     
    </div>
    <div class="w"  id="item">
        <strong>W</strong>
        <h2>Tom</h2>
        <audio class="w" src="./sound/tom.wav" type="audio/wav"  />
         
     
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  created: function () {
    window.addEventListener("keydown", (e) => {
      const audio = document.querySelector(`audio.${e.key}`);
      const key = document.querySelector(`div.${e.key}`)
      if (!audio) return;
      audio.play();
      key.classList.add('select');
    setTimeout(()=>{
      key.classList.remove('select');
    },1000)
    audio.play();

    });
  },
};
</script>

<style>
body {
  background-image: url(./img/bg1.jpg);
}
.d-flex{
  
  margin-top: 200px;
}
 #item{
   margin-left: 15px;
   border:3px solid rgb(0, 255, 106);
   background-color: rgba(128, 128, 128, 0.445);
   color:rgb(217, 255, 0);
   width: 140px;
   height: 140px;
   text-align: center;
   }
   strong{
     margin-top: 15px!important;
     position: relative;
     top: 20px;
   }
   h2{
     position: relative;
     top: 25px;
   }
   .select{
    box-shadow: 1px 0px 7px 7px #28a745;
   }
</style>
