<template>
  <nav class="navbar navbar-dark bg-green-gradient py-4 shadow">
    <div class="container">
      <div class="row w-100 align-items-center">
        <div class="col">
          <span class="navbar-brand mb-0 h1">Light Vue 3 validation</span>
        </div>
        <div class="col-auto">
          <a
            href="https://github.com/AlisherARI/light-vue3-validation"
            target="_blank"
            rel="noreferrer noopener nofollow"
            class="text-decoration-none navbar-brand"
            style="display: flex; align-items: center"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 496 512"
              style="height: 24px; margin-right: 10px"
            >
              <path
                fill="#fff"
                d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"
              />
            </svg>
            Github
          </a>
        </div>
      </div>
    </div>
  </nav>
  <div class="container">
    <div class="my-5">
      <h4 class="mb-3">This is what our setup returns</h4>
      <div class="bg-light">
        <code>
          <pre>
            {{ setupExample }}
          </pre>
        </code>
      </div>
    </div>
    <form class="my-5">
      <div class="row w-100 mb-4">
        <div class="col-12 col-md mb-3">
          <h4>Form example</h4>
        </div>
        <div class="col-12 col-md mb-3">
          <h4>Validation example</h4>
        </div>
      </div>
      <div class="row w-100">
        <div class="col-12 col-md mb-3">
          <label for="phoneFormControle" class="form-label">Phone</label>
          <input
            v-model="phone.model"
            type="tel"
            class="form-control mb-4"
            id="phoneFormControle"
            placeholder="...."
          />
          <div class="py-2 px-3 bg-light">
            <code>{{ phoneExample }}</code>
          </div>
        </div>
        <div class="col-12 col-md mb-3">
          <pre>{{ phone }}</pre>
        </div>
      </div>
      <hr class="mb-4" />
      <div class="row w-100">
        <div class="col-12 col-md mb-3">
          <label for="emailFormControl" class="form-label">
            Email address
          </label>
          <input
            v-model="loginData.email.model"
            type="email"
            class="form-control mb-4"
            id="emailFormControl"
            placeholder="...."
          />
          <div class="py-2 px-3 bg-light">
            <code>{{ loginDataExample.email }}</code>
          </div>
        </div>
        <div class="col-12 col-md mb-3">
          <pre>{{ loginData.email }}</pre>
        </div>
      </div>
      <div class="row w-100">
        <div class="col-12 col-md mb-3">
          <label for="passwordFormControl" class="form-label">Pasword</label>
          <input
            v-model="loginData.password.model"
            type="text"
            class="form-control mb-4"
            id="passwordFormControl"
            placeholder="...."
          />
          <div class="py-2 px-3 bg-light">
            <code>{{ loginDataExample.password }}</code>
          </div>
        </div>
        <div class="col-12 col-md mb-3">
          <pre>{{ loginData.password }}</pre>
        </div>
      </div>
      <hr class="mb-4" />

      <div class="row w-100">
        <div class="col-12 col-md mb-3">
          <label for="dateFormControl" class="form-label">Date</label>
          <input
            v-model="date.model"
            type="date"
            class="form-control mb-4"
            id="dateFormControl"
            placeholder="...."
          />
          <div class="py-2 px-3 bg-light">
            <code>{{ dateExample }}</code>
          </div>
        </div>
        <div class="col-12 col-md mb-3">
          <pre>{{ date }}</pre>
        </div>
      </div>
    </form>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from "vue";
import { validateRef } from "light-vue3-validation";

export default defineComponent({
  name: "App",
  setup() {
    const phone = validateRef("", [
      "required",
      { type: "minLength", value: 12 },
    ]);
    const loginData = reactive({
      email: validateRef("", [
        "required",
        "email",
        { type: "minLength", value: 10 },
      ]),
      password: validateRef("", [
        "required",
        { type: "maxLength", value: 16 },
        { type: "minLength", value: 6 },
      ]),
    });
    const date = validateRef("", ["required", "date"]);
    const phoneExample = `<input .. type="tel". v-model="phone.model" ... />`;
    const loginDataExample = {
      email: `<input ... type="email" v-model="loginData.email.model" ... />`,
      password: `<input ... type="password" v-model="loginData.password.model" ... />`,
    };
    const dateExample = `<input ... type="date" v-model="date.model" ... />`;
    const setupExample = `
    setup () {

      const phone = validateRef("", ["required", { type: "minLength", value: 12 }]);

      const loginData = reactive({
        email: validateRef("", ["required", "email", { type: "minLength", value: 10 }]),
        password: validateRef("", ["required", { type: "maxLength", value: 16 }, { type: "minLength", value: 6 }]),
      });

      const date = validateRef("", ["required", "date"]);
    }`;

    return {
      setupExample,
      phoneExample,
      loginDataExample,
      dateExample,
      phone,
      loginData,
      date,
    };
  },
});
</script>
