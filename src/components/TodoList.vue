<script setup lang="ts">
    import ListItem from './ListItem.vue';
    type Item = {
        title: string;
        checked?: boolean;
    }
    const GroupsItems: Item[] = [
        { title: 'Leer un libro al mes', checked: false },
        { title: 'Hacer ejercicio', checked: true },
        { title: 'Aprender algo nuevo' },
    ];
</script>

<template>
    <ul>
        <li :key="index" v-for="(element, index) in GroupsItems">
            <ListItem :isChecked="element.checked">
                {{ element.title }}
            </ListItem>

        </li>
    </ul>
</template>

<style scoped>
    ul {
        list-style: none;
        padding: 0;
    }
    li {
        margin: 0.5rem 0;
    }
</style>