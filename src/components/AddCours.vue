<template lang="">
    <div>
        <div class="card">
            <div class="card-body">

                <div class="form-group row">
                    <label for="Title" class="col-sm-2 control-label">Title</label>
                    <div class="col-sm-10">
                        <input ref="Title" type="text" name="Title" class="form-control" placeholder="Title">
                    </div>
                </div>

                <div class="form-group row">
                    <label for="Photo" class="col-sm-2 control-label">Url Photo</label>
                    <div class="col-sm-10">
                        <input ref="Photo" type="text" name="Photo" class="form-control" placeholder="Photo">
                    </div>
                </div>

                <div class="form-group">
                    <div class="col-sm-6 mx-auto">
                        <button @click="addCourse()" class="btn btn-block btn-success">Save</button>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {

            }
        },
        methods: {
            addCourse() {
                let title = this.$refs.Title.value;
                let photo = this.$refs.Photo.value;

                const course = {
                    title,
                    photo
                }

                this.$emit('add', course);

                this.$refs.Title.value = "";
                this.$refs.Photo.value = "";
            }
        },
    }
</script>
<style lang="">

</style>