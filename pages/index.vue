<script setup lang="ts">


</script>

<template>
    <h1 class="stone-100">
        Welcome to Nuxt.js!
    </h1>
	<DropdownMenu>
		<DropdownMenuTrigger as-child>
			<Button variant="outline">
				Open
			</Button>
		</DropdownMenuTrigger>
		<DropdownMenuContent class="w-56">
		<DropdownMenuLabel>My Account</DropdownMenuLabel>
		<DropdownMenuSeparator />
		<DropdownMenuItem>Profile</DropdownMenuItem>
		<DropdownMenuItem>Billing</DropdownMenuItem>
		<DropdownMenuItem>Team</DropdownMenuItem>
		<DropdownMenuItem>Subscription</DropdownMenuItem>
		</DropdownMenuContent>
	</DropdownMenu>
    
</template>