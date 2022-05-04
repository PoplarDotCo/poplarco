<template>
  <section id="contact-us">
    <div class="container">
      <div class="row direction_column">
        <h2>Contact Us</h2>
        <p class="isH4">Be the first one to know when we make the news or have new releases</p>
      </div>

      <form>
        <fieldset>
          <div class="row direction_row">

            <div class="input-container__text name">
              <label for="name">Name <sup>*</sup></label>
              <input type="text" id="name" v-bind="name" required>
            </div>

            <div class="input-container__text email">
              <label for="email">Email <sup>*</sup></label>
              <input type="text" id="email" v-bind="email" required>
            </div>

          </div>

          <div class="row direction_row">

            <div class="input-container__text town">
              <label for="town">Town <sup>*</sup></label>
              <input type="text" id="town" v-bind="town" required>
            </div>

            <div class="input-container__text country">
              <label for="country">Country <sup>*</sup></label>
              <input type="text" id="country" v-bind="country" required>
            </div>

          </div>

          <div class="row direction_row">

            <div class="input-container__textarea message">
              <label for="message">Message (Optional)</label>
              <textarea cols="30" rows="4" id="message" v-bind="message"></textarea>
            </div>

          </div>
        </fieldset>
      </form>

      <button>Request More Info</button>



    </div>
  </section>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {
      name: '',
      email: '',
      town: '',
      country: '',
      message: '',
    }
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
