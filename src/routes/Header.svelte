<script>
	import { page } from '$app/stores';
</script>

<header>
	<p class="header-title">N-profile-Generator</p>
	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">ホーム</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
			<li>
				<a href="https://nuixo.app/">Nuixo</a>
			</li>
		</ul>

	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		letter-spacing: 0.1em;
		padding: 0 2rem;
	}

	.header-title {
		font-weight: 700;
		font-size: 1rem;
		text-transform: uppercase;
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
		width: 60%;
		height: 0;
		position: absolute;
		bottom: 0;
		margin-inline: 20%;
		margin-bottom: 4px;
		border-bottom: 3px solid var(--color-theme-1);
		border-radius: 1.5px;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>
