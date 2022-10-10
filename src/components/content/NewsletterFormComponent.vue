<template>
    <div class="newsletter-form-container">
        <div class="container d-flex flex-column align-items-center">

            <h3 class="pb-4">Subscribe to our Newsletter</h3>

            <form class="w-75 text-center">

                <input type="email" name="userEmail" id="userEmail" placeholder="Insert your email*"
                    class="w-50 p-2 h-100 me-5">

                <!-- Uso di bottone invece input:submit per mancanza di action in form -->
                <button class="btn btn-dark text-uppercase rounded-0 fw-bold w-25 h-100">Send</button>
                <!-- <input type="submit" class="btn btn-dark text-uppercase rounded-0" value="Send"> -->

            </form>

        </div>
    </div>
</template>

<script>
export default {
    name: 'NewsletterFormComponent'
}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

.newsletter-form-container {
    background-color: $tr-custom-grey;

    .container {
        padding: $tr-py-100;

        form {
            height: 50px;

            #userEmail {
                border: 1px solid $tr-silver-chalice;
            }

        }

    }

}
</style>