<script>
  // core components
  import TableItem from "./TableItem.svelte";
  import { fade } from "svelte/transition";

  const portfolio_logo = "../assets/img/portfolio_logo.png";
  const wip = "../assets/img/work_in_progress.png";
  const aws = "../assets/img/aws.png";
  const irobot = "../assets/img/irobot.jpg";
  const skrjecina = "../assets/img/skrejicina-fav.png";

  export let color = "light";
  export let size = "large";
</script>

<div
  transition:fade
  class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded {color ===
  'light'
    ? 'bg-white'
    : 'bg-red-800 text-white'}"
>
  <div class="rounded-t mb-0 px-4 py-3 border-0">
    <div class="flex flex-wrap items-center">
      <div class="relative w-full px-4 max-w-full flex-grow flex-1">
        <h3
          class="font-semibold text-lg {color === 'light'
            ? 'text-blueGray-700'
            : 'text-white'}"
        >
          Projects
        </h3>
      </div>
    </div>
  </div>
  <div class="block w-full overflow-x-auto">
    <!-- Projects table -->
    <table class="items-center w-full bg-transparent border-collapse">
      <thead>
        <tr>
          <th
            class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left {color ===
            'light'
              ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
              : 'bg-red-700 text-red-200 border-red-600'}"
          >
            Project
          </th>
          <th
            class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left {color ===
            'light'
              ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
              : 'bg-red-700 text-red-200 border-red-600'}"
          >
            Description
          </th>
          {#if size == "large"}
            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left {color ===
              'light'
                ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                : 'bg-red-700 text-red-200 border-red-600'}"
            >
              Status
            </th><th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left {color ===
              'light'
                ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                : 'bg-red-700 text-red-200 border-red-600'}"
            >
              Completion
            </th>

            <th
              class="px-6 align-middle border border-solid py-3 text-xs uppercase border-l-0 border-r-0 whitespace-nowrap font-semibold text-left {color ===
              'light'
                ? 'bg-blueGray-50 text-blueGray-500 border-blueGray-100'
                : 'bg-red-700 text-red-200 border-red-600'}">Technologies</th
            >
          {/if}
        </tr>
      </thead>
      <tbody>
        <TableItem
          name="IoT Dashboard"
          icon={wip}
          percentage="10%"
          status="starting"
          live_link=""
          technologies="Raspberry Pi, AWS IoT, Svelte"
          description="Dashboard showing Raspberry Pi collected data."
          small_description="IoT Dashboard"
          {size}
        />
        <TableItem
          name="Portfolio Page"
          icon={portfolio_logo}
          percentage="100%"
          status="completed"
          live_link="#"
          technologies="Svelte, Tailwind CSS, Azure"
          description="A portfolio page containing info about the author and his projects."
          small_description="Portfolio page"
          {size}
        />
        <TableItem
          name="ŠK Rječina"
          icon={skrjecina}
          percentage="100%"
          status="completed"
          live_link="https://www.sk-rjecina.hr"
          technologies="React, SASS"
          description="A website for a local chess club."
          small_description="Chess club website"
          {size}
        />
        <TableItem
          name="iRobot"
          icon={irobot}
          percentage="0"
          status="ongoing"
          live_link=""
          technologies="React, Angular, Material UI, TypeScript, Python, AWS"
          description="Cloud solutions."
          small_description="Cloud solutions."
          {size}
        />
      </tbody>
    </table>

    <!-- Certification -->
    <div class="rounded-t mb-0 px-4 py-3 border-0">
      <div class="flex flex-wrap items-center">
        <div class="relative w-full px-4 max-w-full flex-grow flex-1">
          <h3
            class="font-semibold text-lg {color === 'light'
              ? 'text-blueGray-700'
              : 'text-white'}"
          >
            Certification
          </h3>
        </div>
      </div>
    </div>
    <table class="items-center w-full bg-transparent border-collapse">
      <tbody>
        <tr>
          <th
            class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4 text-left flex items-center"
          >
            <img
              src={aws}
              class="h-12 w-12 bg-white rounded-full border"
              alt="..."
            />
            <span
              class="ml-3 font-bold {color === 'light'
                ? 'btext-blueGray-600'
                : 'text-whit'}"
            >
              {#if size == "large"}
                AWS Certified Solutions Architect - Associate
              {:else}
                AWS Associate Architect
              {/if}
            </span>
          </th>
          {#if size == "large"}
            <td
              class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
            >
              Jul-2021 - Jul-2024
            </td>
          {/if}
        </tr>
      </tbody>
    </table>
  </div>
</div>
