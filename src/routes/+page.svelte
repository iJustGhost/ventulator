<script lang="ts">
	let binary: string = '??????????';
	let hexa: string = '??????????';
	let octal: string = '??????????';
	let textBoxValue: string = '';

	function doConvert() {
		if (parseInt(textBoxValue) >= 0 && parseInt(textBoxValue) <= 10000) {
			binary = parseInt(textBoxValue).toString(2);
			hexa = parseInt(textBoxValue).toString(16);
			octal = parseInt(textBoxValue).toString(8);
			return;
		}
		binary = 'Must be a number between 0 & 10,000!';
		hexa = 'Must be a number between 0 & 10,000!';
		octal = 'Must be a number between 0 & 10,000!';
	}
</script>

<p class="mt-4 text-center text-3xl">👻 Ventulator 👻</p>

<div class="mt-8 flex w-full items-center justify-center">
	<input
		placeholder="Enter Number"
		type="text"
		bind:value={textBoxValue}
		class="h-9 w-1/2 rounded-l-full border-0 bg-emerald-700 px-2 text-2xl text-gray-200 outline-none"
	/>
	<button
		class="h-9 cursor-pointer rounded-r-full bg-emerald-700 px-4 text-2xl text-gray-200 outline-none"
		on:click={doConvert}>Convert</button
	>
</div>

<div class="mt-8">
	<p class="border-b-4 border-b-emerald-300 text-2xl">Binary:</p>
	<p id="binary-text" class="text-2xl">{binary}</p>

	<p class="mt-8 border-b-4 border-b-emerald-500 text-2xl">Hexadecimal:</p>
	<p id="binary-text" class="text-2xl">{hexa}</p>

	<p class="mt-8 border-b-4 border-b-emerald-900 text-2xl">Octal:</p>
	<p id="binary-text" class="text-2xl">{octal}</p>
</div>

<p class="mt-2 text-center text-[5px]">
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣠⣴⣶⣦⣤⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⣾⣿⣿⢿⡷⣧⠈⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣤⣾⣿⣿⣿⣿⣿⣿⣽⢷⣤⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⣠⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣽⣻⣦⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣾⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣳⢯⣷⡀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⢀⣾⠏⠙⢿⣿⣿⣿⣿⣿⣿⣿⡿⠛⠉⣿⣿⣯⢿⣞⣷⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⠀⠀⠀⠻⣿⣿⣿⡛⠋⠁⠀⠀⣰⣿⣿⣟⡿⣾⡽⡇⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⣿⣿⣷⣶⣾⣿⠿⢿⣿⣿⣦⣀⣠⣴⣿⣿⣿⢯⣟⣷⣻⣽⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⣀⣀⣀⣤⡴⣿⣿⣿⣿⣿⣿⠀⠈⣿⣿⣿⣿⣿⢿⣿⣻⣽⣻⣞⣷⣻⢾⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⢠⣾⣿⣿⣿⣿⣯⣟⣿⣿⣿⣿⣿⣿⡀⢀⣿⣿⣻⢾⣽⣻⣞⡷⣯⢷⣻⡾⣽⣻⠆⠀⠀⣀⠀⠀⠀⠀<br />
	⠀⠻⢿⣿⣿⣿⣷⣻⢾⣿⣿⣿⣿⣿⣷⣾⣿⣷⣟⡿⣞⡷⣯⢿⡽⣯⡷⣿⣽⣻⠀⠀⠈⢿⡇⠀⠀⠀<br />
	⠀⠀⠀⠉⠉⠛⠻⢽⣻⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣽⣯⣟⣷⣻⢷⣯⢿⡀⠀⠀⠀⠀⣶⡄⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠙⢿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣾⣯⣟⣾⣻⣇⠀⠀⠀⠀⣿⣽⡀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣞⣷⣻⢾⣳⣤⣤⡴⣟⣾⡇<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣿⣻⢿⣿⣿⣿⣿⡾⣽⢯⣷⣻⢾⣽⣻⢾⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⢸⣿⣿⣿⢿⣿⣿⣿⣿⣿⣿⣿⡷⣯⣟⡾⣿⣿⣿⣻⣽⣻⢾⣽⣻⢾⣽⠃⠀<br />
	⠀⠀⠀⠀⠀⠀⠀⠀⠀⣾⣿⣿⣯⣟⡾⣿⣿⣿⣿⣿⣿⣟⡷⣯⣟⣷⣻⣞⡷⣯⣟⡿⡾⠝⠛⠀⠀⠀<br />
	⠀⠀⡀⠀⠀⠀⠀⠀⣼⣿⣿⣿⣳⣯⢿⡽⣿⣿⣿⣿⣿⣯⣟⣷⣻⣞⡷⣯⣟⡷⣯⡟⠀⣠⡶⡿⠀⠀<br />
	⠀⠀⢿⣄⠀⠀⢀⣼⣿⣿⣿⣿⣳⣯⢿⣽⢯⣿⣿⣿⣟⡾⣽⣞⡷⣯⣟⡷⣯⣟⡷⡇⠀⠉⠉⠀⠀⠀<br />
	⠀⠀⠈⢿⣿⣾⣿⣿⣿⣿⣿⢷⣻⣞⡿⣞⣯⡷⣯⢷⣻⡽⠃⠉⠉⠑⠋⠿⠳⠯⠛⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠈⢻⣿⣿⣿⣿⣿⣟⣯⠷⠋⠉⠉⠓⠻⠽⠻⠃⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
	⠀⠀⠀⠀⠀⠈⠛⠿⣿⣟⠾⠉⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀<br />
</p>

<p class="absolute bottom-0 ml-1">Source Code: https://github.com/iJustGhost/ventulator</p>
