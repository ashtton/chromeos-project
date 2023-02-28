<script>
    export let open;
    export let link;
</script>

{#if open}
    <div class="container">
        <div class="header">
            <div class="tabs">
                <div class="tab">
                    {link.title}
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M376.6 84.5c11.3-13.6 9.5-33.8-4.1-45.1s-33.8-9.5-45.1 4.1L192 206 56.6 43.5C45.3 29.9 25.1 28.1 11.5 39.4S-3.9 70.9 7.4 84.5L150.3 256 7.4 427.5c-11.3 13.6-9.5 33.8 4.1 45.1s33.8 9.5 45.1-4.1L192 306 327.4 468.5c11.3 13.6 31.5 15.4 45.1 4.1s15.4-31.5 4.1-45.1L233.7 256 376.6 84.5z"/></svg>
                </div>
            </div>
            <div class="things">
                <svg class="arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z"/></svg>
                <svg class="arrow rotate" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l160 160c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L109.2 288 416 288c17.7 0 32-14.3 32-32s-14.3-32-32-32l-306.7 0L214.6 118.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-160 160z"/></svg>
                <svg class="refresh" fill="black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M370.3 160H320c-17.7 0-32 14.3-32 32s14.3 32 32 32H448c17.7 0 32-14.3 32-32V64c0-17.7-14.3-32-32-32s-32 14.3-32 32v51.2L398.4 97.6c-87.5-87.5-229.3-87.5-316.8 0s-87.5 229.3 0 316.8s229.3 87.5 316.8 0c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0c-62.5 62.5-163.8 62.5-226.3 0s-62.5-163.8 0-226.3s163.8-62.5 226.3 0L370.3 160z"/></svg>
                <div class="search">
                    <span>{link.link === "/info" ? "https://whatschromeos.com/" : link.link}</span>
                </div>
                <svg class="menu" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
            </div>
        </div>
        <iframe src={link.link} title="description"></iframe>
    </div>
{/if}

<style>
    .container {
        width: 100%;
        position: absolute;
    }

    .header {
    }

    .tabs {
        height: 2rem;
        background-color: #e7eaed;
    }

    .things {
        height: 2rem;
        background-color: white;
        border-bottom: 1px solid rgba(0, 0, 0, 10%);
        display: flex;
        align-items: center;
    }

    .container iframe {
        border: 0;
        height: 41.7rem;
        width: 100%;
    }

    .arrow {
        height: 1rem;
        width: 1rem;
        fill: #babcbe;
        margin-left: 1rem;
    }

    .refresh {
        width: 1rem;
        height: 1rem;
        fill: #797c81;
        margin-left: 1rem;
    }

    .search {
        margin-left: 1rem;
        width: 80rem;
        background-color: #e7eaed !important;
        border-radius: 1rem;
        padding: 0.2rem 0.6rem;
    }

    .search span {
        font-size: 0.7rem;
        color: #7b7c7e;
    }

    .rotate {
        transform: rotate(180deg);
    }

    .menu {
        margin-left: 1rem;
        width: 1rem;
        height: 1rem;
        fill: #797c81;
    }

    .tabs {
        display: flex;
    }

    .tab {
        background-color: white !important;
        color: #a3a5a6;
        font-size: 0.8rem;
        border-radius: 0.7rem 0.7rem 0 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-left: 1rem;
        padding-right: 1rem;
    }

    .tab svg {
        height: 0.5rem;
        width: 0.5rem;
        margin-left: 0.5rem;
        fill: #878a8b;
    }
</style>