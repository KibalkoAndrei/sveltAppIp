<script>
    import Table from "./pageIPtable.svelte";
    let element = 1;
    console.log(element)

</script>

<div class="menu">
    <h2>222</h2>

    <button on:click={() => element+1}>
        настройки
    </button>
    
    <button>
        +сеть
    </button>
    <button>
        +сеть
    </button>
    <button>
        .
    </button>
</div>




<div>
    <h2>222</h2>
    {#if element%2==0}
    <Table></Table>
    {/if}
    <Table></Table>
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



