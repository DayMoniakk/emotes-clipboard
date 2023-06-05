<script>
    let modalVisible = false;

    export function onHelpButtonClicked(){
        modalVisible = true;
    }

    function handleExit(){
        modalVisible = false;
    }

    function handleKeyDown(event){
        if (event.key === "Enter"){
            handleExit();
        }
    }
</script>

{#if modalVisible}
    <div class="container" on:click={handleExit} on:keydown={handleKeyDown}>
        <div class="modal">
            <div class="modal-title">
                <h1>How to use ?</h1>
            </div>
            <ul class="help-content">
                <li>Click on the emote of your choice.</li>
                <li>You will get a link, paste the link in your Discord message.</li>
                <li>Enjoy people reactions !</li>
            </ul>
            <div class="modal-title modal-title-limitations">
                <h1>Limitations</h1>
            </div>
            <ul class="help-content">
                <li>Some servers may disable embed contents, so only the link will be visible.</li>
                <li>Some servers may also restrict the usage of links.</li>
            </ul>
        </div>
        <span class="span-hint">Click anywhere to close this modal !</span>
    </div>
{/if}

<style>
    .container{
        background-color: rgba(0, 0, 0, 0.589);
        width: 100%;
        height: 100vh;
        position: fixed;
        top: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .modal{
        background-color: #25282c;
        width: 75%;
        max-width: 800px;
        display: flex;
        flex-direction: column;
    }

    .modal-title{
        color: rgb(238, 235, 37);
        background-color: #1d2024;
        width: 100%;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-bottom: 2px solid rgb(175, 173, 27);
    }
    
    .modal-title-limitations{
        color: rgb(214, 0, 0);
        border-bottom: 2px solid rgb(214, 0, 0);
    }

    .help-content{
        color: white;
        font-weight: 300;
        font-size: 20px;
        list-style: decimal;
    }
    .help-content li{
        padding-bottom: 10px;
    }

    .span-hint{
        color: rgb(201, 200, 200);
        font-weight: 100;
    }
</style>