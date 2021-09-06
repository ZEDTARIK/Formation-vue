<template lang="">

    <div class="card my-1">
        <img :src="course.photo" class="card-img-top" :alt="course.title" />
        <div class="card-body">
            <p class="card-text">{{ course.title }}</p>
            <span>
                <button class="btn btn-sm btn-danger" @click="onDeleted(course.id)">Delete</button>
            </span>
        </div>
    </div>

</template>
<script>
    export default {
        props: ['course'],
        data() {
            return {
                
            }
        },
        methods: {
            onDeleted(id) {
                    this.$emit("delete", id)
            }
        },
    };
</script>
<style lang="">
</style>