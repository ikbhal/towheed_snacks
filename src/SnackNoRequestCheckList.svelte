<script>
import SnackMoney from './SnackMoney.js';
import SnackNoRequestCheck from './SnackNoRequestCheck.svelte';
let startDate = new Date(2021, 11, 3); //const d = new Date(2018, 11, 24);
let endDate = new Date(2021, 11, 9);// includin ending date 3, 4, 5,     6,   7, 8, 9

var getDateArray = function(start, end) {
    var arr = new Array(),
    dt = new Date(start);
    while (dt <= end) {
        arr.push(new Date(dt));
        dt.setDate(dt.getDate() + 1);
    }
    return arr;
}

var fmtDate = (dt) => dt.toISOString().split('T')[0]

var dateArr = getDateArray(startDate, endDate);
let snackMoneyArr = dateArr.map(dt => new SnackMoney(fmtDate(dt), false));

</script>
<div class="noSnackMoneyCheckList">
    <h3>Snack Money Taken this day or not</h3>
    {#each snackMoneyArr as snackMoneyEle}
        <SnackNoRequestCheck dateString={snackMoneyEle.date} takenMoneyForSnack={snackMoneyEle.taken} />
    {/each}
</div> 