<script lang="ts">
	interface Resource {
		title: string;
		description: string;
		downloadUrl: string;
		tutorialUrl: string;
	}

	const resources: Resource[] = [
		{
			title: 'Adobe Flash CC 2015',
			description: 'Membuat animasi interaktif',
			downloadUrl: 'https://od.meong.club/kuy1415n/file14/Flash.Pro.CC.2015.15.0.1.u1.kuyhAa.7z',
			tutorialUrl:
				'https://drive.google.com/file/d/1ilXmzR3iqynDnvKLk4ztzyxO0nFJXYj2/view?usp=sharing'
		},
		{
			title: 'Visual Studio Code',
			description: 'Kode Editor',
			downloadUrl: 'https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user',
			tutorialUrl: '#'
		},
		{
			title: 'Packet Tracer',
			description: 'Simulasi jaringan komputer',
			downloadUrl:
				'https://drive.google.com/file/d/1WcjedzTFVInh8WtOuNJld_cZwHPo7LYY/view?usp=sharing',
			tutorialUrl: '#'
		}
	];
</script>

<div class="container mx-auto px-4 py-8">
	<h1 class="mb-8 text-center text-3xl font-bold">Aura Resources</h1>
	<div class="grid grid-cols-1 gap-6 md:grid-cols-2 lg:grid-cols-3">
		{#each resources as resource}
			<div class="overflow-hidden rounded-lg bg-white shadow-md">
				<div class="p-6">
					<h2 class="mb-2 text-xl font-semibold">{resource.title}</h2>
					<p class="mb-4 text-gray-600">{resource.description}</p>
					<div class="flex gap-4">
						<a
							href={resource.downloadUrl}
							class="inline-block rounded-md bg-blue-500 px-4 py-2 text-white transition-colors hover:bg-blue-600"
							>Download</a
						>
						<a
							href={resource.tutorialUrl}
							class="inline-block rounded-md bg-green-500 px-4 py-2 text-white transition-colors hover:bg-green-600"
							>Tutorial</a
						>
					</div>
				</div>
			</div>
		{/each}
	</div>
</div>

<style>
	:global(body) {
		background-color: #f0f0f0;
		font-family: 'Arial', sans-serif;
	}
</style>
