<template>
    <button
        class="menu-item"
        :class="{ 'is-active': isActive ? isActive(): null }"
        @click="action"
        :title="title">
        <i :class="`ri-${icon}`"></i>
    </button>
</template>

<script>
export default {
    props: {
        icon: {
            type: String,
            required: true,
        },
        title: {
            type: String,
            required: true,
        },
        action: {
            type: Function,
            required: true,
        },
        isActive: {
            type: Function,
            default: null,
        },
    },
    data() {
        return {}
    },
}
</script>

<style lang="scss">
.menu-item {
    background: transparent;
    border: none;
    border-radius: 0.4rem;
    color: #000;
    cursor: pointer;
    height: 1.75rem;
    padding: 0.25rem;
    margin-right: 0.25rem;
    width: 1.75rem;

    svg {
        fill: currentColor;
        height: 100%;
        width: 100%;
    }

    &.is-active,
    &:hover {
        background-color: #303030;
        color:#fff;
    }
}
</style>
