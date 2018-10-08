<template>
    <v-container fluid>
        <v-text-field label="Search Students" dark/>
        <v-slide-y-transition mode="out-in">
            <v-layout wrap>

                <v-card class="student" v-for="student in students">
                    <v-container class="student-container">
                        <h1>
                            {{ student.fullname }}
                            <span class="actions">
                                <span class="edit"><v-icon>create</v-icon></span>
                                <span class="delete"><v-icon>delete</v-icon></span>
                            </span>
                        </h1>
                        <em class="recent-books">
                            <h4>Recent Books:</h4>
                            <ul>
                                <li>Software Engineering</li>
                                <li>IT Strategy</li>
                                <li>Cinderella</li>
                                <li>Science of Gravity</li>
                            </ul>
                        </em>
                        <h4>Passcode: <span class="passcode">{{ student.passcode }}</span></h4>
                    </v-container>
                </v-card>

            </v-layout>
        </v-slide-y-transition>
    </v-container>
</template>

<script>
    import axios from 'axios'

    export default {
        name: 'Students',

        data() {
            return {
                students: {}
            }
        },

        methods: {
            getStudents() {
                axios.get('http://127.0.0.1:5000/api/v1/students')
                    .then((response) => {
                        this.students = response.data.students
                    })
            }
        },

        created() {
            this.getStudents()
        }

    }
</script>

<style scoped>
    .student {
        margin: 20px;
        width: 400px;
    }

    .recent-books {
        margin: 0 10px;
    }

    .passcode {
        color: red;
    }

    .actions {
        padding-left: 50px;
    }

    .edit, .delete {
        font-size: 0.52em;
        margin: 0 20px;
    }
</style>
