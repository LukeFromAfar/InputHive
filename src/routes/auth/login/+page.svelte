<script lang="ts">
    import { Section, Register } from 'flowbite-svelte-blocks';
    import { Button, Label, Input } from 'flowbite-svelte';
    import ThemeAwareIcon from '$lib/components/ThemeAwareIcon.svelte';
</script>

<Section name="login" class="mt-16">
    <Register href="/" class="2xl:max-w-1/3 lg:max-w-2/5 md:max-w-2/3 sm:max-w-full">
        {#snippet top()}
            InputHive
        {/snippet}
        <div class="space-y-4 p-6 sm:p-8 md:space-y-6">
            <form class="flex flex-col space-y-6" action="/">
                <h3 class="p-0 text-xl font-medium text-gray-900 dark:text-white">Log in</h3>
                <Label class="space-y-2">
                    <span>Your email</span>
                    <Input type="email" name="email" placeholder="name@company.com" required />
                </Label>
                <Label class="space-y-2">
                    <span>Your password</span>
                    <Input type="password" name="password" placeholder="•••••" required />
                </Label>
                <div class="flex items-center my-4 *:px-4">
                    <div class="flex-grow mx-2" style="border-top: 0.5px solid #e5e5e5;"></div>
                    <p class="px-4 text-sm text-neutral-400">OR</p>
                    <div class="flex-grow mx-2" style="border-top: 0.5px solid #e5e5e5;"></div>
                </div>
        
                <div class="flex flex-row justify-center mt-4 *:px-2">
                	<a href="/" class=" rounded-lg hover:bg-neutral-100 dark:hover:bg-neutral-800 transition">
                        <ThemeAwareIcon src="/icons/login/github-mark-white.svg" alt="Github logo" />
                    </a>
                    <a href="/" class="rounded-lg hover:bg-neutral-100 dark:hover:bg-neutral-800 transition">
                        <ThemeAwareIcon src="/icons/login/web_dark_rd_na.svg" alt="Google logo" />
                    </a>
                </div>
                <Button type="submit" class="w-full">Log in</Button>
                <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
                    Don´t have an account yet? <a href="/auth/register" class="text-primary-600 dark:text-primary-500 font-medium underline hover:text-neutral-100">Register here</a>
                </div>
            </form>
        </div>
    </Register>
</Section>