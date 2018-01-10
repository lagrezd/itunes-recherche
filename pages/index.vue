<template>
    <div>
        <h1>Recherche sur iTunes</h1>
        <br>

        <form action="" @submit.prevent="submit">
            <input
                type="text"
                placeholder="Entrer nom de l'artiste"
                v-model="search"
                autofocus>
        </form>
    </div>
</template>

<script>

export default {
  data(){
    return {
      search: ''
    }
  },
  methods: {
    submit(event) {
        this.$router.push(`results/${this.search}`);
    }
  },
  components: {
  }
}
</script>

<style>
* {
    text-align: center;
}
h1 {
    padding: 20px;
}

</style>
