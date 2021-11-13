<script>
 import ProgressBar from './ProgressBar.svelte'

 const totalSeconds = 20
 let secondLeft = totalSeconds
 let isRunning = false
 

 $:progress = ((totalSeconds - secondLeft) /totalSeconds) *100

 function startTimer () {
  isRunning = true
     const timer = setInterval(() => {
      console.log(timer);
     secondLeft -= 1
     if (secondLeft == 0) {
      clearInterval(timer)
      isRunning = false
      secondLeft = totalSeconds
     }
  }, 1000);
}


</script>

<!------------------------------------------ HTML section ----------------->

<div bp="grid">
 <h2 bp="offset-5@md 4@md 12@sm">Seconds left {secondLeft} :</h2>
</div>


<ProgressBar {progress}/>

<div bp="grid">
 <button disabled={isRunning} on:click={startTimer} class="start" bp="offset-5@md 4@md 12@sm"> start</button>
</div>


<!------------------------------------------ CSS section ----------------->

<style>

 h2 {
  margin: 0;
 }

 .start {
  background-color: rgba(41, 132, 175, 0.986);
  border-radius: .5rem;
  width: 100%;
  margin: .3rem;
 }
 .start[disabled] {
  background-color: rgba(58, 60, 61, 0.986);
  cursor: not-allowed;
 }
</style>