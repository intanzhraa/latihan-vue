<template>
    <div>
        <Header text="Ini Adalah Header">
            <template #footer>
                <p>Ini Adalah Slot Dari Footer</p>
            </template>
        </Header>
        <my-component nama="Intan" umur="20"></my-component>
        <latihan-component nama="Indira" umur="19"></latihan-component>
        <latihan-dua-component></latihan-dua-component>
        <watchers-component nama="Selpi" umur="22"></watchers-component>
        <latihan-event-component :nama="nama" :umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            <template #header>
                <div>
                    <p>Ini Adalah Header latihan Event</p>
                </div>
            </template>
        </latihan-event-component>
    </div>
</template>

<script setup>
import LatihanEventComponent from './LatihanEventComponent.vue';
import latihanComponent from './LatihanComponent.vue';
import MyComponent from './MyComponent.vue';
import Header from './Headers.vue';
import LatihanDuaComponent from './LatihanDuaComponent.vue';
import WatchersComponent from './WatchersComponent.vue';

// event
import { ref } from 'vue';
const nama = ref('Otan');
const umur = ref(17);

const onGreeted = () => {
    console.log('Kamu udah disapa, bro!');
};

</script>