<script>
  import { onMount } from 'svelte';

  export let src = '';
  // export let poster = '';
  export let autoplay = true;
  export let muted = false;
  export let controls = false;
  export let loop = true;

  let videoElement;
  let errorMessage = '';

  $: if (!src) {
    errorMessage = 'Error: Video source is undefined';
  } else {
    errorMessage = '';
  }

  onMount(() => {
    if (videoElement) {
      videoElement.addEventListener('error', (e) => {
        console.error('Video error:', e);
        errorMessage = `Error: ${videoElement.error?.message || 'Unknown error'}`;
      });
    }
  });
</script>

{#if src}
  <video
    bind:this={videoElement}
    {src}
    {autoplay}
    {controls}
    {muted}
    {loop}
    playsinline
  >
    Your browser does not support the video tag.
  </video>
{:else}
  <p>No video source provided</p>
{/if}

{#if errorMessage}
  <p style="color: red;">{errorMessage}</p>
{/if}

<style>
  video {
    max-width: 100%;
    height: auto;
  }
</style>