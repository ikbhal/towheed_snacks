<script>

export let dateString = "2021-11-03"; //yyyy-mm-dd
export let takenMoneyForSnack= false;
</script>

<div class="noSnackMoneyCheck">
    <input type="date" bind:value={dateString}/> 
    <label>
        <input type=checkbox checked={takenMoneyForSnack}>
        Yes! Taken money for snack
    </label>
</div>

<style>
.noSnackMoneyCheck{
    border-color:0 solid #d2d6dc;
    background-color: #db930e79;
    border-radius: 0.375rem;
    box-shadow:0 1px 2px 0 rgba(0,0,0,.05);
    color: white;
    margin: 20px;
    padding: 20px;

}
</style>