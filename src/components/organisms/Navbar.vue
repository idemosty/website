<template>
	<nav
		id="header"
		class="fixed top-0 z-30 w-full text-white"
		:class="[scrollPosition > 10 ? 'bg-white shadow' : '']"
	>
		<div
			class="container flex flex-wrap items-center justify-between p-2 mx-auto"
		>
			<div class="flex items-center">
				<a
					class="text-2xl font-bold lg:text-4xl"
					:class="[scrollPosition > 10 ? 'text-gray-900' : 'text-white']"
					href="#"
				>
					<!--Icon from: http://www.potlabicons.com/ -->
					<svg
						class="inline h-8 fill-current"
						xmlns="http://www.w3.org/2000/svg"
						viewBox="0 0 512.005 512.005"
					>
						<rect
							:fill="[
								scrollPosition > 10 ? 'text-gray-900' : 'text-white',
							]"
							x="16.539"
							y="425.626"
							width="479.767"
							height="50.502"
							transform="matrix(1,0,0,1,0,0)"
						/>
						<path
							class="plane-take-off"
							d=" M 510.7 189.151 C 505.271 168.95 484.565 156.956 464.365 162.385 L 330.156 198.367 L 155.924 35.878 L 107.19 49.008 L 211.729 230.183 L 86.232 263.767 L 36.614 224.754 L 0 234.603 L 45.957 314.27 L 65.274 347.727 L 105.802 336.869 L 240.011 300.886 L 349.726 271.469 L 483.935 235.486 C 504.134 230.057 516.129 209.352 510.7 189.151 Z "
						/>
					</svg>
					Idemosty
				</a>
			</div>
			<div class="block lg:hidden">
				<button
					id="nav-toggle"
					class="flex items-center p-1 text-pink-800 transition duration-300 ease-in-out transform hover:text-gray-900 focus:outline-none focus:shadow-outline hover:scale-105"
					@click="toggleHeader()"
				>
					<svg
						class="w-6 h-6 fill-current"
						viewBox="0 0 20 20"
						xmlns="http://www.w3.org/2000/svg"
					>
						<title>Menu</title>
						<path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
					</svg>
				</button>
			</div>
			<div
				id="nav-content"
				class="z-20 flex-grow w-full p-4 mt-2 lg:flex lg:items-center lg:w-auto lg:mt-0 lg:bg-transparent lg:p-0"
				:class="[
					scrollPosition > 10
						? 'text-white bg-white'
						: 'bg-gray-100 text-gray-900',
					{ block: open, hidden: !open },
				]"
			>
				<ul class="items-center justify-end flex-1 list-reset lg:flex">
					<li class="mr-3">
						<a
							class="inline-block px-4 py-2 font-bold text-gray-900 hover:underline"
							href="#"
							>Active</a
						>
					</li>
					<li class="mr-3">
						<a
							class="inline-block px-4 py-2 text-gray-900 hover:text-gray-600 hover:underline"
							href="#"
							>link</a
						>
					</li>
					<li class="mr-3">
						<a
							class="inline-block px-4 py-2 text-gray-900 hover:text-gray-600 hover:underline"
							href="#"
							>link</a
						>
					</li>
				</ul>
				<button
					id="navAction"
					class="px-8 py-4 mx-auto mt-4 font-bold transition transform rounded-full shadow opacity-75 lg:mx-0 lg:mt-0 hover:underline focus:outline-none focus:shadow-outline hover:scale-105"
					:class="[
						scrollPosition > 10
							? 'gradient text-white'
							: 'bg-white text-gray-900',
					]"
				>
					Action
				</button>
			</div>
		</div>
		<hr
			class="border-b border-gray-100 opacity-25"
			:class="{ block: !open, hidden: open }"
		/>
	</nav>
</template>

<script>
export default {
	components: {},
	props: {},
	data() {
		return {
			scrollPosition: null,
			open: false,
		};
	},
	mounted() {
		window.addEventListener('scroll', this.updateScroll);
	},
	unmounted() {
		window.removeEventListener('scroll', this.updateScroll);
	},
	methods: {
		updateScroll() {
			this.scrollPosition = window.scrollY;
		},
		toggleHeader() {
			this.$data.open = !this.$data.open;
		},
	},
};
</script>
