<script lang="ts">
    import settings from "$lib/setting.svg";
    import stat from "$lib/stat.svg";
    import Navi from "./Navi.svelte";
    import Item from "./Item.svelte";
</script>

<Navi>
    <Item itemName="Custom" iconPath={settings} href="/about" />
    <Item itemName="Missile log" iconPath={stat} href="/stat" />
</Navi>
<div>
    <slot />
</div>

<style>
    div{
        margin-left: 100px;
    }
</style>
