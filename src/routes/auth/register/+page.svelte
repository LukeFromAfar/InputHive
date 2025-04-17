<script lang="ts">
	import { Section, Register } from 'flowbite-svelte-blocks';
	import { Button, Checkbox, Label, Input } from 'flowbite-svelte';
</script>

<Section name="register" class="mt-16">
	<Register href="/" class="2xl:max-w-1/3 lg:max-w-2/5 md:max-w-2/3 sm:max-w-full">
		{#snippet top()}
			InputHive
		{/snippet}
		<div class="space-y-4 p-6 sm:p-8 md:space-y-6">
			<form class="flex flex-col space-y-6" action="/">
				<h3 class="p-0 text-xl font-medium text-gray-900 dark:text-white">Create and account</h3>
				<Label class="space-y-2">
					<span>Your email</span>
					<Input type="email" name="email" placeholder="name@company.com" required />
				</Label>
				<Label class="space-y-2">
					<span>Your password</span>
					<Input type="password" name="password" placeholder="•••••" required />
				</Label>
				<Label class="space-y-2">
					<span>Confirm password</span>
					<Input type="password" name="confirm-password" placeholder="•••••" required />
				</Label>
				<div class="flex items-start">
					<Checkbox>I accept the&nbsp;<a class="text-primary-600 dark:text-primary-500 font-medium underline hover:text-neutral-100" href="/">Terms and Conditions</a></Checkbox>
				</div>
				<div class="flex items-center my-4 *:px-4">
					<div class="flex-grow mx-2" style="border-top: 0.5px solid #e5e5e5;"></div>
					<p class="px-4 text-sm text-neutral-400">OR</p>
					<div class="flex-grow mx-2" style="border-top: 0.5px solid #e5e5e5;"></div>
				</div>
		
				<div class="flex flex-row justify-center pt-4 *:px-2">
					<a href="/" >
						<img src="/icons/login/github-mark-white.svg" alt="Github logo" class="w-10 h-10">
					</a>
					<a href="/">
						<img src="/icons/login/web_dark_rd_na.svg" alt="Google logo" class="w-10 h-10">
					</a>
				</div>
				<Button type="submit" class="w-full1">Create an account</Button>
				<div class="text-sm font-medium text-gray-500 dark:text-gray-300">
					Already have an account? <a href="/auth/login" class="text-primary-600 dark:text-primary-500 font-medium underline hover:text-neutral-100">Login here</a>
				</div>
			</form>
		</div>
	</Register>
</Section>