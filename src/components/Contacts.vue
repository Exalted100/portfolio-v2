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
}


a {
    color: black;
    text-decoration: none;
    background: linear-gradient(180deg, #FFD2A8 50%, #00FFFF 50%);
    transition: ease-in background-color 0.4s;
}

a:hover {
    background: #00FFFF;
}

a:active {
    background-color: none;
}

@media only screen and (max-width: 900px) {
    p {
        margin-bottom: 1em;
    }
}

</style>