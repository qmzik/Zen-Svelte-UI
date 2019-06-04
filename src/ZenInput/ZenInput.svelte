<script>
    export let value = '';
    export let type = 'text';
    export let placeholder = '';
    export let width = '100%';
    export let status = '';
    export let disabled = false;
    let focus = false;

    function handleFocus(e) {
        focus = true;
    }

    function handleBlur(e) {
        focus = false;
    }
</script>

<style>
.zenInput {
    border-radius: 5px;
    outline: none;
}

.zenInput:disabled {
    cursor: not-allowed;
}

.focus {
    border-color: #6190e8;
}

.info {
    border-color: #6190e8;
}

.success {
    border-color: #13ce66;
}

.error {
    border-color: #FF4949;
}

.warning {
    border-color: #FFC82C;
}
</style>



{#if type === 'password'}
    <input class="zenInput {status}"
        type="password"
        bind:value
        disabled={disabled}
        placeholder={placeholder}
        style="width: {width}"
        on:focus={handleFocus}
        on:blur={handleBlur}
        class:focus={focus}
    >
{:else}
    <input class="zenInput {status}"
        type="text"
        bind:value
        disabled={disabled}
        placeholder={placeholder}
        style="width: {width}"
        on:focus={handleFocus}
        on:blur={handleBlur}
        class:focus={focus}
    >
{/if}