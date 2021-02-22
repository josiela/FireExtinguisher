<template>
    <div class="container">
        <h4 class="header">
            {{ cardSection.title }}
        </h4>
        <p class="snippet">
            {{ cardSection.snippet }}
        </p>
        <div class="cards-container">
            <!-- in here we're going to display the largCard-Components. Dafür iterieren wir nun durch das cards-Array in der data.js -->
            <LargeCard v-for="card in cardSection.cards" :key="card.id" :card="card"/>
            <!-- :card is a prop that we're übergeben. This prop we define in the props-section in LargeCard.vue-->
        </div>
    </div>
</template>

<script>
export default {
    props: ['cardSection']
}
</script>

<style scoped>
.container {
    margin-top: 2rem;
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>>

</style>