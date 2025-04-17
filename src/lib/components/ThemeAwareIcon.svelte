<script>
    export let src;
    export let alt;
    export let className = "w-10 h-10";
    
    // Determine which icon we're showing
    $: isGithub = src.includes('github');
    $: isGoogle = src.includes('web');
    
    // Hardcoded paths for light and dark versions
    $: darkModeSrc = isGithub ? "/icons/login/github-mark-white.svg" : 
                     isGoogle ? "/icons/login/web_dark_rd_na.svg" : 
                     src;
                     
    $: lightModeSrc = isGithub ? "/icons/login/github-mark.svg" : 
                      isGoogle ? "/icons/login/web_light_rd_na.svg" : 
                      src;
</script>

<!-- Dark mode icon -->
<img 
    src={darkModeSrc} 
    alt={alt} 
    class="{className} dark:block hidden" 
/>

<!-- Light mode icon -->
<img 
    src={lightModeSrc} 
    alt={alt} 
    class="{className} dark:hidden block" 
/>