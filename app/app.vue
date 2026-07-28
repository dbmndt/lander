<template>
  <div>
    <NuxtRouteAnnouncer />
    <NuxtPage/>
  </div>
  <Link
  rel="icon"
  href="/favicon.svg"
  type="image/svg"
/>
</template>

<style >
@import url('https://fonts.googleapis.com/css2?family=Figtree:wght@400;500;700&display=swap');

*, *::before, *::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --bg-dark: #1c2029;
  --purple-accent: rgba(92, 92, 153, 0.2);
  --card-bg: #2a303d;
  --card-border: #6c9468;
  --text-primary: #e1e8f5;
  --text-muted: rgba(225, 232, 245, 0.6);
  --font: 'Figtree', sans-serif;
}

body {
  background-color: var(--bg-dark);
  color: var(--text-primary);
  font-family: var(--font);
  min-height: 100vh;
}
</style>