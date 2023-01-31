<script lang="ts">
	export let title: string
	export let description: string
</script>

<div class="flex flex-col justify-between p-4 leading-normal bg-gray-500 rounded drop-shadow-lg">
	<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{title}</h5>
	<p class="mb-3 font-normal text-gray-900">{description}</p>
</div>
