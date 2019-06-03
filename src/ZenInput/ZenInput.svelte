<script>
    export let value = '';
    export let placeholder = '';
    export let width = '100%';
    export let focus = false;
    export let status = '';
    export let disabled = false;

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

<input class="zenInput {status}"
       bind:value
       disabled={disabled}
       placeholder={placeholder}
       style="width: {width}"
       on:focus={handleFocus}
       on:blur={handleBlur}
       class:focus={focus}
>