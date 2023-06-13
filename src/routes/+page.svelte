<script>
	import Counter from './Counter.svelte';
	import logo from '$lib/images/airisp.png';
	import { redirect } from '@sveltejs/kit';

	async function kasm() {
		window.location.assign("https://kasm.michalhicz.eu/");
	}
	async function railway() {
		window.location.assign("https://railway.michalhicz.eu/");
	}
	async function host() {
		window.location.assign("https://host.michalhicz.eu/");
	}
	async function hosting() {
		window.location.assign("https://hosting.michalhicz.eu/");
	}
	async function ebooks() {
		window.location.assign("https://ebooks.michalhicz.eu/");
	}
	async function lyrics() {
		window.location.assign("https://lyrics.michalhicz.eu/");
	}
	async function mc() {
		window.location.assign("https://mc.michalhicz.eu/");
	}
	async function api() {
		window.location.assign("https://api.michalhicz.eu/");
	}
	async function cloud() {
		window.location.assign("https://cloud.michalhicz.eu/");
	}
	async function proxy() {
		window.location.assign("https://proxy.michalhicz.eu/");
	}
	async function proxy2() {
		window.location.assign("https://proxy2.michalhicz.eu/");
	}
	async function portainer() {
		window.location.assign("https://portainer.michalhicz.eu/");
	}
	async function portainer2() {
		window.location.assign("https://portainer2.michalhicz.eu/");
	}

	let current = "publicc";

</script>

<svelte:head>
	<title>Michal Hicz App Portal</title>
	<meta name="description" content="Sieťové vzdelanie" />
</svelte:head>

<section>
	
	<div class="welcome">
		<!-- <picture>
			<img src={logo} alt="" />
		</picture> -->
		<h2 class="drac-heading drac-text-bold drac-heading-2xl drac-text-yellow-pink">App portal</h2>
	</div>

	<div style="height: 6em"></div>
	<div class="drac-box">
		<ul class="drac-tabs drac-tabs-red">
		  <li class="{current === 'publicc' ? 'drac-tab drac-tab-active' : 'drac-tab'}">
			<a class="drac-tab-link drac-text" on:click={() => current = 'publicc'} >Public Apps</a>
		  </li>
		  <li class="{current === 'private' ? 'drac-tab drac-tab-active' : 'drac-tab'}">
			<a class="drac-tab-link drac-text" on:click={() => current = 'private'} >Private Apps</a>
		  </li>
		  <li class="{current === 'admin' ? 'drac-tab drac-tab-active' : 'drac-tab'}">
			<a class="drac-tab-link drac-text" on:click={() => current = 'admin'} >Admin Apps</a>
		  </li>
		</ul>
	</div>
	<div style="height: 2em"></div>
	<div class="buttons">
		<center>
	{#if current == "publicc"}
	<div style="white-space: nowrap;">
		<button on:click={cloud} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Cloud</button>
		<button on:click={mc} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">MC portal</button>
		<button on:click={hosting} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Hosting</button>
	</div>
	<div style="white-space: nowrap;">

	</div>
	{:else if current == "private"}
	<div style="white-space: nowrap;">
		<button on:click={api} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">n8n API</button>
		<button on:click={lyrics} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Lyrics A.I.</button>
		<button on:click={ebooks} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Ebooks</button>
	</div>
	<div style="white-space: nowrap;">
		<button on:click={host} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Host (ptero)</button>
		<button on:click={railway} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Railway Cloud</button>
		<button on:click={kasm} class="drac-btn drac-bg-yellow-pink drac-m-sm drac-btn-lg">Kasm</button>
	</div>
	{:else if current == "admin"}
	<div style="white-space: nowrap;">
		<button on:click={proxy} class="drac-btn drac-bg-red-transparent drac-btn-ghost drac-text-red drac-m-sm drac-btn-lg">Proxy</button>
		<button on:click={proxy2} class="drac-btn drac-bg-red-transparent drac-btn-ghost drac-text-red drac-m-sm drac-btn-lg">Proxy2</button>
		<button on:click={portainer} class="drac-btn drac-bg-red-transparent drac-btn-ghost drac-text-red drac-m-sm drac-btn-lg">Portainer</button>
	</div>
	<div style="white-space: nowrap;">
		<button on:click={portainer2} class="drac-btn drac-bg-red-transparent drac-btn-ghost drac-text-red drac-m-sm drac-btn-lg">Portainer2</button>
	</div>
	{/if}
</center>
	</div>
</section>

<style>
	.buttons {
		height: 8em;
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
		font-size: 4rem;
	}

	@media only screen and (max-width: 450px) {
		h1 {
			font-size: 3.5rem;
		}
	}

	.welcome {
		display: block;
		position: relative;
		padding: 0 0 0 0;
		align-items: center;
	}

	.welcome img {
		height: 8em;
		margin: auto;
		display: block;
		pointer-events: none;
	
	}
	a { text-decoration: none; }
</style>
