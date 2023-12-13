let output = document.querySelector('div')
let textbox = document.querySelector('input')
let wordsToType ="hello world this is typing";
let timeDispalyer = document.querySelector('[data-time-display]')

let time = 200;

function timer (){
  time --

  timeDispalyer.innerHTML = time
  // console.log(time);
}

let timing = setInterval(timer, 1000);

setTimeout(() => {

  clearTimeout(timing)
}, 200*1000);

textbox.oninput= (e)=>{
  for (let i = 0; i < wordsToType.length; i++) {
    const element = wordsToType[i];
    if (element == e.target.value[i]) {
      console.log(element);
    }
    
  }
}
