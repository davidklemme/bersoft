<script>
	import Impressum from "$lib/Components/Impressum.svelte";
import Skyline from "$lib/Components/Skyline.svelte";
	import SlideOver from "$lib/Components/SlideOver.svelte";

</script>


<div class="p-6 md:pt-24 mt-24 sm:mt-18 md:m-24 h-[80vh]">
    <div class="flex items-start justify-between h-full">
    <div class="flex flex-col justify-between h-full">        
        <div class="flex justify-between">
            <div>
                <div class="">
                    <h1 
                        class="
                            text-3xl sm:text-8xl font-extrabold font-sans
                            text-transparent bg-clip-text bg-gradient-to-br from-primary to-primary-content
                            ">Berliner <br>Softwareschmiede</h1>
                    <div class="text-3xl font-bold m-8 flex">
                        <div class="border-l-2 pr-2">
                        </div>
                        <div>
                            <h4>Software</h4>
                            <h4>Consulting</h4>
                        </div>
                    </div>
                    <div class="flex w-full h-full items-start justify-end ">
                        
                            <!-- <Skyline /> -->
                        
                    </div>
                </div>
            </div>
            
        </div>
            <div class="flex flex-col prose ml-8 mt-24 md:flex-row justify-start items-start md:items-center">
                <h2 class="m-0 mr-20 mb-8 md:mb-0 w-28">Portfolio</h2>
                    <a class="no-underline" href='https://www.cvcentral.io'><h4 class="m-0 ml-4 md:ml-0 mr-4 text-transparent bg-clip-text bg-gradient-to-br from-primary to-primary-content">cvcentral.io</h4></a>
                    <a class="no-underline" href='https://www.aeulogy.com'><h4 class="m-0 mr-4 ml-4 md:ml-0 text-transparent bg-clip-text bg-gradient-to-br from-accent to-primary">aeulogy.com</h4></a>
                    <h4 class="m-0 mr-4 ml-4 md:ml-0 text-transparent bg-clip-text bg-gradient-to-br from-secondary to-secondary-focus">service.vbg.de</h4>
                    <a class="no-underline" href='https://blog.cvcentral.io'><h4 class="m-0 mr-4 ml-4 md:ml-0 text-transparent bg-clip-text bg-gradient-to-br from-secondary to-slate-500">blog.cvcentral.io</h4></a>
                    <a class="no-underline" href='https://blog.aeulogy.com'><h4 class="m-0 mr-4 ml-4 md:ml-0 text-transparent bg-clip-text bg-gradient-to-br from-slate-500 to-primary">blog.aeulogy.com</h4></a>
            </div>        
            
        </div>
        <div >
            <SlideOver>
                <Impressum />
            </SlideOver>
        </div>
    </div>
   
</div>

