<template>
    <div>
        <div v-for="(items, category) in content" :key="category" class="category">
            <h2>{{ category }}</h2>
            <ul>
                <li v-for="item in items" :key="item">{{ item }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        content: {
            type: Object,
            required: true
        }
    }
};
</script>

<style scoped>
.category {
    margin-bottom: 20px;
}

.category h2 {
    margin-bottom: 10px;
    color: #007bff;
}

ul {
    list-style: disc;
    margin-left: 20px;
}
</style>