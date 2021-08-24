<script>
  export let icon;
  export let name;
  export let status;
  export let percentage;
  export let live_link;
  export let technologies;
  export let color = "light";
  export let description;
  export let size = "large";
  export let small_description;
</script>

<tr>
  <th
    class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4 text-left flex items-center"
  >
    <img src={icon} class="h-12 w-12 bg-white rounded-full border" alt="..." />
    <span
      class="ml-3 font-bold {color === 'light'
        ? 'btext-blueGray-600'
        : 'text-whit'}"
    >
      {#if live_link != ""}
        <a
          class="hover:text-emerald-500 mr-1"
          target="_blank"
          rel="noopener noreferrer"
          href={live_link}
          >{#if size == "large"}
            {name}
          {/if}</a
        >
      {:else if size == "large"}
        {name}
      {/if}
    </span>
  </th>

  <td
    class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
  >
    {#if size == "large"}
      {description}
    {:else}
      {small_description}
    {/if}
  </td>
  {#if size == "large"}
    <td
      class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
    >
      <i
        class="fas fa-circle {status == 'starting'
          ? 'text-orange-500 mr-2'
          : 'text-emerald-500 mr-2'} "
      />
      {status}
    </td>

    <td
      class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
    >
      <div class="flex items-center">
        <span class="mr-2">{percentage != "0" ? percentage : ""}</span>
        <div class="relative w-full">
          <div
            class="overflow-hidden h-2 text-xs flex rounded {status ==
            'starting'
              ? 'bg-orange-200'
              : 'bg-emerald-200'} "
          >
            <div
              style="width: {percentage};"
              class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center {status ==
              'starting'
                ? 'bg-orange-500'
                : 'bg-emerald-500'}"
            />
          </div>
        </div>
      </div>
    </td>

    <td
      class="border-t-0 px-6 align-middle border-l-0 border-r-0 text-xs whitespace-nowrap p-4"
    >
      {technologies}
    </td>
  {/if}
</tr>
