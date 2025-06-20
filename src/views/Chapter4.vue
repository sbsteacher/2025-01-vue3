<script setup>
    const fruits = [ 'apple', 'banana', 'pear' ];
    const sports = [
        { id: 1, name: '농구' },
        { id: 2, name: '축구' },
        { id: 3, name: '배구' }
    ];

    const pop = message => alert(message);
    const pop2 = () => alert('파라미터 없음');
</script>

<template>
    <h1>Chapter4.vue</h1>
    <div v-for="(item, idx) in fruits" :key="idx">
        {{ idx + 1 }}. {{  item }}        
    </div>

    <select>
        <option v-for="item in sports" :key="item.id" :value="item.id">
            {{ item.name }}
        </option>
    </select>

    <select>
        <option value="1">농구</option>
        <option value="2">축구</option>
        <option value="3">배구</option>
    </select>

    <button @click="pop('반가워')">Hello pop</button>
    <button v-on:click="pop2">Hello pop2</button>

</template>

<style scoped>

</style>