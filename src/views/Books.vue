<template>
    <v-container fluid class="container1">
        <v-text-field label="Search Books" dark/>
        <v-slide-y-transition mode="out-in">
            <v-layout wrap class="books-container">

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>block</v-icon> Not available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>done</v-icon> Available</p>
                    </v-container>
                </v-card>

                <v-card class="book">
                    <v-container>
                        <h3>Book Title</h3>
                        <small><em>by Author Name</em></small>
                        <p>Description : Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                            Nobis pariatur quasi repellat veniam vero!</p>
                        <p><v-icon>block</v-icon> Not available</p>
                    </v-container>
                </v-card>

            </v-layout>
        </v-slide-y-transition>
    </v-container>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .container1 {
        margin: auto;
    }

    .books-container {
        margin: 0 auto;
    }

    .book {
        margin: 10px;
        width: 280px;
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
