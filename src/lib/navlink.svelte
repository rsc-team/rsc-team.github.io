<script lang="ts">
    let {
        label = 'NavLabel',
        link = '',
        newtab = false,
        textclass = "transition-all text-white"
    } = $props()
</script>


<a href={link} 
   target={newtab ? "_blank" : undefined}
   rel={newtab ? "noopener noreferrer" : undefined}
   class="flex justify-center items-center text-center pl-4 pr-4
           text-2xl
           text-shadow-lg/45
           font-sweetsquare
           font-bold
           hover:underline
           
           "

>
<p class={textclass}>
{label}
</p>

</a>