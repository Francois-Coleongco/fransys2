<script>
	import "../app.css";

	// import golang from "@iconify-svelte/simple-icons/go";
	// import rust from "@iconify-svelte/simple-icons/rust";
	// import cpp from "@iconify-svelte/simple-icons/cplusplus";
	// import python from "@iconify-svelte/simple-icons/python";
	// import javascript from "@iconify-svelte/simple-icons/javascript";
	// import bash from "@iconify-svelte/simple-icons/gnubash";
	import Github from "@iconify-svelte/simple-icons/github";

	const projects = [
		{
			name: "Multithreaded Encrypted File Server/Client",
			description: "A terminal-based file storage server and client",
			link: "https://github.com/Francois-Coleongco/MEFSC",
		},
		{
			name: "HTTP Load Balancer",
			description: "A hybrid scheduling HTTP load balancer",
			link: "https://github.com/Francois-Coleongco/LoadBalancer",
		},
		{
			name: "Encrypted Steganography Suite",
			description: "A GUI tool to encode encrypted messages in PNG files",
			link: "https://github.com/Francois-Coleongco/Steganography_Suite",
		},
		{
			name: "Speech-Driven AI Video Preprocessor",
			description:
				"AI-powered video preprocessing for the lazy video editor",
			link: "https://github.com/Francois-Coleongco/KeepItRolling",
		},
		{
			name: "Distributed Threat Detection System",
			description: "A distributed threat detection framework",
			link: "https://github.com/Francois-Coleongco/SATD",
		},
		{
			name: "Network Encryption Interface",
			description: "C++ systems programming & encryption interface",
			link: "https://github.com/Francois-Coleongco/Network-Encryption-Interface",
		},
	];
</script>

<div class="flex flex-col min-h-screen flicker-in text-white">
	<nav
		class="opacity-75 border-b border-white px-6 py-3 flex justify-between items-center"
		style="position: relative; z-index: 1;"
	>
		<a
			href="#"
			class="font-mono text-xl tracking-widest flicker-in transform transition-transform duration-200 hover:scale-104"
		>
			Francois Coleongco
		</a>

		<div class="hidden md:flex space-x-6 font-mono">
			<a
				href="#projects"
				class="hover:text-white transform transition-transform duration-200 hover:scale-104"
				>Projects</a
			>
			<a
				href="#contact"
				class="hover:text-white transform transition-transform duration-200 hover:scale-104"
				>Contact</a
			>
		</div>

		<div class="md:hidden flex flex-col gap-4 mt-2">
			<a
				href="#projects"
				class="flicker-in transition transform transition-transform duration-200 hover:scale-104"
				>Projects</a
			>
			<a
				href="#contact"
				class="flicker-in transition transform transition-transform duration-200 hover:scale-104"
				>Contact</a
			>
		</div>

		<div class="md:hidden">
			<button id="menu-btn">
				<svg
					class="w-6 h-6"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					viewBox="0 0 24 24"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M4 6h16M4 12h16M4 18h16"
					></path>
				</svg>
			</button>
		</div>
	</nav>

	<main class="flex-grow p-6">
		<h2 class="text-center pipboy-flicker text-4xl mt-4 mb-4">
			Hi, I'm Francois
		</h2>

		<section id="about">
			<div class="max-w-xl mx-auto text-center mt-4 pt-16 pb-12 -mt-24">
				<p
					class="text-md font-mono leading-relaxed"
					style="position: relative; z-index: 1;"
				>
					I'm an honors CS major at the <a
						href="https://www.ualberta.ca/en/index.html"
						class="underline">University of Alberta</a
					>, interested in high-performance systems, cybersecurity,
					and AI-driven solutions.
				</p>
			</div>
		</section>

		<br />

		<section
			id="projects"
			class="min-h-screen flex flex-col justify-center items-center text-center px-4 py-16 md:py-24"
		>
			<h2
				class="pipboy-flicker text-4xl mb-4 pb-8"
				style="position: relative; z-index: 1;"
			>
				Projects
			</h2>
			<section class="bg-panelBg/80 p-6">
				<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
					{#each projects as project (project.name)}
						<div
							class="backdrop-blur-sm opacity-75 w-full md:w-auto project-panel rounded-md shadow-lg p-4 flex flex-col justify-between hover:shadow-[0_0_15px_rgba(255,255,255,0.3)] transition-shadow border transform transition-transform duration-200 hover:scale-101 text-white"
						>
							<a
								href={project.link}
								target="_blank"
								class="block"
							>
								<h3 class="text-xl font-mono mb-2 leading-snug">
									{project.name}
								</h3>
								<p class="text-sm leading-relaxed mb-2">
									{project.description}
								</p>
							</a>
							<Github
								height="24"
								class="animate-pulse text-gray-400 hover:text-white transition-all duration-1000 drop-shadow-[0_0_5px_rgba(255,255,255,0.6)] hover:drop-shadow-[0_0_10px_rgba(255,255,255,0.9)] cursor-pointer"
							/>
						</div>
					{/each}
				</div>
			</section>
		</section>
	</main>

	<section
		id="contact"
		class="min-h-screen flex flex-col justify-center items-center text-center px-4 py-16 md:py-24"
	>
		<h2
			class="pipboy-flicker text-4xl mb-4 pb-8"
			style="position: relative; z-index: 1;"
		>
			CONTACT
		</h2>
		<p class="mb-6 pb-4" style="position: relative; z-index: 1;">
			Want to get in touch? Shoot me an email or connect on GitHub.
		</p>
		<div class="flex flex-col md:flex-row gap-4">
			<a
				href="mailto:francois.coleongco@gmail.com"
				class="backdrop-blur-sm project-panel p-4 border border-white rounded-lg hover:text-white flicker-in transition text-center transform transition-transform duration-200 hover:scale-104"
				style="position: relative; z-index: 1;"
			>
				Email Me
			</a>
			<a
				href="https://linkedin.com/in/francois-coleongco"
				target="_blank"
				rel="noopener noreferrer"
				class="backdrop-blur-sm project-panel p-4 border border-white rounded-lg hover:text-white flicker-in transition text-center transform transition-transform duration-200 hover:scale-104"
				style="position: relative; z-index: 1;"
			>
				LinkedIn
			</a>
		</div>
	</section>

	<p class="text-center" style="position: relative; z-index: 1;">
		(you == void *) == true
	</p>
	<br />

	<footer
		class="bg-panelBg/90 scanline border-t-2 border-white py-6 px-6 flex flex-col md:flex-row justify-between items-center text-sm mt-0"
	>
		<div
			class="mb-4 md:mb-0 font-mono"
			style="position: relative; z-index: 1;"
		>
			© 2025 Francois Coleongco
		</div>
		<div class="flex gap-6">
			<a
				href="https://github.com/Francois-Coleongco"
				target="_blank"
				class="flex items-center gap-1 hover:text-white transform transition-transform duration-200 hover:scale-104"
				style="position: relative; z-index: 1;"
			>
				GitHub
			</a>
			<a
				href="https://www.linkedin.com/in/francois-coleongco"
				target="_blank"
				class="flex items-center gap-1 hover:text-white transform transition-transform duration-200 hover:scale-104"
				style="position: relative; z-index: 1;"
			>
				LinkedIn
			</a>
			<a
				href="mailto:francois.coleongco@gmail.com"
				class="flex items-center gap-1 hover:text-white transform transition-transform duration-200 hover:scale-104"
				style="position: relative; z-index: 1;"
			>
				Email
			</a>
		</div>
	</footer>
</div>
