<template>
    <div>
        <v-navigation-drawer
                v-model="drawer"
                clipped
                fixed
                app
        >
            <v-list dense>
                <v-list-tile v-on:click="navigateToBooks">
                    <v-list-tile-action>
                        <v-icon>book</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title>Books</v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>

                <v-list-tile v-on:click="navigateToStudents">
                    <v-list-tile-action>
                        <v-icon>supervised_user_circle</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <v-list-tile-title>Students</v-list-tile-title>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>

        <v-toolbar app fixed clipped-left>
            <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title>Book Loaner</v-toolbar-title>
        </v-toolbar>
    </div>

</template>

<script>
    export default {
        name: "AppBar",

        data: () => ({
            drawer: false
        }),

        methods: {
            navigateToBooks() {
                this.drawer = false
                this.$router.push({ name: 'books'})
            },

            navigateToStudents() {
                this.drawer = false
                this.$router.push({ name: 'students'})
            }
        }
    }
</script>

<style scoped>

</style>