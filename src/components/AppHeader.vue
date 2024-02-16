<script>
export default {
    name: 'Header',
    data() {
        return {
            lists: [
                {
                    title: 'home',
                    links: '#',
                },
                {
                    title: 'progetti',
                    links: '#',
                },
                {
                    title: 'chi-sono',
                    links: '#',
                }
            ]
        }
    },
    components: {

    },
    methods: {

    },
    created() {

    }
}
</script>

<template>
    <header class="bg-black text-white">
        <div class=" container d-flex justify-content-between p-3">
            <div>logo</div>
            <div>
                <ul class="list-unstyled d-flex gap-5">
                    <li v-for="list in this.lists"> <a class="text-decoration-none text-white" :href="list.links">{{
                        list.title.toUpperCase() }} </a>
                    </li>
                </ul>
            </div>

        </div>
    </header>
</template>

<style scoped></style>