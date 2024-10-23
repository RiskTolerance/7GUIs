<script lang="ts">
	let fahrenheit = $state('');
	let celsius = $state('');
	let error = $state('');
</script>

<div>
	<span class="prose"><h1>Temperature Converter</h1></span>

	<div>
		{#if error === ''}
			<p>Enter a number!</p>
		{:else}
			<p class="font-bold text-red-500">{error}</p>
		{/if}
	</div>
	<div class="flex gap-8">
		<div class="flex flex-col w-40">
			<label for="f">Fahrenheit</label>
			<input
				class="rounded"
				id="f"
				type="text"
				bind:value={fahrenheit}
				oninput={(e) => {
					const value = (e.target as HTMLInputElement).value;
					const isNum = /^\d+$/.test(value);
					if (value === '' || isNum) {
						error = '';
						celsius = ((parseInt(value) - 32) * (5 / 9)).toString();
					} else {
						fahrenheit = '';
						celsius = '';
						error = 'Please enter only numbers!';
					}
				}}
			/>
		</div>

		<div class="flex flex-col w-40">
			<label for="c">Celsius</label>
			<input
				class="rounded"
				id="c"
				type="text"
				bind:value={celsius}
				oninput={(e) => {
					const value = (e.target as HTMLInputElement).value;
					const isNum = /^\d+$/.test(value);
					if (value === '' || isNum) {
						error = '';
						fahrenheit = ((parseInt(value) * 9) / 5 + 32).toString();
					} else {
						fahrenheit = '';
						celsius = '';
						error = 'Please enter only numbers!';
					}
				}}
			/>
		</div>
	</div>
</div>
