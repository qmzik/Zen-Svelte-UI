<script>
    export let type = 'primary';
    export let rounded = false;
    export let disabled = false;
    export let width = '100%';
    export let className = '';
</script>

<style>
.btn {
    cursor: pointer;
    padding: 10px 15px;
    width: 100%;
    text-align: center;
    border-radius: 30px;
    user-select: none;
    border-radius: 5px;
}

.primary {
    background-color: #D25F7E;
    color: white;
}

.secondary {
    color: #D25F7E;
    border: 1px solid #D25F7E;
}

.disabled {
    opacity: .5;
    cursor: not-allowed;
}

.rounded {
    border-radius: 30px;
}
</style>

<div on:click
     class="btn {type} {className}"
     class:disabled={disabled}
     class:rounded={rounded}
     style='width: {width}'>
    <slot></slot>
</div>
