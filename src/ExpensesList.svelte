<script>
  import SectionTitle from "./Title.svelte";
  import Expense from "./Expense.svelte";
  export let expenses = [];
</script>

<section>
  <SectionTitle title="expense list" />
  <ul>
    {#each expenses as expense, index}
      <Expense {...expense} />
    {:else}
      <h2>Currently you have no expense</h2>
    {/each}
  </ul>
</section>
