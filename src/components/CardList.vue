<template>
    <div class="course-list">
        <div class="course-card" v-for="(item, index) in course" :key="item.id">
            <div :class="{ 'course-title': item.isActive, 'course-is-not-active': !item.isActive }">{{ item.isActive ? item.title
                : 'Кажется, курс уже не существует…' }}</div>
            <div class="course-description" v-if="item.isActive">{{ item.description }}</div>
            <div class="course-duration" v-if="item.isActive">{{ item.duration }}</div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const course = ref([
    {
        id: 1,
        title: 'Python-разработчик',
        description: 'Описание: На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropbox и Yotube написаны на Python.',
        duration: '10 месяцев',
        isActive: true
    },
    {
        id: 2,
        title: 'Веб-разработчик',
        description: 'Описание: Веб-разработчик создает сайты, сервисы и приложения, которыми мы ежедневно пользуемся.',
        duration: '7 месяцев',
        isActive: true
    },
    {
        id: 3,
        title: 'Графический дизайнер',
        description: 'Описание: Научим делать бренды узнаваемыми через создание логотипов, графики для рекламы, упаковки и не только.',
        duration: '6 месяцев',
        isActive: true
    },
    {
        id: 4,
        title: 'Инженер по тестированию',
        description: 'Описание: Вы научитесь находить ошибки в работе сайтов и пложения с помщью Java, JavaScript или Python.',
        duration: '7 месяцев',
        isActive: true
    },
    {
        id: 5,
        title: 'Веб-разработчик',
        description: 'Описание: Веб-разработчик создает сайты, сервисы и приложения, которыми мы ежедневно пользуемся.',
        duration: '7 месяцев',
        isActive: false
    },
    {
        id: 6,
        title: 'Графический дизайнер',
        description: 'Описание: Научим делать бренды узнаваемыми через создание логотипов, графики для рекламы, упаковки и не только.',
        duration: '6 месяцев',
        isActive: false
    },
    {
        id: 7,
        title: 'Инженер по тестированию',
        description: 'Описание: Вы научитесь находить ошибки в работе сайтов и пложения с помщью Java, JavaScript или Python.',
        duration: '7 месяцев',
        isActive: false
    },
])
</script>

<style scoped>

.course-list {
    display: flex;
    flex-wrap: wrap;
    
}
.course-card {
    width: 420px;
    padding: 24px 24px 16px;
    background-color: #f0ebeb;
    border-radius: 16px;
    margin-bottom: 16px;
    margin-right: 16px;
}

.course-title {
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 8px;
}

.course-description {
    color: rgb(106, 109, 114);
    margin-bottom: 16px;
}

.course-is-not-active {
    color: rgb(213, 146, 157);
}

.form {
    margin-bottom: 12px;
}
</style>