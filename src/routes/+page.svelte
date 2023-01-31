<script lang="ts">
	import { tasks } from '../mockData';
	import Card from '../components/Card.svelte';

	const todos = tasks.filter((task) => task.status === 'TODO');
	const inProgress = tasks.filter((task) => task.status === 'IN_PROGRESS');
	const dones = tasks.filter((task) => task.status === 'DONE');

	const columns = [
		{ title: 'Todo', data: todos },
		{ title: 'In Progress', data: inProgress },
		{ title: 'Done', data: dones }
	];
</script>

<main class="grid grid-cols-3 gap-12 p-4 h-screen bg-gray-900">
	{#each columns as column}
		<section class="flex flex-col gap-4 p-4 rounded">
			<h2 class="text-white">{column.title}</h2>
			{#each column.data as card}
				<Card title={card.title} description={card.message} />
			{/each}
		</section>
	{/each}
</main>
