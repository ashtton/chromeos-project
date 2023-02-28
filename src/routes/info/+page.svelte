<script>
    let state = 0
    let map = new Map();
    map.set(0, "Does the system have system health monitors?")
    map.set(1, "Is the system compatible with hardware drivers?")
    map.set(2, "Does the system run most software?")
    map.set(3, "Is there a specific function this OS is designed for?")
    map.set(4, "How much does it cost?")
    map.set(5, "Is chrome os bulky?")
    map.set(6, "Is chrome os friendly?")
    map.set(7, "Is chrome os easy to install?")
    map.set(8, "The history of Chrome OS.")
    map.set(9, "What makes it different?")
</script>

<div class="container">
    <div class="content">
        <div class="title">{map.get(state)}</div>
        <div class="description">
            {#if state === 0}
                Yes. You can access the chrome os system health monitors fairly easy by navigating to
                <code>'chrome://sys-internals/'</code> which will show you information about your hardware.
            {:else if state === 1}
                Yes. Chrome OS is compatible with a majority of hardware drivers.
                Chrome OS is built off of <a href="ssdf">Linux</a> which has lots of drivers made for it.
                Because of the fact that it is built off of Linux, the drivers that you're looking for
                may be third party rather than being made by the original company.
            {:else if state === 2}
                By default, Chrome OS will only run a handful of chrome extensions and google app store apps.
                If you are an administrator and put the Chromebook is developer mode however, you can run any
                app that usually runs on Linux.
            {:else if state === 3}
                The whole purpose of Chrome OS is to mainly run web applications and not much more.
            {:else if state === 4}
                Chrome OS is a free, open source software.
            {:else if state === 5}
                Chrome OS is between 1GB and 3GB in size which means it's not bulky whatsoever.
            {:else if state === 6}
                Chrome OS is extremely user friendly, considering it's literally just a web browser.
            {:else if state === 7}
                Chrome OS is extremely easy to install, all you have to do is download the image onto
                a USB stick and you're good to go.
            {:else if state === 8}
                Chrome OS was created by Google in 2011 for Chromebooks to run. Their vision with Chromebooks is
                to be a cheaper alternative to a computer while still providing access to the neccessities like the web.
            {:else if state === 9}
                Chrome OS is very different from other operating systems because it's essentially just a web browser.
                You can breathe new life into older machines by installing chrome os onto them.
            {/if}
        </div>
        <div class="buttons">
            <div>
                {#if state !== 0}
                    Previous:<br> <strong on:click={() => state -= 1}>{map.get(state - 1)}</strong>
                {/if}
            </div>
            <div>
                {#if state !== 9}
                    Next:<br> <strong on:click={() => state += 1}>{map.get(state + 1)}</strong>
                {/if}
            </div>
        </div>

    </div>
</div>

<style>
    :global(body) {
        margin: 0;
        font-family: Arial, serif;
        background-color: white;
    }

    .container {
        max-width: 800px;
        margin: auto;
    }

    .title {
        margin-bottom: 1rem;
        margin-top: 3rem;
        font-size: 3rem;
        font-weight: bold;
    }

    .buttons {
        display: flex;
        justify-content: space-between;
        margin-top: 3rem;
    }

    .buttons strong {
        cursor: pointer;
    }

    .buttons strong:hover {
        color: gray;
    }

    .description {
        font-size: 1.2rem;
    }

    #pass {
        font-weight: bold;
    }

    @media(max-width: 800px) {
        .container {
            margin-left: 2rem;
            margin-right: 2rem;
            margin-bottom: 2rem;
        }
    }
</style>