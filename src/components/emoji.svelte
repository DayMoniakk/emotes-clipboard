<script>
    export let link;
    export let onHandleClipboardNotification;

    let displayImage = true;

    async function copyToClipboard(content){
        try {
            await navigator.clipboard.writeText(content);
            onHandleClipboardNotification();
        } catch (error) {
            console.error("Failed to copy to clipboard: ", error);
        }
    }

    function handleClick(){
        copyToClipboard(link);
    }

    function handleKeyDown(event){
        if (event.key === "Enter"){
            handleClick();
        }
    }

    function handleImageError(){
        displayImage = false;
    }
</script>

{#if displayImage}
    <img src={link} alt="" on:click={handleClick} on:keydown={handleKeyDown} on:error={handleImageError}>
{/if}

<style>
    img{
        padding: 5px;
        width: 65px;
        height: 65px;
        border-radius: 10px;
        cursor: pointer;
        transition: background-color 0.2s, filter 0.2s;
        background-color: #2b2e336c;
        object-fit: contain;
    }
    img:hover{
        background-color: #40454d;
        filter: brightness(1.2);
    }
</style>