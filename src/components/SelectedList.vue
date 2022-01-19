<template>
    <div>
        <h3>
            <a v-bind:href="item.link" target="_blank" rel="noopener noreferrer">
                {{ item.title }}
            </a>
        </h3>
        <p>
            {{ item.description }}
        </p>
    </div>
</template>

<script>
export default {
    name: "SelectedList",
    props: [ "item" ]
}
</script>

<style scoped>
h3 {
    font-size: 35px;
    font-family: Raleway-Bold;
    margin-bottom: 25px;
}

a {
    color: black;
    text-decoration: none;
}

a:hover {
    color: #007878;
}

div {
    margin-bottom: 50px;
}
</style>