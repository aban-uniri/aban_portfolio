<script>
  // core components
  import Navbar from "components/Navbars/Navbar.svelte";
  import ProjectsTable from "components/ProjectsTable/ProjectsTable.svelte";
  import Technologies from "components/Technologies/technologies.svelte";
  import { fade } from "svelte/transition";

  const profileImage = "/assets/img/2020-03-09.jpg";
</script>

<div transition:fade>
  <Navbar />
  <main class="profile-page">
    <section class="relative block h-500-px">
      <div
        class="absolute top-0 w-full h-full bg-center bg-cover"
        style="
        background-image: url(https://images.unsplash.com/photo-1497032628192-86f99bcd76bc?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80);
        "
      >
        <span
          id="blackOverlay"
          class="w-full h-full absolute opacity-50 bg-black"
        />
      </div>
      <div
        class="top-auto bottom-0 left-0 right-0 w-full absolute pointer-events-none overflow-hidden h-70-px"
        style="transform: translateZ(0);"
      >
        <svg
          class="absolute bottom-0 overflow-hidden"
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="none"
          version="1.1"
          viewBox="0 0 2560 100"
          x="0"
          y="0"
        >
          <polygon
            class="text-blueGray-200 fill-current"
            points="2560 0 2560 100 0 100"
          />
        </svg>
      </div>
    </section>
    <section class="relative py-16 bg-blueGray-200">
      <div class="container mx-auto px-4">
        <div
          class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-xl rounded-lg -mt-64"
        >
          <div class="px-6">
            <button
              class="absolute hidden md:block top-0 right-0 mt-4 mr-4 bg-red-400 active:bg-red-500 uppercase text-white font-bold hover:shadow-md shadow text-xs px-4 py-2 rounded outline-none focus:outline-none  ease-linear transition-all duration-150"
              type="button"
              onclick="window.open('https://resume.io/r/u20Yhu7FH?fbclid=IwAR0RKkWErFoVQH0CW3lWtS_zLzNKlc8v4DzgzmlgUCRHhE7QIAsqNQr9Jko', '_blank')"
            >
              Curiculum Vitae
            </button>
            <div class="flex flex-wrap justify-center">
              <div class="w-full lg:w-3/12 px-4 lg:order-2 flex justify-center">
                <div class="relative justify-center">
                  <img
                    alt="ProfileImage"
                    src={profileImage}
                    class="shadow-xl rounded-full h-auto align-middle border-none absolute -m-16 -ml-21 lg:-ml-16 max-w-150-px"
                  />
                </div>
              </div>
              <div
                class="w-full lg:w-4/12 px-4 lg:order-3 lg:text-right lg:self-center text-center"
              >
                <div class="py-6 px-3 mt-32 sm:mt-0  mx-auto ">
                  <span class="inline-block align-middle">
                    <button
                      class=" md:hidden  bg-red-400 active:bg-red-500 uppercase text-white font-bold hover:shadow-md shadow text-xs px-4 py-2 rounded outline-none focus:outline-none sm:mr-2 mb-1 ease-linear transition-all duration-150"
                      type="button"
                      onclick="window.open('https://resume.io/r/u20Yhu7FH?fbclid=IwAR0RKkWErFoVQH0CW3lWtS_zLzNKlc8v4DzgzmlgUCRHhE7QIAsqNQr9Jko', '_blank')"
                    >
                      Curiculum Vitae
                    </button>
                  </span>
                </div>
              </div>
              <div class="w-full lg:w-4/12 px-4 lg:order-1" />
            </div>
            <div class="text-center mt-10">
              <h3
                class="text-4xl font-semibold leading-normal text-blueGray-700 mb-2"
              >
                Antonio Ban
              </h3>
              <div
                class="text-sm leading-normal mt-0 mb-2 text-blueGray-400 font-bold uppercase"
              >
                <i
                  class="fas fa-map-marker-alt mr-2 text-lg text-blueGray-400"
                />
                Rijeka, Croatia
              </div>
              <div class="mb-2 text-blueGray-600 mt-5">
                <i class="fas fa-briefcase mr-2 text-lg text-blueGray-400" />
                Fullstack Developer - iOLAP
              </div>
              <div class="mb-2 text-blueGray-600">
                <i class="fas fa-university mr-2 text-lg text-blueGray-400" />
                University of Rijeka, Department of Informatics
              </div>
            </div>

            <div class="mt-2 py-3 border-t border-blueGray-200 text-center">
              <div class="flex flex-wrap justify-center">
                <div class="w-full lg:w-9/12 px-4">
                  <h1 class="font-semibold text-lg my-2">About</h1>
                  <p class="mb-4 text-lg leading-relaxed text-blueGray-700">
                    Hi! My name is Antonio Ban and I'm a programmer that likes
                    to try out all of the new upcoming tools, currently employed
                    by iOLAP as a Fullstack developer working for iRobot and
                    creating solutions in the cloud. Loves his dog, playing the
                    guitar and an occasional basketball game.
                  </p>
                  <p class="mb-4 text-lg leading-relaxed text-blueGray-700">
                    Here you can find a list of projects that I worked on,
                    currently working on, or am planning to do. I'm most
                    familliar with React/Python on AWS and I'm trying to expand
                    my developer experience with side-projects that use
                    different frameworks/programming languages or different
                    cloud service providers.
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div
            class="hidden md:block mt-2 py-3 border-t border-blueGray-200 text-center"
          >
            <h1 class="font-semibold text-lg my-3">Technologies</h1>
            <br />

            <Technologies />
          </div>
        </div>

        <div class="hidden lg:block">
          <ProjectsTable />
        </div>
        <div class="lg:hidden">
          <ProjectsTable size={"small"} />
        </div>
      </div>
    </section>
  </main>
</div>
