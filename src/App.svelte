<script lang="ts">
import Hangman from './lib/Hangman.svelte'

let errors = 0

const checkErrors = () => {
  if (errors < 6) {
    errors = errors + 1
  } else {
    errors = 0
  }
}
</script>

<main class="flex flex-col max-w-6xl mx-auto justify-center items-center w-screen h-screen">
  <h1 class="text-stone-800 font-bold text-6xl my-12">Hangman Game</h1>
  <div class="flex w-full bg-stone-400">
    <div class="w-full">
      <Hangman errors={errors} />
    </div>
    <div class="flex justify-between items-start p-6 w-full">
      <div class="text-stone-800">Total errors: {errors}</div>
      <button class="inline bg-stone-600 text-stone-100 px-4 py-1 rounded hover:opacity-75" on:click={checkErrors}>{ errors === 6 ? 'Reset' : 'Click' }</button>
    </div>
  </div>
</main>
