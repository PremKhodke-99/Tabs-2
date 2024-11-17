<template>
    <div class="tab-nav">
        <ul>
            <li v-for="tab in tabs" :key="tab" :class="{ active: tab === selected }" @click="selectTab(tab)">
                {{ tab }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        tabs: Array,
        selected: String
    },
    methods: {
        selectTab(tab) {
            this.$emit('selected', tab);
        }
    }
};
</script>

<style scoped>
.tab-nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    padding: 0;
}

.tab-nav li {
    cursor: pointer;
    padding: 10px 20px;
    border-bottom: 2px solid transparent;
}

.tab-nav li.active {
    border-bottom: 2px solid #007bff;
    color: #007bff;
}
</style>