<template lang="">
    <div class="col-md-12">
        <div class="text-center">
            <h3>List of Courses : </h3>
        </div>
    </div>

    <div class="col-md-3" v-for="course in ListCourses" :key="course.id">
        <OneCourse :course="course" @delete="deleteCourse($event)" />
    </div>

</template>
<script>

    import OneCourse from './OneCourse.vue';
    export default {
        components: {
            OneCourse
        },
        props: [],
        data() {
            return {
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
            }
        },
    };
</script>
<style lang="">
</style>