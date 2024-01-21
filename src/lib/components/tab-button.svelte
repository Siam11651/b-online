<script lang="ts">
    export let selected: boolean = false;
    export let on_click: ()=> void;
</script>

{#if selected}
    <button type="button" class="btn btn-primary text-white mx-1">
        <slot></slot>
    </button>
{:else}
    <button type="button" class="btn btn-outline-primary text-white mx-1" on:click={on_click}>
        <slot></slot>
    </button>
{/if}