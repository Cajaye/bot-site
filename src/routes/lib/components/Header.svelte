<script lang="ts">
    let state = false;
    const toggleState = () => state = !state;
</script>

<header>
    <h1>ANIMISTA</h1>
</header>

<style lang="scss">
header {
    text-align: center;
    h1 {
    @include font-props(h1);
}
}
</style>