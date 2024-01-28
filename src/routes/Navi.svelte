<script lang="ts">
    import { clickOutside } from "./clickOutside";
    import { navExpand } from "./stores";
    import arrow from "$lib/arrow.svg";

    const navAction = () => {
        $navExpand = !$navExpand;
    };

    const closeNav = () => {
        $navExpand = false;
    };
</script>

<nav
    class={`navi-main ${$navExpand ? "open" : "close"}`}
    use:clickOutside
    on:click_outside={closeNav}
>
    <button on:click={navAction} id="expandBtn">
        <img src={arrow} alt="burger" id="expandIcon" />
    </button>
    <slot />
</nav>

<style>
    * {
        font-family:
            system-ui,
            -apple-system,
            BlinkMacSystemFont,
            "Segoe UI",
            Roboto,
            Oxygen,
            Ubuntu,
            Cantarell,
            "Open Sans",
            "Helvetica Neue",
            sans-serif;
        margin: 0;
        padding: 0;
    }
    #expandBtn {
        background-color: transparent;
        border: 0;
        cursor: pointer;
        position: relative;
        left: -9px;
    }

    #expandIcon {
        scale: 1.2;
    }

    .open {
        width: 12em;
    }

    .close {
        width: 2em;
    }

    .navi-main {
        position: absolute;
        display: flex;
        flex-direction: column;
        justify-content: start;
        align-items: start;
        padding-left: 1.2rem;
        padding-right: 1.2rem;
        padding-top: 1.2rem;
        list-style: none;
        left: 0.7rem;
        transition: 0.2s all ease-out;
        height: calc(100% - 4.5%);
        border-radius: 0.5rem;
        background-color: #1a1a1a;
        gap: 2rem;
        color: white;
    }

    .navi-item {
        display: flex;
        align-items: center;
        gap: 2rem;
        font-size: 17px;
    }

    .hide {
        visibility: hidden;
    }
</style>
