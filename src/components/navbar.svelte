<script>
    export let onHelpClick;

    function handleKeyDown(event){
        if (event.key === "Enter"){
            onHelpClick();
        }
    }
</script>

<nav>
    <h1>Emotes Clipboard</h1>
    <h2>Use your favorites emotes on discord without nitro !</h2>

    <h3 on:click={onHelpClick} on:keydown={handleKeyDown}>?</h3>
</nav>

<style>
    *{
        margin: 0;
    }

    nav{
        background-color: #25282c;
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        border-bottom: 4px solid #1c1f22;
    }

    h1{
        color: rgb(238, 235, 37);
        padding: 5px;
    }

    h2{
        color: rgb(128, 127, 107);
        font-size: medium;
        padding: 5px;
        font-weight: 100;
    }

    h3{
        position: absolute;
        right: 20px;
        top: 20px;
        color: rgb(121, 121, 121);
        border: 2px solid rgb(121, 121, 121);
        border-radius: 5px;
        padding: 5px 10px 5px 10px;
        cursor: pointer;
        transition: background-color 0.2s, color 0.2s, border 0.2s;
    }
    h3:hover{
        background-color: white;
        color: black;
        border: 2px solid black;
    }
</style>