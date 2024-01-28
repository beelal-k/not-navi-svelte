<script lang="ts">
    import { navExpand } from "./stores";
    export let iconPath: any;
    export let itemName: string;
    export let href: string;
    // console.log(navState);
</script>

<a {href}>
    <div class={`navi-item `} id="headIcon">
        <img alt="burger menu" src={iconPath} />
        <li class={`${$navExpand ? null : "hide"}`}>{itemName}</li>
    </div>
</a>

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
    a {
        cursor: pointer;
        text-decoration: none;
    }
    .hide {
        visibility: hidden;
    }

    .navi-item {
        display: flex;
        align-items: center;
        gap: 2rem;
        font-size: 17px;
        /* background-color: #1a1a1a; */
        color: white;
        /* border: 1px solid red; */
        width: auto;
        list-style: none;
    }

    .navi-item img {
        width: 1.8rem;
        /* border: 1px solid red; */
    }
    .navi-item li {
        width: 100px;
    }
</style>
