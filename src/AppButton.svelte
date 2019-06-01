<script>
    export let type = 'primary';
    export let disabled = false;
</script>

<style>
.btn {
    cursor: pointer;
    padding: 10px 15px;
    width: 100%;
    text-align: center;
    border-radius: 30px;
    user-select: none;
}

.primary {
    background-color: #D25F7E;
    color: white;
}

.secondary {
    color: #D25F7E;
    border: 1px solid #D25F7E;
    background-color: transparent;
}

.disabled {
    opacity: .5;
    cursor: not-allowed;
}
</style>

<div class="btn {type}" class:disabled={disabled}>
    <slot></slot>
</div>
