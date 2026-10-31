<!-----
Nav link
------->

<script lang="ts">
    let {
        label = 'NavLabel',
        link = '',
        newtab = false,
        textclass = "transition-all text-white hover:text-white navigation-button"
    } = $props()
</script>


<a href={link} 
   target={newtab ? "_blank" : undefined}
   rel={newtab ? "noopener noreferrer" : undefined}
   class="flex justify-center items-center text-center pl-4 pr-4
           text-2xl
           drop-shadow-med
           font-sweetsquare
           font-bold
           transition-all
           h-10
           solar-clip-rectangle 
           
           
           bg-red
           sm:bg-transparent
           mb-5
           sm:mb-0
           hover:bg-red

           hover:text-white
           hover:border-navy
           "
>
<p class={textclass}>
{label}
</p>

</a>