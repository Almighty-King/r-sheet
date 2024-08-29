<script setup lang="ts">
    import { defineModel } from 'vue';
    const visible = defineModel('visible');
    function closeModal() {
        visible.value = false;
    }
</script>
<template>
    <Teleport to="body">
        <Transition name="modal">
            <div v-if="visible">
                <div class="fixed top-0 w-full h-screen bg-opacity-40 bg-black" @click.self="closeModal">
                    asdasd
                </div>
            </div>
        </Transition>
    </Teleport>
</template>

<style scoped>
    .modal-from-active, .modal-leave-active {
        transition: all 0.8s ease-in-out;
    }

    .modal-enter-from,
    .modal-leave-to {
        opacity: 0;
    }
</style>
