<template>
  <section id="contact-us">
    <div class="container">
      <div class="row direction_column">
        <h2>Contact Us</h2>
        <p class="isH4">Be the first one to know when we make the news or have new releases</p>
      </div>

      <form
        v-show="!isSubmitted"
        @submit.prevent="validate"
      >
        <fieldset>
          <div class="row direction_row">

            <div class="input-container__text name">
              <label for="name">Name <sup>*</sup></label>
              <input type="text" id="name" v-bind="name" required @blur="touch('name')">
              <div class="error" v-if="nameTouched && !name">Field is required</div>
            </div>

            <div class="input-container__text email">
              <label for="email">Email <sup>*</sup></label>
              <input type="text" id="email" v-bind="email" required @blur="touch('email')">
              <div class="error" v-if="emailTouched && !email">Field is required</div>
              <div class="error" v-if="emailTouched && !emailValidated">This is not a valid email</div>
            </div>

          </div>

          <div class="row direction_row">

            <div class="input-container__text town">
              <label for="town">Town <sup>*</sup></label>
              <input type="text" id="town" v-bind="town" required @blur="touch('town')">
              <div class="error" v-if="townTouched && !town">Field is required</div>
            </div>

            <div class="input-container__text country">
              <label for="country">Country <sup>*</sup></label>
              <input type="text" id="country" v-bind="country" required @blur="touch('country')">
              <div class="error" v-if="countryTouched && !country">Field is required</div>
            </div>

          </div>

          <div class="row direction_row">

            <div class="input-container__textarea message">
              <label for="message">Message (Optional)</label>
              <textarea cols="30" rows="4" id="message" v-bind="message"></textarea>
            </div>

          </div>
        </fieldset>
        <fieldset>
          <button
              type="submit"
              :disabled="submitting"
          >Request More Info</button>
        </fieldset>
      </form>


    </div>
  </section>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {
      name: '',
      nameTouched: false,
      email: '',
      emailTouched: false,
      town: '',
      townTouched: false,
      country: '',
      countryTouched: false,
      message: '',
      isSubmitted: false,
      submitting: false,
      error: false,
    }
  },
  methods: {
    touch(field) {
      if (field === 'name') {
        this.nameTouched = true;
      }

      if (field === 'email') {
        this.emailTouched = true;
      }

      if (field === 'town') {
        this.townTouched = true;
      }

      if (field === 'country') {
        this.countryTouched = true;
      }

    },
    validate() {

    },
    emailValidated() {

    },
  }
}
</script>

<style lang="scss">
#contact-us {

  .isH4 {
    max-width: 500px;
  }

  form {

    .row {
      max-width: 700px;
      justify-content: space-between;
      margin-top: 30px;


      .input-container__text {
        width: 45%;
      }

      .input-container__textarea {
        width: 100%;
      }

    }

  }

  button {
    margin-top: 30px;
  }

  @include breakpoint(xxs-down) {

    .direction_row {
      flex-direction: column;
    }

    form {
      .row {
        margin: 0;

        .input-container__textarea,
        .input-container__text {
          width: 100%;
          margin-top: 30px;
        }

      }
    }

  }

}
</style>
