<script>
    export let checked = false;
    export let disabled = false;
</script>

<style>
.zenCheckbox {
    font-size: 14px;
    color: black;
    display: flex;
    align-items: center;
    cursor: pointer;
    user-select: none;
}


.zenCheckbox__input {
    display: none;
}

.zenCheckbox__sub {
    margin-right: 10px;
    min-width: 11px;
    height: 11px;
    background-color: white;
    border: #6190e8 1px solid;
    border-radius: 3px;
    transition: .3s all;
    position: relative;
}

.zenCheckbox__input:checked + .zenCheckbox__sub::before {
    visibility: visible;
}

.zenCheckbox__sub::before {
    content: '';
    position: absolute;
    left: 1.2px;
    width: 7px;
    height: 5px;
    border-radius: 1px;
    border-left: 2px solid white;
    border-bottom: 2px solid white;
    -webkit-transform: rotate(-45deg);
    transform: rotate(-45deg);
    visibility: hidden;
}

.zenCheckbox__input:checked ~ .zenCheckbox__sub {
    background-color: #6190e8;
}

.disabled {
    opacity: .5 !important;
    cursor: not-allowed;
}
</style>

<label class="zenCheckbox" class:disabled={disabled}>
    <input class="zenCheckbox__input" type="checkbox" bind:checked disabled={disabled}>
    <div class="zenCheckbox__sub"></div>
    <div class="zenCheckbox__caption">
        <slot></slot>
    </div>
</label>
