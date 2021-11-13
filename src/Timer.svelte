<script>
 import ProgressBar from './ProgressBar.svelte'
</script>

<!------------------------------------------ HTML section ----------------->

<div bp="grid">
 <h2 bp="offset-5@md 4@md 12@sm">Seconds left :</h2>
</div>

<ProgressBar/>

<button class="start">
 start
</button>
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
</style>