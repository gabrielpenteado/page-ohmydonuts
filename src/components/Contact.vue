<script setup lang="ts">
import { ref } from "vue";

const WEB3FORMS_ACCESS_KEY = import.meta.env.VITE_WEB3FORMS_KEY;

const name = ref("");
const email = ref("");
const message = ref("");
const buttonText = ref("Send message");
const isSending = ref(false);
const subject = ref("New Message from Oh My Donuts website");
const from_name = ref("Oh My Donuts");

const resetForm = () => {
  name.value = "";
  email.value = "";
  message.value = "";
  isSending.value = false;
  buttonText.value = "Send message";
};

const submitForm = async () => {
  isSending.value = true;
  buttonText.value = "Message Sent";
  try {
    const response = await fetch("https://api.web3forms.com/submit", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        Accept: "application/json",
      },
      body: JSON.stringify({
        access_key: WEB3FORMS_ACCESS_KEY,
        name: name.value,
        email: email.value,
        message: message.value,
        subject: subject.value,
        from_name: from_name.value,
      }),
    });

    const data = await response.json();
    if (data.success) {
      // console.log(data);
    }

    setTimeout(() => {
      resetForm();
    }, 2000);
  } catch (error) {
    console.log("Error sending form data:", error);
  }
};
</script>

<template>
  <div id="contact" class="py-20 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="section-title">Take the First Step Forward</h2>
        <p class="section-description">
          Ready to take your donut business to the next level?<br />
          Drop us a message and we'll show you how Oh My Donuts can help you
          grow.
        </p>
      </div>
      <div class="mx-auto mt-16 max-w-xl">
        <form @submit.prevent="submitForm" class="space-y-6">
          <div>
            <label
              for="name"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Name</label
            >
            <div class="mt-2">
              <input
                type="text"
                id="name"
                name="name"
                v-model="name"
                class="form-input"
                placeholder="Your name"
                required
              />
            </div>
          </div>
          <div>
            <label
              for="email"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Email</label
            >
            <div class="mt-2">
              <input
                type="email"
                id="email"
                name="email"
                v-model="email"
                class="form-input"
                placeholder="your@email.com"
                required
              />
            </div>
          </div>
          <div>
            <label
              for="message"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Message</label
            >
            <div class="mt-2">
              <textarea
                id="message"
                v-model="message"
                name="message"
                rows="4"
                class="form-input"
                placeholder="Your message"
                required
              ></textarea>
            </div>
          </div>
          <div>
            <div>
              <input type="hidden" name="subject" />
            </div>
            <div>
              <input type="hidden" name="from_name" />
            </div>
          </div>
          <button
            type="submit"
            :disabled="isSending"
            :class="{
              'btn-primary w-full': !isSending,
              'btn-primary bg-transparent border-2 border-primary-600 text-primary-600 w-full':
                isSending,
            }"
          >
            {{ buttonText }}
          </button>
        </form>
      </div>
    </div>
  </div>
</template>
