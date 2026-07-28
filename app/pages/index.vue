<template>
	<main class="homepage">
		<section class="hero">
			<div class="hero-content">
				<h1 class="hero-title">dbmndt</h1>
				<p class="hero-subtitle">creative collective</p>
			</div>
			<!-- Member Cards -->
			<div class="cards-grid">
				<article class="member-card">
					<div class="avatar-wrapper">
						<img src="/shawn.png" alt="Shawn"
							class="avatar" />
					</div>
					<h2 class="member-name">Shawn</h2>
					<p class="member-roles">Design, Code, Live Event Production</p>
					<a href="shawn.dbmndt.com" class="member-link">Visit Site →</a>
					<a href="mailto:shawn@dbmndt.com" class="member-email">
						<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none"
							stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
							<rect width="20" height="16" x="2" y="4" rx="2" />
							<path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7" />
						</svg>
						Email
					</a>
				</article>
			</div>
		</section>
	</main>
</template>

<script>
const members = [
    {
        name: 'Shawn',
        roles: 'Design, Code, Live Event Production',
        avatar: 'https://www.figma.com/api/mcp/asset/638d1f56-82d7-457e-925c-de05e304358d',
        website: 'shawn.dbmndt.com',
        email: 'shawn@dbmndt.com'
    }
]
</script>

<style></style>

<style scoped>
.homepage {
	min-height: 100vh;
	display: flex;
	flex-direction: column;
	position: relative;
	background: linear-gradient(0deg, var(--purple-accent) 0%, transparent 100%), #1A202B;
}

/* Hero */
.hero {
	flex: 1;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	gap: 64px;
	padding: 100px 40px;
	position: relative;
	z-index: 1;
}

.hero-content {
	display: flex;
	flex-direction: column;
	align-items: center;
	gap: 16px;
	text-align: center;
}

.hero-title {
	font-size: clamp(5rem, 8vw, 6rem);
	font-weight: 700;
	line-height: 1.1;
	color: #fff;
	letter-spacing: -0.02em;
	animation: fadeSlideDown 0.8s cubic-bezier(0.16, 1, 0.3, 1) both;
}

.hero-subtitle {
	font-size: clamp(2rem, 3vw, 2.5rem);
	font-weight: 500;
	color: #fff;
	line-height: 1.25;
	animation: fadeSlideDown 0.8s 0.1s cubic-bezier(0.16, 1, 0.3, 1) both;
}

/* Cards Grid */
.cards-grid {
	display: flex;
	flex-wrap: wrap;
	gap: 24px;
	justify-content: center;
	animation: fadeSlideDown 0.9s 0.2s cubic-bezier(0.16, 1, 0.3, 1) both;
}

.member-card {
	background: var(--card-bg);
	border: 4px solid var(--card-border);
	border-radius: 20px;
	width: 240px;
	min-height: 320px;
	padding: 40px 24px;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	gap: 10px;
	overflow: hidden;
	transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
	cursor: default;
}

.member-card:hover {
	transform: translateY(-4px);
	box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4), 0 0 0 1px rgba(108, 148, 104, 0.4);
}

/* Avatar */
.avatar-wrapper {
	width: 80px;
	height: 80px;
	border-radius: 50%;
	overflow: hidden;
	flex-shrink: 0;
}

.avatar {
	width: 100%;
	height: 100%;
	object-fit: cover;
	display: block;
}

.placeholder-avatar {
	background: rgba(255, 255, 255, 0.08);
	display: flex;
	align-items: center;
	justify-content: center;
	font-size: 28px;
	color: rgba(255, 255, 255, 0.3);
	font-weight: 700;
}

/* Member Info */
.member-name {
	font-size: 2rem;
	font-weight: 700;
	color: var(--text-primary);
	line-height: 1.25;
	text-align: center;
}

.member-roles {
	font-size: 1rem;
	font-weight: 500;
	color: var(--text-primary);
	text-align: center;
	line-height: 1.25;
	white-space: pre-wrap;
}

.member-link {
	font-size: 1rem;
	font-weight: 700;
	color: var(--text-primary);
	text-decoration: underline;
	text-decoration-skip-ink: none;
	transition: opacity 0.2s;
	margin-top: 2px;
}

.member-link:hover {
	opacity: 0.75;
}

.member-email {
	display: flex;
	align-items: center;
	gap: 4px;
	font-size: 16px;
	font-weight: 700;
	color: var(--text-primary);
	text-decoration: underline;
	text-decoration-skip-ink: none;
	transition: opacity 0.2s;
}

.member-email:hover {
	opacity: 0.75;
}

/* Footer */
.footer {
	position: relative;
	z-index: 1;
	text-align: center;
	padding: 24px 40px;
	font-size: 14px;
	color: var(--text-muted);
	font-weight: 500;
	border-top: 1px solid rgba(255, 255, 255, 0.06);
}

/* Animations */
@keyframes fadeSlideDown {
	from {
		opacity: 0;
		transform: translateY(-20px);
	}

	to {
		opacity: 1;
		transform: translateY(0);
	}
}

@keyframes fadeUp {
	from {
		opacity: 0;
		transform: translateY(30px);
	}

	to {
		opacity: 1;
		transform: translateY(0);
	}
}

/* Responsive */
@media (max-width: 600px) {
	.hero {
		padding: 60px 20px;
		gap: 48px;
	}

	.member-card {
		width: 100%;
		max-width: 300px;
		min-height: auto;
	}
}
</style>
