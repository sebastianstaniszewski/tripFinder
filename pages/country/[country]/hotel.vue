<template>
	<div>
		<div class="mt-32 flex">
			<SideBar />
			<NuxtPage />
		</div>
	</div>
</template>

<script setup>
	definePageMeta({
		layout: "custom",
	});
</script>
