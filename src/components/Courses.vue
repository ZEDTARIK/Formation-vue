<template lang="">


    <div class="row" v-if="showForm">
        <div class="col-md-6 mx-auto">
            <AddCours @add="addNewCourse($event)" />
        </div>
    </div>

    <div class="row my-3">
        <div class="col-md-6">
            <h4>List of Courses </h4>
        </div>
        <div class="col-md-6 text-right">
            <button @click="DisplayForm()" 
                    class="btn btn-sm" 
                    :class="{
                        'btn-outline-success': !showForm,
                        'btn-dark': showForm
                    }">
                {{ showForm ? 'Close' : 'Add New' }}
            </button>
        </div>
    </div>

    <div class="row">
        <div class="col-md-3" v-for="course in ListCourses" :key="course.id">
            <OneCourse :course="course" @delete="deleteCourse($event)" />
        </div>
    </div>


</template>
<script>

    import OneCourse from './OneCourse.vue';
    import AddCours from './AddCours'
    export default {
        components: {
            OneCourse,
            AddCours
        },
        props: [],
        data() {
            return {
                showForm: false,
                ListCourses: [
                    { id: 1, title: "Learn Spring Boot", photo: "https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/5miGPBu8RbCSc4hCzN39" },
                    { id: 2, title: "Learn Angular", photo: "https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/nrOHB2iQTIiGe7hHX9O0" },
                    { id: 3, title: "Learn JS", photo: "https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/H9QyEOsSLG05qNb2kC0V" },
                    { id: 4, title: "Learn Laravel", photo: "https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/aL2OXWSpTguVo0azLaPb" },
                    { id: 5, title: "Learn OOP PHP", photo: "https://process.fs.teachablecdn.com/ADNupMnWyR7kCWRvm76Laz/resize=width:705/https://www.filepicker.io/api/file/3qx2G451TvGZa32C7dEH" },
                ],
            };
        },
        methods: {
            deleteCourse(id) {
                this.ListCourses = this.ListCourses.filter(course => course.id != id);
            },
            addNewCourse(course) {
                this.ListCourses = [course, ...this.ListCourses];
                this.showForm = false;
            },
            DisplayForm() {
                this.showForm = !this.showForm;
            }
        },
    };
</script>
<style lang="">
</style>