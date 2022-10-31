<template>
   <h1 class="title">Sorting Visualizer</h1>

   <section class="data-container"></section> 
   <div class = "nav">
    <button  class="btn2" data-hover="Generate Bars" v-on:click="generatebars()" id="Button1" >
      <svg id="Layer_1" height="25" viewBox="0 0 24 24" width="30" class="imgbutton" xmlns="http://www.w3.org/2000/svg" data-name="Layer 1"><path d="m16 16a1 1 0 0 1 -1 1h-2v2a1 1 0 0 1 -2 0v-2h-2a1 1 0 0 1 0-2h2v-2a1 1 0 0 1 2 0v2h2a1 1 0 0 1 1 1zm6-5.515v8.515a5.006 5.006 0 0 1 -5 5h-10a5.006 5.006 0 0 1 -5-5v-14a5.006 5.006 0 0 1 5-5h4.515a6.958 6.958 0 0 1 4.95 2.05l3.484 3.486a6.951 6.951 0 0 1 2.051 4.949zm-6.949-7.021a5.01 5.01 0 0 0 -1.051-.78v4.316a1 1 0 0 0 1 1h4.316a4.983 4.983 0 0 0 -.781-1.05zm4.949 7.021c0-.165-.032-.323-.047-.485h-4.953a3 3 0 0 1 -3-3v-4.953c-.162-.015-.321-.047-.485-.047h-4.515a3 3 0 0 0 -3 3v14a3 3 0 0 0 3 3h10a3 3 0 0 0 3-3z"/></svg>
    </button>   
      
    <button class="btn2" data-hover="Selection Sort"
            v-on:click="SelectoinSort()" id="Button2" >
            <svg id="Layer_1" height="25" viewBox="0 0 24 24" width="30" class="imgbutton"  xmlns="http://www.w3.org/2000/svg" data-name="Layer 1"><path d="m18 9.064a3.049 3.049 0 0 0 -.9-2.164 3.139 3.139 0 0 0 -4.334 0l-11.866 11.869a3.064 3.064 0 0 0 4.33 4.331l11.87-11.869a3.047 3.047 0 0 0 .9-2.167zm-14.184 12.624a1.087 1.087 0 0 1 -1.5 0 1.062 1.062 0 0 1 0-1.5l7.769-7.77 1.505 1.505zm11.872-11.872-2.688 2.689-1.5-1.505 2.689-2.688a1.063 1.063 0 1 1 1.5 1.5zm-10.825-6.961 1.55-.442.442-1.55a1.191 1.191 0 0 1 2.29 0l.442 1.55 1.55.442a1.191 1.191 0 0 1 0 2.29l-1.55.442-.442 1.55a1.191 1.191 0 0 1 -2.29 0l-.442-1.55-1.55-.442a1.191 1.191 0 0 1 0-2.29zm18.274 14.29-1.55.442-.442 1.55a1.191 1.191 0 0 1 -2.29 0l-.442-1.55-1.55-.442a1.191 1.191 0 0 1 0-2.29l1.55-.442.442-1.55a1.191 1.191 0 0 1 2.29 0l.442 1.55 1.55.442a1.191 1.191 0 0 1 0 2.29zm-5.382-14.645 1.356-.387.389-1.358a1.042 1.042 0 0 1 2 0l.387 1.356 1.356.387a1.042 1.042 0 0 1 0 2l-1.356.387-.387 1.359a1.042 1.042 0 0 1 -2 0l-.387-1.355-1.358-.389a1.042 1.042 0 0 1 0-2z"/></svg>
          </button>

      <button class="btn2" data-hover="Comb Sort"
            v-on:click="CombSort()" id="Button3" >
        <svg xmlns="http://www.w3.org/2000/svg" id="Layer_1" data-name="Layer 1" viewBox="0 0 24 24" width="30" height="25" class="imgbutton"><path d="M11.828,16.462a53.471,53.471,0,0,1-3.685-5.776C9.665,7.709,11,4.189,11,1A1,1,0,0,0,9,1,18.683,18.683,0,0,1,7.005,8.431,18.694,18.694,0,0,1,5,1,1,1,0,0,0,3,1c0,3.174,1.342,6.7,2.868,9.685a50.636,50.636,0,0,1-3.695,5.777A3.986,3.986,0,1,0,7,22.618a3.985,3.985,0,1,0,4.828-6.156ZM4,22a2,2,0,1,1,2-2A2,2,0,0,1,4,22Zm.883-5.895c.585-.844,1.337-1.991,2.122-3.342.784,1.35,1.534,2.5,2.117,3.341A3.984,3.984,0,0,0,7,17.382,3.989,3.989,0,0,0,4.883,16.105ZM10,22a2,2,0,1,1,2-2A2,2,0,0,1,10,22ZM18,6V8h5a1,1,0,0,1,0,2H18v2h5a1,1,0,0,1,0,2H18v2h5a1,1,0,0,1,0,2H18v5a1,1,0,0,1-2,0V5a5.006,5.006,0,0,1,5-5h2a1,1,0,0,1,0,2H21a3,3,0,0,0-2.816,2H23a1,1,0,0,1,0,2Z"/></svg>
          </button>

      <button class="btn2" data-hover="Shell Sort"
            v-on:click="ShellSort()" id="Button4" >
            <svg width="30px" height="25px" viewBox="0 0 24 24" role="img" xmlns="http://www.w3.org/2000/svg" class="imgbutton"><title>Shell icon</title><path d="M12 .863C5.34.863 0 6.251 0 12.98c0 .996.038 1.374.246 2.33l3.662 2.71.57 4.515h6.102l.326.227c.377.262.705.375 1.082.375.352 0 .732-.101 1.024-.313l.39-.289h6.094l.563-4.515 3.695-2.71c.208-.956.246-1.334.246-2.33C24 6.252 18.661.863 12 .863zm.996 2.258c.9 0 1.778.224 2.512.649l-2.465 12.548 3.42-12.062c1.059.36 1.863.941 2.508 1.814l.025.034-4.902 10.615 5.572-9.713.033.03c.758.708 1.247 1.567 1.492 2.648l-6.195 7.666 6.436-6.5.01.021c.253.563.417 1.36.417 1.996 0 .509-.024.712-.164 1.25l-3.554 2.602-.467 3.71h-4.475l-.517.395c-.199.158-.482.266-.682.266-.199 0-.483-.108-.682-.266l-.517-.394H6.322l-.445-3.61-3.627-2.666c-.11-.436-.16-.83-.16-1.261 0-.72.159-1.49.426-2.053l.013-.024 6.45 6.551L2.75 9.621c.25-1.063.874-2.09 1.64-2.713l5.542 9.776L4.979 6.1c.555-.814 1.45-1.455 2.546-1.827l3.424 12.069L8.355 3.816l.055-.03c.814-.45 1.598-.657 2.457-.657.195 0 .286.004.528.03l.587 13.05.46-13.059c.224-.025.309-.029.554-.029z"/></svg>
          </button>

      <button class="btn2" data-hover="Reset"
            v-on:click="reset()" id="Button5" >
            <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="30" height="25" class="imgbutton"
            viewBox="0 0 383.748 383.748" style="enable-background:new 0 0 383.748 383.748;" xml:space="preserve">
              <path d="M62.772,95.042C90.904,54.899,137.496,30,187.343,30c83.743,0,151.874,68.13,151.874,151.874h30
                C369.217,81.588,287.629,0,187.343,0c-35.038,0-69.061,9.989-98.391,28.888C70.368,40.862,54.245,56.032,41.221,73.593
                L2.081,34.641v113.365h113.91L62.772,95.042z"/>
              <path d="M381.667,235.742h-113.91l53.219,52.965c-28.132,40.142-74.724,65.042-124.571,65.042
                c-83.744,0-151.874-68.13-151.874-151.874h-30c0,100.286,81.588,181.874,181.874,181.874c35.038,0,69.062-9.989,98.391-28.888
                c18.584-11.975,34.707-27.145,47.731-44.706l39.139,38.952V235.742z"/>
            </svg>
            </button>
   </div>
</template>
<script>

export default {
  data: function(){
    return{
      loaded: true,
    }
  },
  methods: {
    disable: function(){
    
      document.getElementById("Button2").disabled = true;
      document.getElementById("Button2").style.backgroundColor = "#cda4de";      
      document.getElementById("Button3").disabled = true;
      document.getElementById("Button3").style.backgroundColor = "#cda4de";      
      document.getElementById("Button4").disabled = true;
      document.getElementById("Button4").style.backgroundColor = "#cda4de";      
    },
    generatebars: function(){
      const container = document.querySelector(".data-container");

      for (let i = 0; i < 95; i += 1){
        const value = Math.floor(Math.random() * 100) + 1;
        const bar = document.createElement("div");
        bar.classList.add("bar");
        bar.style.height = `${value * .75}vh`;
        bar.style.transform = `translateX(${i * 1.04}vw)`;
        const barLabel = document.createElement("label");
        barLabel.classList.add("bar_id");
        barLabel.innerHTML = value;        
        bar.appendChild(barLabel);
        container.appendChild(bar);

      }
      document.getElementById("Button1").disabled = true;
      document.getElementById("Button1").style.backgroundColor = "#cda4de";  
    },



    SelectoinSort: async function(){
      let bars = document.querySelectorAll(".bar");
      this.disable();
      var min_idx = 0;
      for (var i = 0; i < bars.length; i += 1) {
        min_idx = i;

        bars[i].style.backgroundColor = "#266DD3";
        for (var j = i + 1; j < bars.length; j += 1) {
        bars[j].style.backgroundColor = "red";
          
        await new Promise((resolve) =>
          setTimeout(() => {
          resolve();
          }, 50)
        );

        var val1 = parseInt(bars[j].childNodes[0].innerHTML);
        var val2 = parseInt(bars[min_idx].childNodes[0].innerHTML);

        if (val1 < val2) {
          if (min_idx !== i) {
          bars[min_idx].style.backgroundColor = "#6B6B71";
          }
          min_idx = j;
        } 
        else {
          bars[j].style.backgroundColor = "#6B6B71";
        }
        }

        var temp1 = bars[min_idx].style.height;
        var temp2 = bars[min_idx].childNodes[0].innerText;
        bars[min_idx].style.height = bars[i].style.height;
        bars[i].style.height = temp1;
        bars[min_idx].childNodes[0].innerText = bars[i].childNodes[0].innerText;
        bars[i].childNodes[0].innerText = temp2;

        await new Promise((resolve) =>
        setTimeout(() => {
          resolve();
        }, 50)
        );

        bars[min_idx].style.backgroundColor = " rgb(24, 190, 255)";
        bars[i].style.backgroundColor = " rgb(49, 226, 13)";


      }
    },




    calculate_gap: function(gap){
      gap = parseInt((gap * 10) / 13, 10);
      if (gap < 1) return 1;
      return gap;
    },



    CombSort: async function(){
      let bars = document.querySelectorAll(".bar");
      this.disable();

      var gap = 95;
      
      let swapped = true;
      
      while (gap != 1 || swapped == true) {
      
        gap = this.calculate_gap(gap);
      
        swapped = false;
      
        for (var i = 0; i < 95 - gap; i++) {

          var value1 = parseInt(bars[i].childNodes[0].innerHTML);
      
          var value2 = parseInt(bars[i + gap].childNodes[0].innerHTML);
          if (value1 > value2) {
            
            bars[i].style.backgroundColor = "red";
      
            bars[i + gap].style.backgroundColor = "red";

            var temp1 = bars[i].style.height;
            var temp2 = bars[i].childNodes[0].innerText;

            await new Promise((resolve) =>
              setTimeout(() => {
                resolve();
              }, 40)
            );
            bars[i].style.height = bars[i + gap].style.height;
            bars[i].childNodes[0].innerText = bars[i + gap].childNodes[0].innerText;
            bars[i + gap].style.height = temp1;
            bars[i + gap].childNodes[0].innerText = temp2;
            
            swapped = true;

            await new Promise((resolve) =>
              setTimeout(() => {
                resolve();
              }, 40)
            );
          }
          bars[i].style.backgroundColor = "#6B6B71";
          bars[i + gap].style.backgroundColor = "#7B7B75";
          await new Promise((resolve) =>
            setTimeout(() => {
              resolve();
            }, 100)
          );
        }
      }
      for (var x = 0; x < 95; x++) {
        bars[x].style.backgroundColor = "rgb(49, 226, 13)";
      }
    },



    ShellSort: async function(){
    let bars = document.querySelectorAll(".bar");
    this.disable();

    for (var i = 10; i > 0; i = Math.floor(i / 2)) {
      await new Promise((resolve) =>
          setTimeout(() => {
              resolve();
          }, 1)
      );

      for (var j = i; j < 95; j++) {
          var temp = parseInt(bars[j].childNodes[0].innerHTML);
          var k;

          var temp1 = bars[j].style.height;
          var temp2 = bars[j].childNodes[0].innerText;

          for (k = j;k >= i && parseInt(bars[k - i].childNodes[0].innerHTML) > temp;k -= i) {
              bars[k].style.height = bars[k - i].style.height;

              bars[k].childNodes[0].innerText = bars[k - i].childNodes[0].innerText;

              await new Promise((resolve) =>
                  setTimeout(() => {
                      resolve();
                  }, 1)
              );
          }

          bars[j].style.backgroundColor = "darkblue";
          bars[k].style.backgroundColor = "darkblue";
          bars[k].style.height = temp1;
          bars[k].childNodes[0].innerText = temp2;
          await new Promise((resolve) =>
              setTimeout(() => {
                  resolve();
              }, 600)
          );

          bars[j].style.backgroundColor = "#6B6B71";

          bars[k].style.backgroundColor = "#6B6B71";
          await new Promise((resolve) =>
              setTimeout(() => {
                  resolve();
              }, 300)
          );
        }
     }
      for (var x = 0; x < 95; x++) {
          bars[x].style.backgroundColor 
              = "rgb(49, 226, 13)";
      }

    },


    reset: function()
    {
      window.location.reload();
      
    },

  }
}
</script>

<style>

.mySlides {
	display: none;
}
button{
  background:none;
  border:none;
  margin:0;
  padding:0;
  cursor: pointer;
  transition: all .2s ease-in-out;
  color:white;
  border-radius: 50%;

}
button:hover{
  box-shadow:
  0 0 20px 2px #fff;
  transform: scale(1.5);
}
body {
background-color: #2D2D2F;
overflow: hidden;
font-family: 'Signika', sans-serif;
}

.title {
  width: 100vw;
  text-align: center;
  color: #EAE6E5;
}

.data-container {
	width: 100vw;
	height: 80vh;
	position: relative;
	margin: 0;
}

.bar {
	width: 1vw;
  padding: none;
	position: absolute;
	left: 0;
	bottom: 0;
	background-color: #EAE6E5;
	transition: 0.2s all ease;
}
.nav{
  width: 100vw;
  text-align: center;
  padding-top: 20px;
}
.bar_id {
  color: white;
  display: none;
}
.btn1 {
	padding: 12px;
  display: inline;
}
.btn2 {
	padding: 12px;
  display: inline;
}

.imgbutton{
  fill:white;
}
.btn2 {
  position: relative;
  border-bottom: 1px dotted black;
}

.btn2:before {
  content: attr(data-hover);
  visibility: hidden;
  opacity: 0;
  width: 140px;
  background-color: black;
  color: #fff;
  text-align: center;
  border-radius: 5px;
  padding: 5px 0;
  transition: opacity 1s ease-in-out;

  position: absolute;
  z-index: 1;
  left: -75%;
  top: -50%;
}

.btn2:hover:before {
  opacity: 1;
  visibility: visible;
}
</style>
