<script lang="ts">
  import { userData } from '$lib/firebase';
</script>

<svelte:head>
  <title>Thunderlink - a place for links</title>
  <meta
    name="description"
    content="You can use it for storing your all social links."
  />
</svelte:head>

<main class="flex w-full min-h-screen text-center">
  <div class="hero bg-base-200">
    <div class="w-full">
      <h1 class="text-7xl font-bold">Thunderlink</h1>
      <p class="py-6 text-2xl">
        One simple link to share your entire developer portfolio
      </p>

      {#if $userData?.username}
        <a class="btn btn-primary" href="/{$userData.username}/edit">
          Edit Profile
        </a>
      {:else}
        <a class="btn bg-primary" href="/login">Get Started</a>
        <a class="btn bg-secondary" href="/abduraimbek">Example Profile</a>
      {/if}
    </div>
  </div>
</main>
