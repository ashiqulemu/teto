<template>
    <div v-if="$root.stepThree">
        <div class="step-form">
            <p class="academic"> Your Academic Qualifications</p><br>
            <p class="degree pb-3">What was your top qualification ( Masters in Physics/Engineering)</p>

            <qualifications :qualifications="qualifications"></qualifications>

            <p class="academic pb-3">
                What was your core subjects during your study that you want to highlight in your
                profile ?
            </p>

            <subject :subjects="subjects"></subject>

            <hr class="horizontalRule pt-3">
            <div class="row">
                <div class="col-md-12">
                    <p class="academic pb-3">Certificate</p>
                    <p class="degree">Please upload your certificate to become verified tutor. You can skip and upload
                        later.
                    </p>
                    <label for="fileUpload" class="uploadFile">Upload Documents</label>
                    <input class="back-button " type="file" name="" id="fileUpload" style="display: none;">
                    <p class="degree pt-3">Only .pdf, .jpg and .png files. 4mb max file size</p>
                </div>
                <div class="col-md-12">
                    <div class="control-button">
                        <button class="back-button" @click.prevent="$root.backSecondPage">Back</button>
                        <button class="continue-button" @click="$root.callFourStep">Continue</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import qualifications from './qualifications.vue'
    import subject from './subject.vue'

    export default {
        name: "step3",
        props: ['qualifications', 'subjects'],
        components: {qualifications, subject}
    }
</script>

<style scoped>

</style>
