<script>
    import { onMount } from "svelte";
    import { FFmpeg } from "@ffmpeg/ffmpeg";
    import { browser } from "$app/environment";
    let ffmpeg = null;
    onMount(async ()=>{
        ffmpeg = new FFmpeg();
        console.log(ffmpeg);
        if (browser){
            await ffmpeg.load();
        }
    })




</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
