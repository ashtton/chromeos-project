<script>
    import Browser from '$lib/browser.svelte'

    let browserOpen = false
    let browserLink = ""
</script>


<Browser open={browserOpen} link={browserLink} />

<div class="container">
    <div class="search">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M512 256C512 397.4 397.4 512 256 512C114.6 512 0 397.4 0 256C0 114.6 114.6 0 256 0C397.4 0 512 114.6 512 256zM256 48C141.1 48 48 141.1 48 256C48 370.9 141.1 464 256 464C370.9 464 464 370.9 464 256C464 141.1 370.9 48 256 48z"/></svg>
    </div>

    <div class="icons">
        <div>
            <img alt="google chrome" src="/google-chrome.svg" on:click={() => {
                browserOpen = !browserOpen
                browserLink = {
                    title: "Information",
                    link: "/info"
                }
            }} />
            <hr style="visibility: {browserOpen ? 'visible' : 'hidden'}">
        </div>
        <div>
            <img alt="google docs" src="/google-docs.svg" on:click={() => {
                browserOpen = !browserOpen
                browserLink = {
                    title: "Google Docs",
                    link: "https://docs.google.com/document/d/1GitSsnWlWuNU5iWuz-loA5PldM6bO6veI0z9RGYRiWE/edit?usp=sharing"
                }
            }} />
        </div>
        <div>
            <img alt="google presentation" src="/google-slides.svg" on:click={() => {
                browserOpen = !browserOpen
                browserLink = {
                    title: "Google Slides",
                    link: "https://docs.google.com/presentation/d/1bv2Nc0W-SsFSb8fGjB5D--7C8Ha3qOZ90RF-B6fM1lU/edit?usp=sharing"
                }
            }} />
        </div>
    </div>

    <div class="menu">
        <div>
            <span>Feb 27</span>
        </div>
        <div>
            <span>
                <span>12:31</span>
                <span>EXTD</span>
                <svg class="wifi" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M54.2 202.9C123.2 136.7 216.8 96 320 96s196.8 40.7 265.8 106.9c12.8 12.2 33 11.8 45.2-.9s11.8-33-.9-45.2C549.7 79.5 440.4 32 320 32S90.3 79.5 9.8 156.7C-2.9 169-3.3 189.2 8.9 202s32.5 13.2 45.2 .9zM320 256c56.8 0 108.6 21.1 148.2 56c13.3 11.7 33.5 10.4 45.2-2.8s10.4-33.5-2.8-45.2C459.8 219.2 393 192 320 192s-139.8 27.2-190.5 72c-13.3 11.7-14.5 31.9-2.8 45.2s31.9 14.5 45.2 2.8c39.5-34.9 91.3-56 148.2-56zm64 160a64 64 0 1 0 -128 0 64 64 0 1 0 128 0z"/></svg>
                <svg class="battery" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><!--! Font Awesome Pro 6.3.0 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2023 Fonticons, Inc. --><path d="M80 160c-8.8 0-16 7.2-16 16V336c0 8.8 7.2 16 16 16H464c8.8 0 16-7.2 16-16V176c0-8.8-7.2-16-16-16H80zM0 176c0-44.2 35.8-80 80-80H464c44.2 0 80 35.8 80 80v16c17.7 0 32 14.3 32 32v64c0 17.7-14.3 32-32 32v16c0 44.2-35.8 80-80 80H80c-44.2 0-80-35.8-80-80V176z"/></svg>
            </span>
        </div>
    </div>
</div>

<style>
    hr {
        margin: 0;
        width: 0.7rem;
        visibility: hidden;
        position: absolute;
        right: 0.6rem;
    }

    .container {
        width: 100%;
        position: absolute;
        bottom: 0;
        background-color: #3d494c;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        border-radius: 1rem 1rem 0 0;
        color: white;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        align-items: center;
        font-size: 0.9rem;
    }

    .search {
        margin-left: 0.3rem;
        padding: 0.4rem;
        display: flex;
        background-color: #4a5b5d;
        border-radius: 1rem;
        cursor: pointer;
        max-width: 1rem;
        justify-content: center;
    }

    .search svg {
        width: 0.9rem;
        height: 0.9rem;
        fill: white;
    }

    .icons {
        display: flex;
        justify-content: center;
        gap: 1rem;
    }

    .icons div {
        position: relative;
    }

    .menu {
        display: flex;
        margin-right: 0.3rem;
        gap: 0.2rem;
        justify-content: end;
    }

    .menu div {
        background-color: #4a5b5d;
        padding: 0.7rem;
    }

    .menu div:first-child {
        border-radius: 1rem 0.2rem 0.2rem 1rem;
    }

    .menu div:last-child {
        border-radius: 0.2rem 1rem 1rem 0.2rem;
    }

    .menu div span {
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .wifi {
        height: 1rem;
        width: 1rem;
        fill: white;
    }

    .battery {
        transform: rotate(-90deg);
        height: 1rem;
        width: 1rem;
        fill: white;
    }

    .icons img {
        width: 2rem;
        height: 2rem;
    }
</style>
