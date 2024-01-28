<script lang="ts">
    import burger from "$lib/burger.svg";
    import settings from "$lib/setting.svg";
    import stat from "$lib/stat.svg";

    let navExpand: Boolean = false;

    const navAction = () => {
        navExpand = !navExpand;
    };
</script>


<h1>About</h1>

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
        /* font-weight: 600; */
        margin: 0;
        padding: 0;
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
        /* border: 1px solid red; */
        background-color: #1a1a1a;
        gap: 2rem;
        color: white;
    }

    .navi-item {
        display: flex;
        align-items: center;
        /* justify-content: center; */
        gap: 2rem;
        /* padding-bottom: 1rem; */
        /* border-bottom: 1px solid #2a2a2a; */
        font-size: 17px;
        /* line-height: 30px; */
    }

    .navi-item img {
        width: 1.8rem;
    }

    .hide {
        visibility: hidden;
    }
</style>
