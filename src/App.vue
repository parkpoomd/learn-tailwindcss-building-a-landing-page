<template>
  <div class="min-h-screen">
    <div class="relative overflow-hidden">
      <div class="hidden sm:block sm:absolute sm:inset-0" aria-hidden="true">
        <svg
          class="absolute bottom-0 right-0 transform translate-x-1/2 mb-48 text-gray-700 lg:top-0 lg:mt-28 lg:mb-0 xl:transform-none xl:translate-x-0"
          width="364"
          height="384"
          viewBox="0 0 364 384"
          fill="none"
        >
          <defs>
            <pattern
              id="eab71dd9-9d7a-47bd-8044-256344ee00d0"
              x="0"
              y="0"
              width="20"
              height="20"
              patternUnits="userSpaceOnUse"
            >
              <rect x="0" y="0" width="4" height="4" fill="curentColor" />
            </pattern>
          </defs>
          <rect
            width="364"
            height="384"
            fill="url(#eab71dd9-9d7a-47bd-8044-256344ee00d0)"
          />
        </svg>
      </div>
      <div class="relative">
        <div class="bg-gray-900 pt-6">
          <nav
            class="relative max-w-7xl mx-auto flex items-center justify-between px-4 sm:px-6"
            aria-label="Global"
          >
            <div class="flex items-center flex-1">
              <div class="flex items-center justify-between w-full md:w-auto">
                <a href="#">
                  <span class="sr-only">Workflow</span>
                  <img
                    class="h-8 w-auto sm:h-10"
                    src="./assets/workflow-mark-teal-200-cyan-400.svg"
                    alt=""
                  />
                </a>
                <div class="-mr-2 flex items-center md:hidden">
                  <button
                    @click="mainMenu = true"
                    type="button"
                    class="bg-gray-900 rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:bg-gray-800 focus:outline-none focus:ring-2 focus-ring-inset focus:ring-white"
                    aria-haspopup="true"
                  >
                    <span class="sr-only">Open main menu</span>
                    <svg
                      class="h-6 w-6"
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
                  </button>
                </div>
              </div>
              <div class="hidden space-x-10 md:flex md:ml-10">
                <a
                  href="#"
                  class="font-medium text-white hover:text-gray-300"
                  v-for="item in [
                    'Product',
                    'Features',
                    'Marketplace',
                    'Company',
                  ]"
                  :key="item"
                  >{{ item }}</a
                >
              </div>
            </div>
            <div class="hidden md:flex">
              <a
                href="#"
                class="inline-flex items-center px-4 py-2 border border-transparent text-sm font-medium rounded-md text-white bg-gray-600 hover:bg-gray-700"
              >
                Log in
              </a>
            </div>
          </nav>
        </div>
        <transition
          enter-active-class="duration-150 ease-out"
          enter-from-class="opacity-0 scale-95"
          enter-to-class="opacity-100 scale-100"
          leave-active-class="duration-100 ease-in"
          leave-from-class="opacity-100 scale-100"
          leave-to-class="opacity-0 scale-95"
        >
          <div
            v-show="mainMenu"
            class="absolute top-0 inset-x-0 p-2 transition transform origin-top-right md:hidden"
          >
            <div
              class="rounded-lg shadow-md bg-white ring-1 ring-black ring-opacity-5 overflow-hidden"
            >
              <div class="px-5 pt-4 flex items-center justify-between">
                <div>
                  <img
                    class="h-8 w-auto"
                    src="./assets/workflow-mark-teal-500-cyan-600.svg"
                    alt=""
                  />
                </div>
                <div class="-mr-2">
                  <button
                    @click="mainMenu = false"
                    type="button"
                    class="bg-white rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-cyan-600"
                  >
                    <span class="sr-only">Close menu</span>
                    <svg
                      class="h-6 w-6"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 24 24"
                      stroke="currentColor"
                    >
                      <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M6 18L18 6M6 6l12 12"
                      />
                    </svg>
                  </button>
                </div>
              </div>
              <div
                class="pt-5 pb-6"
                role="menu"
                aria-orientation="vertical"
                aria-labelledby="main-menu"
              >
                <div class="px-2 space-y-1" role="none">
                  <a
                    href="#"
                    class="block px-3 py-2 rounded-md text-base font-medium text-gray-900 hover:bg-gray-50"
                    role="menuitem"
                    v-for="item in [
                      'Product',
                      'Features',
                      'Marketplace',
                      'Company',
                    ]"
                    :key="item"
                    >{{ item }}</a
                  >
                </div>
                <div role="none" class="mt-6 px-5">
                  <a
                    href="#"
                    class="block text-center w-full py-3 px-4 rounded-md shadow bg-gradient-to-r from-teal-500 to-cyan-600 text-white font-medium hover:form-teal-600 hover:to-cyan-700"
                    >Start free trial</a
                  >
                </div>
                <div role="none" class="mt-6 px-5">
                  <p class="text-center text-base font-medium text-gray-500">
                    Existing customer?
                    <a href="#" class="text-gray-900 hover:underline">Login</a>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </transition>

        <main>
          <div class="pt-10 bg-gray-900">
            <div class="mx-auto max-w-7xl">
              <div class="lg:grid lg:grid-cols-12 lg:gap-8">
                <div
                  class="mx-auto max-w-md px-4 sm:max-w-2xl sm:px-6 sm:text-center lg:col-span-6 lg:text-left lg:flex lg:items-center"
                >
                  <div>
                    <a
                      href="#"
                      class="inline-flex items-center text-white bg-black rounded-full p-1 pr-2 sm:text-base lg:text-sm xl:text-base hover:text-gray-200"
                    >
                      <span
                        class="px-3 py-0.5 text-white text-xs font-semibold leading-5 uppercase tracking-wide bg-gradient-to-r from-teal-500 to-cyan-600 rounded-full"
                      >
                        We're hiring
                      </span>
                      <span class="ml-4 text-sm">Visit our careers page</span>
                      <svg
                        class="ml-2 h-5 w-5 text-gray-500"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M9 5l7 7-7 7"
                        />
                      </svg>
                    </a>
                    <h1
                      class="mt-4 text-4xl tracking-tight font-extrabold text-white sm:mt-5 sm:text-6xl lg:mt-6 xl:text-6xl"
                    >
                      <span class="block">A better way to</span>
                      <span
                        class="bg-clip-text text-transparent bg-gradient-to-r from-teal-200 to-cyan-400 block"
                        >ship web apps</span
                      >
                    </h1>
                    <p
                      class="mt-3 text-base text-gray-300 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl"
                    >
                      Anim aute id magna aliqua ad ad non deserunt sunt. Qui
                      irure qui Lorem cupidatat commode. Elit sunt amet fugiat
                      veniam occaecat fugiat.
                    </p>
                    <div class="mt-10 sm:mt-12">
                      <form action="#" class="sm:max-w-xl sm:mx-auto">
                        <div class="sm:flex">
                          <div class="min-w-0 flex-1">
                            <label for="email" class="sr-only"
                              >Email address</label
                            >
                            <input
                              type="email"
                              placeholder="Enter your email"
                              class="block w-full px-4 py-3 rounded-md border-0 text-base text-gray-900 placeholder-gray-500"
                            />
                          </div>
                          <div class="mt-3 sm:mt-0 sm:ml-3">
                            <button
                              type="submit"
                              class="block w-full py-3 px-4 rounded-md shadow bg-gradient-to-r from-teal-500 to-cyan-600 text-white font-medium hover:form-teal-600 hover:to-cyan-700"
                            >
                              Start free trial
                            </button>
                          </div>
                        </div>
                        <p class="mt-3 text-sm text-gray-300 sm:mt-4">
                          Start your free 14-day trial, no credit card
                          necessary. By providing your email, you agree to our
                          <a href="#" class="font-medium text-white"
                            >terms or service</a
                          >.
                        </p>
                      </form>
                    </div>
                  </div>
                </div>
                <div class="mt-12 -mb-16 sm:-mb-32">
                  <div class="mx-auto max-w-md px-4 sm:max-w-2xl sm:px-6">
                    <img
                      class="w-full"
                      src="./assets/cloud-illustration-teal-cyan.svg"
                      alt="Cloud infrastructure illustration"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Feature section with screenshot -->
          <div class="relative bg-gray-50 pt-16 sm:pt-24">
            <div class="mx-auto max-w-md px-4 text-center sm:px-6 sm:max-w-7xl">
              <h2
                class="text-base font-semibold tracking-wider text-cyan-600 uppercase"
              >
                Serverless
              </h2>
              <p
                class="mt-2 text-3xl font-extrabold text-gray-900 tracking-tight"
              >
                No server? No problem
              </p>
              <p class="mt-5 text-xl text-gray-500">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Natus
                officia nobis error optio dolore? Incidunt earum quod odit
                officiis esse ipsam excepturi autem amet eos omnis! Tempore
                totam impedit tempora!
              </p>
              <div class="mt-12 -mb-10">
                <img
                  class="rounded shadow-xl ring-1 ring-black ring-opacity-5"
                  src="./assets/green-project-app-screenshot.jpg"
                  alt=""
                />
              </div>
            </div>
          </div>

          <!-- Feature section with grid -->
          <div class="relative bg-white py-16 sm:py-24">
            <div class="mx-auto max-w-md px-4 text-center sm:max-w-7xl sm:px-6">
              <h2
                class="text-base font-semibold tracking-wider text-cyan-600 uppercase"
              >
                Deploy faster
              </h2>
              <p
                class="mt-2 text-3xl font-extrabold text-gray-900 tracking-tight"
              >
                Everything you need to deploy your app
              </p>
              <p class="mt-5 text-xl text-gray-500">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Natus
                officia nobis error optio dolore? Incidunt earum quod odit
                officiis esse ipsam excepturi autem amet eos omnis! Tempore
                totam impedit tempora!
              </p>
              <div class="mt-12">
                <div class="grid grid-cols-1 gap-8 sm:grid-cols-2">
                  <div
                    class="pt-6"
                    v-for="item in featureItems"
                    :key="item.title"
                  >
                    <div class="flow-root bg-gray-50 rounded-lg px-6 pb-8">
                      <div class="-mt-6">
                        <div>
                          <span
                            class="inline-flex items-center justify-center p-3 bg-gradient-to-r from-teal-500 to-cyan-600 rounded-md shadow-lg"
                          >
                            <span v-html="item.icon"></span>
                          </span>
                        </div>
                        <h3
                          class="mt-8 text-lg font-medium text-gray-900 tracking-tight"
                        >
                          {{ item.title }}
                        </h3>
                        <p class="mt-5 text-base text-gray-500">
                          Lorem ipsum dolor sit amet consectetur adipisicing
                          elit. Iusto at et corrupti optio soluta,
                          necessitatibus dicta.
                        </p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Testimonial section -->
          <div class="pb-16 bg-gradient-to-r from-teal-500 to-cyan-600">
            <div class="relative">
              <div class="absolute inset-x-0 top-0 h-1/2 bg-white"></div>
              <div class="mx-auto max-w-md px-4 sm:max-w-7xl sm:px-6">
                <div
                  class="aspect-w-10 aspect-h-6 rounded-xl shadow-xl overflow-hidden sm:aspect-w-16 sm:aspect-h-6"
                >
                  <img
                    class="object-cover"
                    src="https://images.unsplash.com/photo-1520333789090-1afc82db536a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2102&q=80"
                    alt=""
                  />
                </div>
              </div>
            </div>
            <div class="mt-12">
              <div class="mx-auto max-w-md px-4 sm:max-w-7xl sm:px-6">
                <blockquote>
                  <div>
                    <svg
                      class="h-12 w-12 text-white opacity-25"
                      fill="currentColor"
                      viewBox="0 0 32 32"
                      aria-hidden="true"
                    >
                      <path
                        d="M9.352 4C4.456 7.456 1 13.12 1 19.36c0 5.088 3.072
                    8.064 6.624 8.064 3.36 0 5.856-2.688 5.856-5.856
                    0-3.168-2.208-5.472-5.088-5.472-.576 0-1.344.096-1.536.192.48-3.264 3.552-7.104 6.624-9.024L9.352 4zm16.512 0c-4.8 3.456-8.256 9.12-8.256 15.36 0 5.088 3.072 8.064 6.624 8.064 3.264 0 5.856-2.688 5.856-5.856 0-3.168-2.304-5.472-5.184-5.472-.576 0-1.248.096-1.44.192.48-3.264 3.456-7.104 6.528-9.024L25.864 4z"
                      />
                    </svg>
                    <p class="mt-6 text-2xl font-medium text-white">
                      Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                      Quidem ea obcaecati et voluptatum provident modi autem,
                      harum ab accusantium! Dolores architecto harum.
                    </p>
                  </div>
                  <footer class="mt-6">
                    <p class="text-base font-medium text-white">Judith Black</p>
                    <p class="text-base font-medium text-cyan-100">
                      CEO at PureInsights
                    </p>
                  </footer>
                </blockquote>
              </div>
            </div>
          </div>

          <!-- Blog section -->
          <div class="relative bg-gray-50 py-16 px-4 sm:px-6 sm:py-24 lg:px-8">
            <div class="relative mx-auto max-w-md sm:max-w-7xl">
              <div class="text-center">
                <p
                  class="text-base font-semibold tracking-wider text-cyan-600 uppercase"
                >
                  Learn
                </p>
                <h2
                  class="mt-2 text-3xl font-extrabold text-gray-900 tracking-tight"
                >
                  Helpful Resources
                </h2>
                <p class="mt-5 text-xl text-gray-500">
                  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                  Natus officia nobis error optio dolore? Incidunt earum quod
                  odit officiis esse ipsam excepturi autem amet eos omnis!
                  Tempore totam impedit tempora!
                </p>
              </div>
              <div
                class="mt-12 max-w-lg mx-auto grid gap-6 lg:grid-cols-3 lg:max-w-none"
              >
                <div
                  class="flex flex-col rounded-lg shadow-lg overflow-hidden"
                  v-for="item in blogItems"
                  :key="item.title"
                >
                  <div flex-shrink-0>
                    <img
                      :src="
                        `https://images.unsplash.com/photo-${item.image}?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80`
                      "
                      alt=""
                    />
                  </div>
                  <div
                    class="flex-1 bg-white p-6 flex flex-col justify-between"
                  >
                    <div class="flex-1">
                      <p class="text-sm font-medium text-cyan-600">
                        <a href="#" class="hover:underline">
                          {{ item.category }}
                        </a>
                      </p>
                      <a href="#" class="block mt-2">
                        <p class="text-xl font-semibold text-gray-900">
                          {{ item.title }}
                        </p>
                        <p class="mt-3 text-base text-gray-500">
                          {{ item.description }}
                        </p>
                      </a>
                    </div>
                    <div class="mt-6 flex items-center">
                      <div class="flex-shrink-0">
                        <a href="#">
                          <span class="sr-only">{{ item.author }}</span>
                          <img
                            class="h-10 w-10 rounded-full"
                            :src="
                              `https://images.unsplash.com/photo-${item.avatar}?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80`
                            "
                            alt=""
                          />
                        </a>
                      </div>
                      <div class="ml-3">
                        <p class="text-sm font-medium text-gray-900">
                          <a href="#" class="hover:underline">
                            {{ item.author }}
                          </a>
                        </p>
                        <div class="flex space-x-1 text-sm text-gray-500">
                          <time datetime="{{ item.datetime }}">
                            {{ item.date }}
                          </time>
                          <span aria-hidden="true">
                            &middot;
                          </span>
                          <span> {{ item.readingLength }} min read </span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- CTA Section -->
          <div class="relative bg-gray-900">
            <div
              class="relative h-56 bg-indigo-600 sm:h-72 md:absolute md:left-0 md:h-full md:w-1/2"
            >
              <img
                class="w-full h-full object-cover"
                src="https://images.unsplash.com/photo-1525130413817-d45c1d127c42?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1920&q=60&sat=-100"
                alt=""
              />
              <div
                aria-hidden="true"
                class="absolute inset-0 bg-gradient-to-r from-teal-500 to-cyan-600"
                style="mix-blend-mode: multiply;"
              ></div>
            </div>
            <div
              class="relative mx-auto max-w-md px-4 py-12 sm:max-w-7xl sm:px-6 lg:px-8 lg:py-16"
            >
              <div class="md:ml-auto md:w-1/2 md:pl-10">
                <h2
                  class="text-base font-semibold uppercase tracking-wider text-gray-300"
                >
                  Award winning support
                </h2>
                <p
                  class="mt-2 text-white text-3xl font-extrabold tracking-tight sm:text-4xl"
                >
                  We're here to help
                </p>
                <p class="mt-3 text-lg text-gray-300">
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit.
                  Maiores, similique cupiditate, repellat voluptates est odio
                  eveniet soluta eos, accusantium voluptas animi beatae
                  voluptatibus sunt consequuntur eligendi optio ea dignissimos
                  blanditiis.
                </p>
                <div class="mt-8">
                  <div class="inline-flex rounded-md shadow">
                    <a
                      href="#"
                      class="inline-flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-gray-900 bg-white hover:bg-gray-50"
                      >Visit the help center
                      <svg
                        class="-mr-1 ml-3 h-5 w-5 text-gray-400"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke="currentColor"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          stroke-width="2"
                          d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
                        /></svg
                    ></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </main>

        <footer class="bg-gray-50" aria-labelledby="footerHeading">
          <h2 id="footerHeading" class="sr-only">
            Footer
          </h2>
          <div
            class="mx-auto max-w-md py-12 px-4 sm:max-w-7xl sm:px-6 lg:py-16 lg:px-8"
          >
            <div class="xl:grid xl:grid-cols-3 xl:gap-8">
              <div class="space-y-8 xl:col-span-1">
                <img
                  class="h-10"
                  src="./assets/workflow-mark-gray-300.svg"
                  alt="Company name"
                />
                <p>
                  Making the world a better place through constructing elegant
                  hierarchies.
                </p>
                <div class="flex space-x-6">
                  <a
                    href="#"
                    class="text-gray-400 hover:text-gray-500"
                    v-for="item in social"
                    :key="item.name"
                  >
                    <span class="sr-only">
                      {{ item.name }}
                    </span>
                    <span v-html="item.icon"></span>
                  </a>
                </div>
              </div>
              <div class="mt-12 grid grid-cols-2 gap-8 xl:mt-0 xl:col-span-2">
                <div class="md:grid md:grid-cols-2 md:gap-8">
                  <div>
                    <h3
                      class="text-sm font-semibold text-gray-400 tracking-wider uppercase"
                    >
                      Solutions
                    </h3>
                    <ul class="mt-4 space-y-4">
                      <li v-for="(item, i) in solutions" :key="i">
                        <a
                          href="#"
                          class="text-base text-gray-500 hover:text-gray-900"
                        >
                          {{ item }}
                        </a>
                      </li>
                    </ul>
                  </div>
                  <div class="mt-12 md:mt-0">
                    <h3
                      class="text-sm font-semibold text-gray-400 tracking-wider uppercase"
                    >
                      Support
                    </h3>
                    <ul class="mt-4 space-y-4">
                      <li v-for="(item, i) in support" :key="i">
                        <a
                          href="#"
                          class="text-base text-gray-500 hover:text-gray-900"
                        >
                          {{ item }}
                        </a>
                      </li>
                    </ul>
                  </div>
                </div>
                <div class="md:grid md:grid-cols-2 md:gap-8">
                  <div>
                    <h3
                      class="text-sm font-semibold text-gray-400 tracking-wider uppercase"
                    >
                      Company
                    </h3>
                    <ul class="mt-4 space-y-4">
                      <li v-for="(item, i) in company" :key="i">
                        <a
                          href="#"
                          class="text-base text-gray-500 hover:text-gray-900"
                        >
                          {{ item }}
                        </a>
                      </li>
                    </ul>
                  </div>
                  <div class="mt-12 md:mt-0">
                    <h3
                      class="text-sm font-semibold text-gray-400 tracking-wider uppercase"
                    >
                      Legal
                    </h3>
                    <ul class="mt-4 space-y-4">
                      <li v-for="(item, i) in legal" :key="i">
                        <a
                          href="#"
                          class="text-base text-gray-500 hover:text-gray-900"
                        >
                          {{ item }}
                        </a>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
            <div class="mt-12 border-t border-gray-200 pt-8">
              <p class="text-base text-gray-400 xl:text-center">
                &copy; 2020 Workflow, Inc, All rights reserved.
              </p>
            </div>
          </div>
        </footer>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      mainMenu: false,
      featureItems: [
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12" />
          </svg>`,
          title: 'Push to Deploy',
        },
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
          </svg>`,
          title: 'SSL Certificates',
        },
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15" />
          </svg>`,
          title: 'Simple Queues',
        },
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
          </svg>`,
          title: 'Advanced Security',
        },
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z" />
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
          </svg>`,
          title: 'Powerful API',
        },
        {
          icon: `<svg class="h-6 w-6 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 12h14M5 12a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v4a2 2 0 01-2 2M5 12a2 2 0 00-2 2v4a2 2 0 002 2h14a2 2 0 002-2v-4a2 2 0 00-2-2m-2-4h.01M17 16h.01" />
          </svg>`,
          title: 'Database Backups',
        },
      ],
      blogItems: [
        {
          title: 'Boost your conversion rate',
          date: 'Mar 16, 2020',
          datetime: '2020-03-16',
          category: 'Article',
          image: '1496128858413-b36217c2ce36',
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Quidem ea obcaecati et voluptatum provident modi autem, harum ab accusantium!
          Dolores architecto`,
          author: 'Roel Aufderehar',
          avatar: '1472099645785-5658abf4ff4e',
          readingLength: '6',
        },
        {
          title: 'How to use search engine optimization to drive sales',
          date: 'Mar 10, 2020',
          datetime: '2020-03-10',
          category: 'Video',
          image: '1547586696-ea22b4d4235d',
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Quidem ea obcaecati et voluptatum provident modi autem, harum ab accusantium!
          Dolores architecto`,
          author: 'Brenna Goyette',
          avatar: '1550525811-e5869dd03032',
          readingLength: '4',
        },
        {
          title: 'Improve your customer experience',
          date: 'Feb 12, 2020',
          datetime: '2020-02-12',
          category: 'Case Study',
          image: '1492724441997-5dc865305da7',
          description: `Lorem ipsum dolor sit amet consectetur, adipisicing elit.
          Quidem ea obcaecati et voluptatum provident modi autem, harum ab accusantium!
          Dolores architecto`,
          author: 'Daniela Metz',
          avatar: '1487412720507-e7ab37603c6f',
          readingLength: '11',
        },
      ],
      solutions: ['Marketing', 'Analytics', 'Commerce', 'Insights'],
      support: ['Pricing', 'Documentation', 'Guides', 'API Status'],
      company: ['About', 'Blog', 'Jobs', 'Press', 'Partners'],
      legal: ['Claim', 'Privacy', 'Terms'],
      social: [
        {
          name: 'Facebook',
          icon: `<svg class="h-6 w-6 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="none" viewBox="0 0 24 24"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>`,
        },
        {
          name: 'Instagram',
          icon: `<svg class="h-6 w-6 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="none" viewBox="0 0 24 24"><path d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913.306.788.717 1.459 1.384 2.126.667.666 1.336 1.079 2.126 1.384.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558.788-.306 1.459-.718 2.126-1.384.666-.667 1.079-1.335 1.384-2.126.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913-.306-.789-.718-1.459-1.384-2.126C21.319 1.347 20.651.935 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227-.224.562-.479.96-.899 1.382-.419.419-.824.679-1.38.896-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421-.569-.224-.96-.479-1.379-.899-.421-.419-.69-.824-.9-1.38-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678c-3.405 0-6.162 2.76-6.162 6.162 0 3.405 2.76 6.162 6.162 6.162 3.405 0 6.162-2.76 6.162-6.162 0-3.405-2.76-6.162-6.162-6.162zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405c0 .795-.646 1.44-1.44 1.44-.795 0-1.44-.646-1.44-1.44 0-.794.646-1.439 1.44-1.439.793-.001 1.44.645 1.44 1.439z"/></svg>`,
        },
        {
          name: 'Twitter',
          icon: `<svg class="h-6 w-6 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="none" viewBox="0 0 24 24"><path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/></svg>`,
        },
        {
          name: 'GitHub',
          icon: `<svg class="h-6 w-6 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="none" viewBox="0 0 24 24"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>`,
        },
        {
          name: 'Dribbble',
          icon: `<svg class="h-6 w-6 text-gray-400" xmlns="http://www.w3.org/2000/svg" fill="currentColor" stroke="none" viewBox="0 0 24 24"><title>Dribbble icon</title><path d="M12 24C5.385 24 0 18.615 0 12S5.385 0 12 0s12 5.385 12 12-5.385 12-12 12zm10.12-10.358c-.35-.11-3.17-.953-6.384-.438 1.34 3.684 1.887 6.684 1.992 7.308 2.3-1.555 3.936-4.02 4.395-6.87zm-6.115 7.808c-.153-.9-.75-4.032-2.19-7.77l-.066.02c-5.79 2.015-7.86 6.025-8.04 6.4 1.73 1.358 3.92 2.166 6.29 2.166 1.42 0 2.77-.29 4-.814zm-11.62-2.58c.232-.4 3.045-5.055 8.332-6.765.135-.045.27-.084.405-.12-.26-.585-.54-1.167-.832-1.74C7.17 11.775 2.206 11.71 1.756 11.7l-.004.312c0 2.633.998 5.037 2.634 6.855zm-2.42-8.955c.46.008 4.683.026 9.477-1.248-1.698-3.018-3.53-5.558-3.8-5.928-2.868 1.35-5.01 3.99-5.676 7.17zM9.6 2.052c.282.38 2.145 2.914 3.822 6 3.645-1.365 5.19-3.44 5.373-3.702-1.81-1.61-4.19-2.586-6.795-2.586-.825 0-1.63.1-2.4.285zm10.335 3.483c-.218.29-1.935 2.493-5.724 4.04.24.49.47.985.68 1.486.08.18.15.36.22.53 3.41-.43 6.8.26 7.14.33-.02-2.42-.88-4.64-2.31-6.38z"/></svg>`,
        },
      ],
    };
  },
};
</script>
