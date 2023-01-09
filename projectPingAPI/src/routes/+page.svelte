<script>
    import Table from "./pageIPtable.svelte";
    import Chart from './Chart.svelte';
    let buttonOpen = {
        Ip: !true,
        chart: !true
    }
    console.log(buttonOpen.Ip)
</script>

<div class="menu">
    <h2>menu</h2>

    <button on:click={() => {buttonOpen.Ip = !buttonOpen.Ip}}>
        список адресов
    </button>
    
    <button on:click={buttonOpen.chart = !buttonOpen.chart}>
        график
    </button>
    <button>
        
    </button>
    <button>
    </button>
    <button>
    </button>
    <button>
    </button>
    <button>
    </button>
    <button>
    </button>
</div>




<div>
    <h2>222</h2>
    {#if buttonOpen.Ip==true}
    <Table></Table>
    {/if}
    
</div>


<style>
    h2{
        text-align: center;
    }

    .menu{
        display: flex;
        flex-direction: column;
        position: fixed;
        top: 0;
        left: 30px;
        height: 100%;
        width: 200px;
        border-right: 1px black solid;
        
    }

    button {
        height: 30px;
        margin-right: 30px;
        margin-top: 5px;
        background-color: wheat;
        cursor: pointer;
    }
</style>


