<script>
    import Video from "./Video.svelte";
    import VideoWrapper from "./VideoWrapper.svelte";
    let show = false;
</script>

<p class="text-center mx-auto">hello</p>
<h1>Welcome to SvelteKit</h1>
<p>
    "Conversations With My Straight Boyfriends is a multimedia experience of
    dance and film influenced heavily by popular and counterculture.
    Idiosyncratic solo choreographed works of dance and film by male identifying
    heterosexuals will be vetted through an open application process. Works will
    then be selected to be adapted onto my LGBTQIA+ identifying body. I will
    then choreograph a dance and film from my LGBTQIA+ identifying body onto the
    male identifying heterosexual as an exchange. Each work that is created and
    selected will be filmed twice in the same location of the choreographer’s
    choice, once with the male identifying heterosexual choreographer and the
    second with me as the Queer identifying LGBTQIA+ body. All videos will then
    be uploaded and accompanied by an interactive website under the name of
    Conversations With My Straight Boyfriends where the choreographed projects
    will house two versions of each work created and selected. Viewers will be
    able to choose how to watch each work. The options are: 1.) with the male
    identifying heterosexual body, 2.) with my LGBTQIA+ identifying body, or 3.)
    with the male identifying heterosexual body overlaid with my identifying
    LGBTQIA+ body showing both versions simultaneously with an opacity effect.
    Each work will be accompanied with two short essays about the meaning of the
    works and locations chosen. One essay written by the heterosexual
    choreographer and one essay written by myself as the LGBTQIA+ performer and
    then vice versa when I am the choreographer and they are the heterosexual
    performer. Viewers will have the option to read each essay separately or
    read a combined interlaced version that consists of parts from both essays
    randomly stitched together by an algorithm generator. This project is
    designed to push the normative view of binaries related to gender and
    sexuality that are perpetuated in dance and everyday life to acknowledge the
    interactions of authority and artistry with gender and self-expression in
    different bodies. Through viewing and reading, participants in the project
    and viewers who observe the project will be challenged to acknowledge and
    explore their view of what gender and sexuality is, beyond the binary. The
    final work completed will be the films and essays that will be housed
    permanently on the interactive website, Conversations With My Straight
    Boyfriends. The general public will be free to access the content of the
    website as often and frequently as they choose."
</p>

<button on:click={() => (show = !show)}>
    <p class="bg-pink-100">button</p>
</button>
{#if show}
    <VideoWrapper>
        <Video src="/demo.mp4" muted />
    </VideoWrapper>
{/if}
