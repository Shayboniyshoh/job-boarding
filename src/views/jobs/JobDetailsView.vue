<template>
    <div class="job-card" v-if="job">
        <p>The current jobs id is <strong>{{ id }}</strong></p>
        <h1>{{ job.title }}</h1>
        <p>{{ job.details }}</p>
    </div>
    <div v-else>
        <p>Loading the job details...</p>
    </div>
</template>

<script>
export default {
    props: ['id'],
    data() {
        return {
            job: null
        }
    },
    mounted() {
        fetch(`http://localhost:3000/jobs/${this.id}`)
            .then(res => res.json())
            .then(data => this.job = data)
            .catch(err => console.log(err.message)
            )
    }
}
</script>

<style scoped>
.job-card {
    max-width: 400px;
    width: 100%;
    background: #eee;
    padding: 20px 30px;
    border-radius: 8px;
    margin: 100px auto;
}
</style>