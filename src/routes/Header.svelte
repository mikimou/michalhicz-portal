<script>
	import { page } from '$app/stores';
	import github from '$lib/images/github.svg';
	import { redirect } from '@sveltejs/kit';
	import { error } from '@sveltejs/kit';

	async function redirectt() {
		window.location.assign("/");
	}

</script>

<header>
	
	<!--<div class="corner">
		
	</div>-->

	<!-- <nav>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a class="drac-text" href="/">Domov</a>
			</li>
			<li aria-current={$page.url.pathname === '/obsah' ? 'page' : undefined}>
				<a class="drac-text" href="/">Obsah</a>
			</li>
		</ul>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
	</nav> -->

	<!--
	<div class="corner">
		<div>
			<div style="position: relative;margin-top: 1em;margin-left: -1em; width: 2.5em;">
				<select style="padding-right: 0.5em!important; padding-left: 0.5em!important;" class="drac-select drac-select-sm drac-select-white">
				  <option value="default" disabled={false} selected={true}>en</option>
				  <option>sk</option>
				</select>
			  </div>
	</div>-->

</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}

	.corner {
		width: 3em;
		height: 3em;
		display: inline-block;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	.white {
		filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(0deg) brightness(100%) contrast(100%);
	}

	nav {
		display: flex;
		justify-content: center;
		--background: var(--color-theme-1);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
		color: var(--color-theme-1);
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-bg);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-text);
	}
</style>
