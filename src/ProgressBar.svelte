<script>
  export let progress = 0
</script>

<div bp="grid">
  <div bp="offset-5@md 4@md 12@sm" class="progress-container">
    <div class="progress-bar" style="width:{progress}%;" />
  </div>
</div>

<style>
  .progress-container {
    margin: 0.2rem 0rem;
    border: solid #727070 0.1rem;
    border-radius: 0.5rem;
  }
  .progress-bar {
    height: 1.5rem;
    background-color: rgb(32, 245, 4);
    border-top-left-radius: 0.5rem;
    border-bottom-left-radius: 0.5rem;
  }
</style>
