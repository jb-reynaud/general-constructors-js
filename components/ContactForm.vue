<template>
  <form name="contact" method="POST" data-netlify="true">
    <div class="row align-items-stretch mb-5">
      <div class="col-md-6">
        <div class="form-group">
          <!-- Name input-->
          <input
            class="form-control"
            type="text"
            placeholder="Your Name *"
            required
          />
        </div>
        <div class="form-group">
          <!-- Email address input-->
          <input
            class="form-control"
            type="email"
            placeholder="Your Email *"
            required
          />
        </div>
        <div class="form-group mb-md-0">
          <!-- Phone number input-->
          <input
            class="form-control"
            type="tel"
            placeholder="Your Phone *"
            required
          />
        </div>
      </div>
      <div class="col-md-6">
        <div class="form-group form-group-textarea mb-md-0">
          <!-- Message input-->
          <textarea
            id="message"
            class="form-control"
            placeholder="Your Message *"
            required
          ></textarea>
        </div>
      </div>
    </div>
    <div class="text-center">
      <b-button disabled variant="primary" type="submit">Send message</b-button>
    </div>
  </form>
</template>

<style scoped lang="scss">
#message {
  height: 146px;
}
</style>
