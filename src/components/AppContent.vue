<script>
export default {
    name: 'Content',
    props: ['projects'],

    data() {
        return {
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
    <div class="container">
        <div class="row my-4">
            <div class="col col-md-4 g-4" v-for="project in projects">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title" v-if=project.title>Titolo: {{ project.title }}</h5>
                        <p class="card-text" v-if=project.description>Descrizione: {{ project.description }}</p>
                        <p class="card-text" v-if=project.status>Stato: {{ project.status }}</p>
                        <p class="card-text" v-if=project.start_date>Data d'inizio: {{ project.start_date }}</p>
                        <p class="card-text" v-if=project.type_id>Tipo: {{ project.type_id }}</p>
                        <a href="#" class="btn btn-primary">Visualizza progetto</a>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<style scoped></style>
