<script lang="ts">
	export let searchQuery: string;
</script>

<div class="search-bar">
	<input
		class="search-field"
		type="text"
		bind:value={searchQuery}
		placeholder="Search Pokemon..."
	/>
	<button class="search-clear" on:click={() => (searchQuery = "")}>
		Clear
	</button>
</div>

<style>
	.search-bar {
		display: flex;
		width: 100%;
	}

	.search-field {
		padding: 1rem;
		flex-grow: 1;
		font-size: large;
		border: none;
		border-bottom: 1px solid gray;
		outline: none;
	}

	.search-field:focus {
		border: none;
		border-bottom: 1px solid;
	}

	.search-clear {
		padding: 0 1rem;
		font-size: large;
		background-color: #f0f2f4;
		border: 1px solid #c3c3c5;
	}

	.search-clear:hover {
		background-color: #e0e1e4;
	}
</style>
