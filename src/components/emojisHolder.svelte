<script>
    import { fly } from 'svelte/transition';

    import Emoji from "./emoji.svelte";

    let clipboardNotificationVisible = false;

    export function handleClipboardNotification(){
        if (clipboardNotificationVisible) return;

        clipboardNotificationVisible = true;

        setTimeout(() => {
            clipboardNotificationVisible = false;
        }, 4000);
    }

    export function getRandomEmoji(){
    return links[Math.floor(Math.random() * links.length)];
    }

    let links = [
        "https://cdn.7tv.app/emote/603cac391cd55c0014d989be/4x.webp",
        "https://cdn.7tv.app/emote/60ae8d9ff39a7552b658b60d/4x.webp",
        "https://cdn.7tv.app/emote/60aec2196cfcffe15f4e4f93/4x.webp",
        "https://cdn.7tv.app/emote/60a487509485e7cf2f5a6fa7/4x.webp",
        "https://cdn.7tv.app/emote/6042089e77137b000de9e669/4x.webp",
        "https://cdn.7tv.app/emote/60aee9d5361b0164e60d02c2/4x.webp",
        "https://cdn.7tv.app/emote/60b14a737a157a7f3360fb32/4x.webp",
        "https://cdn.7tv.app/emote/60ae3e54259ac5a73e56a426/4x.webp",
        "https://cdn.7tv.app/emote/60b0c36388e8246a4b120d7e/4x.webp",
        "https://cdn.7tv.app/emote/60af769d2c36aae19e32ec9d/4x.webp",
        "https://cdn.7tv.app/emote/60bcb44f7229037ee386d1ab/4x.webp",
        "https://cdn.7tv.app/emote/613937fcf7977b64f644c0d2/4x.webp",
        "https://cdn.7tv.app/emote/60aea1dbf39a7552b6ccb61d/4x.webp",
        "https://cdn.7tv.app/emote/60ae2376b2ecb015058f4aa7/4x.webp",
        "https://cdn.7tv.app/emote/604a93564d948c001460998b/4x.webp",
        "https://cdn.7tv.app/emote/612e638afc02cc1a1f411b2d/4x.webp",
        "https://cdn.7tv.app/emote/60aef3aea564afa26e686d8c/4x.webp",
        "https://cdn.7tv.app/emote/603caea243b9e100141caf4f/4x.webp",
        "https://cdn.7tv.app/emote/603eace1115b55000d7282db/4x.webp",
        "https://cdn.7tv.app/emote/6141f07a962a60904864895e/4x.webp",
        "https://cdn.7tv.app/emote/60af1ba684a2b8e655387bba/4x.webp",
        "https://cdn.7tv.app/emote/60420e5a77137b000de9e676/4x.webp",
        "https://cdn.7tv.app/emote/60aef48211a994a4ac3e00db/4x.webp",
        "https://cdn.7tv.app/emote/60d431e38090e67e368eb5df/4x.webp",
        "https://cdn.7tv.app/emote/6268904f4f54759b7184fa72/4x.webp",
        "https://cdn.7tv.app/emote/60e1b8f4dac155e3661b8090/4x.webp",
        "https://cdn.7tv.app/emote/60aef2b6361b0164e690f782/4x.webp",
        "https://cdn.7tv.app/emote/60e5bbe5a69fc8d27f4d3fe5/4x.webp",
        "https://cdn.7tv.app/emote/634493ce05c2b2cd864d5f0d/4x.webp",
        "https://cdn.7tv.app/emote/60411e5bcf6746000db10353/4x.webp",
        "https://cdn.7tv.app/emote/61b5bfef523b4785d7c20537/4x.webp",
        "https://cdn.7tv.app/emote/60ae9a57ac03cad60771b2d8/4x.webp",
        "https://cdn.7tv.app/emote/610dc478d86cd785a47384b1/4x.webp",
        "https://cdn.7tv.app/emote/610dc478d86cd785a47384b1/4x.webp",
        "https://cdn.7tv.app/emote/63a8d3d9c05f5803112d8218/4x.webp",
        "https://cdn.7tv.app/emote/60aeeb28a564afa26ee7a7f2/4x.webp",
        "https://cdn.7tv.app/emote/63071b80942ffb69e13d700f/4x.webp",
        "https://cdn.7tv.app/emote/60cb2e0194befb7c93dbe281/4x.webp",
        "https://cdn.7tv.app/emote/619e250deecae7a725bcb696/4x.webp",
        "https://cdn.7tv.app/emote/605304ed8c870a000de38b6d/4x.webp",
        "https://cdn.7tv.app/emote/60ae9edaf6a2c3b332b57301/4x.webp",
        "https://cdn.7tv.app/emote/60b2103ee67fbb9dd71cb3fc/4x.webp",
        "https://cdn.7tv.app/emote/634494e194790c62d1eee91f/4x.webp",
        "https://cdn.7tv.app/emote/60af1b5a35c50a77926314ad/4x.webp",
        "https://cdn.7tv.app/emote/61ebede31a1b2a6e7324d897/4x.webp",
        "https://cdn.7tv.app/emote/60afb45412f90fadd65fb1a8/4x.webp",
        "https://cdn.7tv.app/emote/60ae6c1386fc40d488e1ebf9/4x.webp",
        "https://cdn.7tv.app/emote/603d32e968a0fc000dfdda1a/4x.webp",
        "https://cdn.7tv.app/emote/603cb9fd73d7a5001441f9b4/4x.webp",
        "https://cdn.7tv.app/emote/60b012a8e5a579561100b67f/4x.webp",
        "https://cdn.7tv.app/emote/60af105db38361ea91a6b535/4x.webp",
        "https://cdn.7tv.app/emote/60b891c3db8410b2f37b5deb/4x.webp",
        "https://cdn.7tv.app/emote/60ae3804259ac5a73e2bff3d/4x.webp",
        "https://cdn.7tv.app/emote/61f4050697d743f38801127b/4x.webp",
        "https://cdn.7tv.app/emote/6063c87af4dc10001426b915/4x.webp",
        "https://cdn.7tv.app/emote/60b75ba655c320f0e86936c9/4x.webp",
        "https://cdn.7tv.app/emote/603caa69faf3a00014dff0b1/4x.webp",
        "https://cdn.7tv.app/emote/60420b7b77137b000de9e671/4x.webp",
        "https://cdn.7tv.app/emote/603ccedf2c7b4500143b46d7/4x.webp",
        "https://cdn.7tv.app/emote/60b0c3ddb254a5e16b87afc4/4x.webp",
        "https://cdn.7tv.app/emote/639938bf1e2f45552fe4fa03/4x.webp",
        "https://cdn.7tv.app/emote/60b3f949db203df7cd04abe9/4x.webp",
        "https://cdn.7tv.app/emote/60aeb2da5174a619db6cd0e7/4x.webp",
        "https://cdn.7tv.app/emote/60aeb5428a2d7f04b130bddb/4x.webp",
        "https://cdn.7tv.app/emote/60ae480e5d3fdae583b37042/4x.webp",
        "https://cdn.7tv.app/emote/603ea239284626000d068886/4x.webp",
        "https://cdn.7tv.app/emote/603fe923115b55000d728314/4x.webp",
        "https://cdn.7tv.app/emote/60ae53ca0e35477634dd6138/4x.webp",
        "https://cdn.7tv.app/emote/6042290277137b000de9e68d/4x.webp",
        "https://cdn.7tv.app/emote/60b1d7f42985f38fb4fbfbaa/4x.webp",
        "https://cdn.7tv.app/emote/6043181d1d4963000d9dae39/4x.webp",
        "https://cdn.7tv.app/emote/60b07f6fad7fb4b50b55fdd5/4x.webp",
        "https://cdn.7tv.app/emote/63befa0f23e3c08ccb765d80/4x.webp",
        "https://cdn.7tv.app/emote/6042091777137b000de9e66b/4x.webp",
        "https://cdn.7tv.app/emote/614234ad0969108b6718fa15/4x.webp",
        "https://cdn.7tv.app/emote/61ddb0dc27a4f6d6544ef135/4x.webp",
        "https://cdn.7tv.app/emote/61c53b8c1cc80462ef2d0fe8/4x.webp",
        "https://cdn.7tv.app/emote/60ae31b5259ac5a73efa8dc0/4x.webp",
        "https://cdn.7tv.app/emote/60af42a657a061bbef294e17/4x.webp",
        "https://cdn.7tv.app/emote/61de32c05001b6b33b2e32c8/4x.webp",
        "https://cdn.7tv.app/emote/60f4e98ce57bec02166796a5/4x.webp",
        "https://cdn.7tv.app/emote/604137d3cf6746000db10354/4x.webp",
        "https://cdn.7tv.app/emote/62d5a2e83ae7e18b633344d7/4x.webp",
        "https://cdn.7tv.app/emote/60f9ef1115758a7f9af1fe3a/4x.webp",
        "https://cdn.7tv.app/emote/623c29a61aeb248de8494e7c/4x.webp",
        "https://cdn.7tv.app/emote/60ae8c9b3c27a8b79caf0ab6/4x.webp",
        "https://cdn.7tv.app/emote/61500f246251d7e000daa3ca/4x.webp",
        "https://cdn.7tv.app/emote/62a27a7fb12d7075e259f113/4x.webp",
        "https://cdn.7tv.app/emote/61ad779c15b3ff4a5bb9a785/4x.webp",
        "https://cdn.7tv.app/emote/61e9720462858c64061279cb/4x.webp",
        "https://cdn.7tv.app/emote/6101571d04b1d2e5b2c4f8a2/4x.webp",
        "https://cdn.7tv.app/emote/605305868c870a000de38b6f/4x.webp",
        "https://cdn.7tv.app/emote/60b013434d83b66c443fc71a/4x.webp",
        "https://cdn.7tv.app/emote/60c0cc44ff4047301e33bb96/4x.webp",
        "https://cdn.7tv.app/emote/60c43d1156d255581fcfb7f1/4x.webp",
        "https://cdn.7tv.app/emote/60e857ca401af27eed2f6a4e/4x.webp",
        "https://cdn.7tv.app/emote/603cbab273d7a5001441f9c5/4x.webp",
        "https://cdn.7tv.app/emote/61359284baf761f5d4fd6ea1/4x.webp",
        "https://cdn.7tv.app/emote/60ae83a8229664e866a1c168/4x.webp",
        "https://cdn.7tv.app/emote/619ab73870bd995987959204/4x.webp",
        "https://cdn.7tv.app/emote/62437e6ede82a984598efad1/4x.webp",
        "https://cdn.7tv.app/emote/60bc8bb7824feec0de8f94cc/4x.webp",
        "https://cdn.7tv.app/emote/60ae473c5d3fdae583ac6d43/4x.webp",
        "https://cdn.7tv.app/emote/603cb5a2c20d020014423c65/4x.webp",
        "https://cdn.7tv.app/emote/62943c0af75a73adfdc2aa58/4x.webp",
        "https://cdn.7tv.app/emote/622f82622cbc7e45d4cac28f/4x.webp",
        "https://cdn.7tv.app/emote/60b75aa3d115b05311358a67/4x.webp",
        "https://cdn.7tv.app/emote/60bd0c4ed04a92d5b2fd5c8c/4x.webp",
        "https://cdn.7tv.app/emote/62f64c7fac5a78a39d493e54/4x.webp",
        "https://cdn.7tv.app/emote/60b40a52a30f50ff196abc1b/4x.webp",
        "https://cdn.7tv.app/emote/61ca0be212987d64d6aeae3d/4x.webp",
        "https://cdn.7tv.app/emote/60577b64ba9052000d450783/4x.webp",
        "https://cdn.7tv.app/emote/60b051de6862c44dce2de36f/4x.webp",
        "https://cdn.7tv.app/emote/61b9fa4b112f39cb68aff397/4x.webp",
        "https://cdn.7tv.app/emote/61b37fb215b3ff4a5bba5259/4x.webp",
        "https://cdn.7tv.app/emote/60ae3853b2ecb015050540d2/4x.webp",
        "https://cdn.7tv.app/emote/61e745ea3441abfa431d4469/4x.webp",
        "https://cdn.7tv.app/emote/60b28bf9407ad7d4e927d798/4x.webp",
        "https://cdn.7tv.app/emote/60ae69659627f9aff4386a61/4x.webp",
        "https://cdn.7tv.app/emote/60b1517fdb601b4ac8ed7916/4x.webp",
        "https://cdn.7tv.app/emote/61d8e0ee27a4f6d6544e33e8/4x.webp",
        "https://cdn.7tv.app/emote/60e5d610a69fc8d27f2737b7/4x.webp",
        "https://cdn.7tv.app/emote/60ba145c31abfff37bd0d280/4x.webp",
        "https://cdn.7tv.app/emote/6338a580d149695f4ca3114e/4x.webp",
        "https://cdn.7tv.app/emote/60aef4557e8706b5727a802c/4x.webp",
        "https://cdn.7tv.app/emote/6153fdd26251d7e000db05e7/4x.webp",
        "https://cdn.7tv.app/emote/60aeb2375174a619db6274dd/4x.webp",
        "https://cdn.7tv.app/emote/62313510b1ac2f158885fb66/4x.webp",
        "https://cdn.7tv.app/emote/603cb8be73d7a5001441f9ad/4x.webp",
        "https://cdn.7tv.app/emote/603ea1c1284626000d068884/4x.webp",
        "https://cdn.7tv.app/emote/60b0c3b63cadd71dffaca0ab/4x.webp",
        "https://cdn.7tv.app/emote/60aed58d722998ebe4d20b72/4x.webp",
        "https://cdn.7tv.app/emote/60aeaac8f6a2c3b332b5a9aa/4x.webp",
        "https://cdn.7tv.app/emote/60baa2643f56f4a8235d971c/4x.webp",
        "https://cdn.7tv.app/emote/60ae8aac4b1ea4526d954855/4x.webp",
        "https://cdn.7tv.app/emote/60c7687de0918991b726c26d/4x.webp",
        "https://cdn.7tv.app/emote/60af9408a3648f409a52bbdf/4x.webp",
        "https://cdn.7tv.app/emote/6063be22f4dc10001426b8fa/4x.webp",
        "https://cdn.7tv.app/emote/60afab02a3648f409af2db0f/4x.webp",
        "https://cdn.7tv.app/emote/60b15a10c5e3fb453e7fc211/4x.webp",
        "https://cdn.7tv.app/emote/630bdc0b581c4d862ef98174/4x.webp",
        "https://cdn.7tv.app/emote/62f1500d947ca7b836563f5a/4x.webp",
        "https://cdn.7tv.app/emote/60b885525d373afbd6d85264/4x.webp",
        "https://cdn.7tv.app/emote/60b052fe3cadd71dffa73929/4x.webp",
        "https://cdn.7tv.app/emote/603eaaa9115b55000d7282d8/4x.webp",
        "https://cdn.7tv.app/emote/60a95f109d598ea72fad13bd/4x.webp",
        "https://cdn.7tv.app/emote/60ae8d9ff39a7552b658b60d/4x.webp",
        "https://cdn.7tv.app/emote/60aef3e4b74ea8ff797ae5ac/4x.webp",
        "https://cdn.7tv.app/emote/610dc478d86cd785a47384b1/4x.webp",
        "https://cdn.7tv.app/emote/62b6b84c765d72b656d71f5d/4x.webp",
        "https://cdn.7tv.app/emote/60aef3aea564afa26e686d8c/4x.webp",
        "https://cdn.7tv.app/emote/60aee3d912d77014916df13d/4x.webp",
        "https://cdn.7tv.app/emote/60be4b4b62d85a778714b593/4x.webp",
        "https://cdn.7tv.app/emote/631c55da5a703c4a98db23bb/4x.webp",
        "https://cdn.7tv.app/emote/61c6c5d712987d64d6ae7d1a/4x.webp",
        "https://cdn.7tv.app/emote/604a93564d948c001460998b/4x.webp",
        "https://cdn.7tv.app/emote/60b013434d83b66c443fc71a/4x.webp",
        "https://cdn.7tv.app/emote/609f351f4c18609a1daa9303/4x.webp",
        "https://cdn.7tv.app/emote/63c325ef17a417b27a304a9e/4x.webp",
        "https://cdn.7tv.app/emote/6140ca270969108b6718d6a8/4x.webp",
        "https://cdn.7tv.app/emote/61f4050697d743f38801127b/4x.webp",
        "https://cdn.7tv.app/emote/610bc58f11ca9beb46ed7bbe/4x.webp",
        "https://cdn.7tv.app/emote/61de7282aa4c75f589d4d1c6/4x.webp",
        "https://cdn.7tv.app/emote/617666d0ffc7244d797d214f/4x.webp",
        "https://cdn.7tv.app/emote/60bb7481918e96162c51fb71/4x.webp",
        "https://cdn.7tv.app/emote/6393b8128e5faabf7c4c87da/4x.webp",
        "https://cdn.7tv.app/emote/612a803421ca87d781a04fd2/4x.webp",
        "https://cdn.7tv.app/emote/60b75ba655c320f0e86936c9/4x.webp",
        "https://cdn.7tv.app/emote/6133aa5d434bb87c45d90e6b/4x.webp",
        "https://cdn.7tv.app/emote/628e74a1ce2df92d9564b98f/4x.webp"
    ];
</script>

<div class="container">
    <div class="holder">
        {#each links as emojiLink}
            <Emoji link={emojiLink} onHandleClipboardNotification={handleClipboardNotification}/>
        {/each}

    </div>

    {#if clipboardNotificationVisible}
        <div class="clipboard-notification-holder" transition:fly="{{ y: -100, duration: 1000 }}">
            <div class="clipboard-notification">
                <h3>Copied to clipboard !</h3>
            </div>
        </div>
    {/if}
</div>

<style>
    .container{
        display: flex;
        align-items: flex-start;
        width: 100%;
        min-height: 100vh;
    }

    .holder{
        padding-top: 10px;
        width: 100%;
        height: auto;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 10px;
        padding-top: 25px;
    }

    .clipboard-notification-holder{
        position: fixed;
        top: 0;
        width: 100%;
        display: flex;
        justify-content: center;
        user-select: none;
    }

    .clipboard-notification{
        background-color: rgb(212, 209, 28);
        padding: 0 10px 0 10px;
        border-radius: 0 0 20px 20px;
    }
    .clipboard-notification h3{
        color: rgb(48, 48, 48);
    }
</style>