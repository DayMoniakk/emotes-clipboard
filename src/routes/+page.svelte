<script>
    import "../styles/global.css"

    import Navbar from "../components/navbar.svelte";
    import EmojisHolder from "../components/emojisHolder.svelte";
    import Footer from "../components/footer.svelte";
    import HelpModal from "../components/helpModal.svelte";

    let helpModal;
    let emojisHolder;
    let faviconUrl;

    $: if (emojisHolder) {
        faviconUrl = emojisHolder.getRandomEmoji();
    }

    function onHelpButtonClicked(){
        helpModal.onHelpButtonClicked();
    }
</script>

<svelte:head>
    <title>Emotes Clipboard</title>
    <link rel="shortcut icon" href={faviconUrl} type="image/x-icon">
</svelte:head>

<Navbar onHelpClick={onHelpButtonClicked}/>
<EmojisHolder bind:this={emojisHolder}/>
<HelpModal bind:this={helpModal}/>
<Footer/>