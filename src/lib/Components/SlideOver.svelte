<script lang="ts">
  import { fade, fly } from "svelte/transition";
    let iconSrc = '/Vector_Menu.svg'
    let visible = false;
    function handleClose() {
        let modal = document.getElementById("slide-over");
        modal?.classList.add("hidden");

        let menuIcon = document.getElementById("menu-slide");
        menuIcon?.classList.remove("hidden");
        visible = false;
    }
    function handleOpen() {
        let modal = document.getElementById("slide-over");
        modal?.classList.remove("hidden");
        let menuIcon = document.getElementById("menu-slide");
        menuIcon?.classList.add("hidden");

        visible = true;
    }
</script>

<div>
<div id="menu-slide">
    <img src={iconSrc} alt="menu" class="w-4 h-4md:w-8 md:h-8" on:click={handleOpen} on:keydown={handleOpen} on:keypress={handleOpen}  />
</div>
<div in:fly="{{ x: 200, duration: 500 }}" out:fade id="slide-over" class="hidden relative z-10" aria-labelledby="slide-over-title" role="dialog" aria-modal="true">
    <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-all"></div>
    
    <div class="fixed inset-0 overflow-hidden">
      <div class="absolute inset-0 overflow-hidden">
        <div class="pointer-events-none fixed inset-y-0 right-0 flex max-w-full pl-10">
          {#if visible}
            <div  in:fly="{{ x: 400, duration: 2000 }}" out:fly="{{ x:400, duration: 1000 }}" class="pointer-events-auto relative w-screen max-w-2xl ease-in-out duration-1000">
              <div class="absolute top-0 left-0 -ml-8 flex pt-4 pr-2 sm:-ml-10 sm:pr-4">
                <button on:click={handleClose} type="button" class="rounded-md text-gray-300 hover:text-white focus:outline-none focus:ring-2 focus:ring-white">
                  <span class="sr-only">Close panel</span>
                  <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                </button>
              </div>
    
              <div class="flex h-full flex-col overflow-y-scroll bg-slate-900 py-6 shadow-xl">
                <div class="px-4 sm:px-6">
                  <h2 class="text-3xl leading-6 text-white" id="slide-over-title"></h2>
                </div>
                <div class="relative mt-6 flex-1 px-4 sm:px-6">
                  <slot />
                </div>
              </div>
            </div>
          {/if}
        </div>
      </div>
    </div>
  </div>
</div>