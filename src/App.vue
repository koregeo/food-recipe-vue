<template>
  <div class="grid md:grid-cols-3">
    <!-- grid -->
    <div class="md:col-span-1 md:flex md:justify-end">
      <!-- grid -->
      <nav>
        <div class="flex justify-between items-center">
          <h1 class="font-bold uppercase p-4 border-b border-gray-100">
            <a href="/" class="hover:text-gray-700">Food Recipe</a>
          </h1>
          <!--Burger Menu -->
          <div
            @click="toggleClass()"
            class="px-4 cursor-pointer md:hidden"
            id="burger"
          >
            <svg
              class="w-6"
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </div>
        </div>
        <ul
          v-bind:class="[isActive ? 'hidden' : '']"
          class="md:block"
          id="menu"
        >
          <li class="text-gray-700 font-bold py-1">
            <a
              href="#"
              class="px-4 flex justify-end border-r-4 border-white hover:border-primery transition ease-out duration-500"
            >
              <span>Home</span>
              <svg
                class="w-5 inline-block ml-2"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
                />
              </svg>
              <!-- icon -->
            </a>
          </li>
          <li class="py-1">
            <a
              href="#"
              class="px-4 flex justify-end border-r-4 border-white hover:border-primery transition ease-out duration-500"
            >
              <span>About</span>
              <svg
                class="w-5 inline-block ml-2"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </a>
          </li>
          <li class="py-1">
            <a
              href="#"
              class="px-4 flex justify-end border-r-4 border-white hover:border-primery transition ease-out duration-500"
            >
              <span>Contact</span>
              <svg
                class="w-5 inline-block ml-2"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                />
              </svg>
            </a>
          </li>
        </ul>
      </nav>
    </div>
    <!-- end nav-->

    <main class="px-16 py-6 bg-gray-100 md:col-span-2">
      <!-- grid -->
      <div class="flex justify-center md:justify-end ">
        <a
          href="#"
          class="btn text-primery border-primery md:border-2 hover:bg-primery hover:text-white transition ease-out duration-500"
          >Log in</a
        >
        <!--color from config file, button-->
        <a
          href="#"
          class="btn text-primery ml-2 border-primery md:border-2 hover:bg-primery hover:text-white transition ease-out duration-500"
          >Sing up</a
        >
        <!--color from config file, button-->
      </div>

      <header>
        <h2 class="text-gray-700 text-6xl font-semibold">Recipies</h2>
        <h3 class="text-2xl font-semibold">For me</h3>
      </header>

      <div>
        <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">
          Latest Recipes
        </h4>

        <div class="mt-8 grid lg:grid-cols-3 gap-10">
          <!-- grid -->
          <!-- cards go here -->
          <div class="card hover:shadow-lg">
            <!-- this class imported from style.css with @appy directive-->
            <img
              src="./assets/img/stew.jpg"
              alt="stew"
              class="w-full h-32 sm:h-48 object-cover"
            />
            <div class="m-4">
              <span class="font-bold">5 Bean Chilli Stew</span>
              <span class="block text-grey-500 text-sm">Recipe by Mario</span>
            </div>
            <!--Badges-->
            <div class="badge">
              <!-- this class imported from style.css with @appy directive-->
              <svg
                class="w-5 inline-block"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
              <!-- icon -->
              <span>25 min</span>
            </div>
          </div>
          <div class="card hover:shadow-lg">
            <!-- this class imported from style.css with @appy directive-->
            <img
              src="./assets/img/noodles.jpg"
              alt="stew"
              class="w-full h-32 sm:h-48 object-cover"
            />
            <div class="m-4">
              <span class="font-bold">Veg Nodless</span>
              <span class="block text-grey-500 text-sm">Recipe by Mario</span>
            </div>
            <!--Badges-->
            <div class="badge">
              <!-- this class imported from style.css with @appy directive-->
              <svg
                class="w-5 inline-block"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
              <!-- icon -->
              <span>25 min</span>
            </div>
          </div>
          <div class="card hover:shadow-lg">
            <!-- this class imported from style.css with @appy directive-->
            <img
              src="./assets/img/curry.jpg"
              alt="stew"
              class="w-full h-32 sm:h-48 object-cover"
            />
            <div class="m-4">
              <span class="font-bold">Tofu Curry</span>
              <span class="block text-grey-500 text-sm">Recipe by Mario</span>
            </div>
            <!--Badges-->
            <div class="badge">
              <!-- this class imported from style.css with @appy directive-->
              <svg
                class="w-5 inline-block"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
              <!-- icon -->
              <span>25 min</span>
            </div>
          </div>
        </div>

        <h4 class="font-bold mt-12 pb-2 border-b border-gray-200">
          Most Popular
        </h4>
        <div class="mt-8">
          <!-- cards go here  -->
        </div>

        <div class="flex justify-center">
          <div
            class="btn bg-secondary-100 text-secondary-200 hover:shadow-inner transform hover:scale-125 hover:bg-opacity-50 transition ease-out duration-300"
          >
            Load more
          </div>
          <!--color from config file, button-->
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",

  data: function() {
    return {
      isActive: true  // <-- data for burger menu
    };
  },
  methods: {
    toggleClass: function() {     // <-- method for burger menu
      this.isActive = !this.isActive;
    }
  }
};
</script>
