<template>
    <p><a v-bind:href="contact.link" target="_blank" rel="noopener noreferrer">{{ contact.title }} </a></p>
</template>

<script>
export default {
    name: "Contacts",
    props: [ "contact" ]
}
</script>

<style scoped>
p {
    display: inline-block;
    margin-right: 20px;
    background: linear-gradient(180deg, #FFD2A8 50%, #00FFFF 50%);
    transition: ease-in background-color 0.4s;
}

p:hover {
    background: #00FFFF;
}

a {
    color: black;
    text-decoration: none;
}

a:hover {
    color: #00555A;
}
</style>