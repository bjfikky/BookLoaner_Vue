<template>
    <v-container fluid>
        <v-text-field label="Search Books" dark/>
        <v-slide-y-transition mode="out-in">
            <v-layout wrap>

                <v-card class="book" v-for="(book, index) in books" v-bind:key="index">
                    <v-container class="book-container">
                        <h3>{{ book.title }}</h3>
                        <small>AUTHOR: <em>{{ book.author }}</em></small>
                        <br>
                        <small>EDITION: <em>{{ book.edition }}</em></small>
                        <br>
                        <small>GENRE: <em>{{ book.genre }}</em></small>
                        <p>Description: Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p class="status"><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

            </v-layout>
        </v-slide-y-transition>
    </v-container>
</template>


<script>
    import axios from 'axios'

    export default {
        name: 'Books',

        data() {
            return {
                books: {}
            }
        },

        methods: {
            getBooks() {
                axios.get('http://127.0.0.1:5000/api/v1/books')
                    .then((response) => {
                        this.books = response.data.books
                    })
            }
        },

        created() {
            this.getBooks()
        }

    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


    .status {
        margin-top: auto;
    }

    .book {
        margin: 10px;
        width: 300px;
    }

    h1, h2 {
      font-weight: normal;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      display: inline-block;
      margin: 0 10px;
    }
    a {
      color: #42b983;
    }
</style>
