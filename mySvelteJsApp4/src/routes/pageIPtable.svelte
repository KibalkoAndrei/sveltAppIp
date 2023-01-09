<script>
    let value = '';
    function RandomItem(min, max) {
        min = Math.ceil(min);
        max = Math.floor(max);
        return Math.floor(Math.random() * (max - min) + min);
    }
    let listIp = [
        {id:1, ip: '87.240.137.164', itemBite: [RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50)], time: [RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50)]}
    ]
  

    const addIp = () => {
        listIp = listIp.concat([{
            id: Date.now(),
            ip: value,
            itemBite: [RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50)],
            time: [RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50),RandomItem(30, 50)]
        }]);
    }
    
</script>


<div class="block-table">
    <h1>настройки</h1>
    <div class="form-table">
        <input type="text" bind:value>
        <button class="start-btn" on:click={addIp}>START</button>
    </div>
    <table border=".5px" cellspacing=0 cellpadding=10>
        <tr>
            <td>IP</td>
            <td>вес пакетов</td>
           <td>время приема-передачи пакетов</td>
        </tr>
        {#each listIp as ipp}
            <tr>
                <td>{ipp.ip}</td>
                <td>{ipp.itemBite.map((bite) => `байт:${bite}   `)}</td>
                <td>{ipp.time.map((bite) => `${bite}ms   `)}</td>
            </tr>
        {/each}
    </table>
</div>

<style>
    .block-table {
        display: block;
        margin-left: 50%;
        margin-right: 50%;
        margin-top: 50px;
    }

    .form-table {
        display: flex;
        margin-bottom: 60px;
    }
    .start-btn {
        margin-left: 50px;
        background-color: brown;
    }
</style>