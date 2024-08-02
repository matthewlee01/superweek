<script>
  import "../app.css";
  import "@fontsource/itim";
  import "@fontsource/inter/300.css";
  import "@fontsource/inter/500.css";
  import logo from "$lib/images/logo.png";
  import footer from "$lib/images/footer.png";
  import { fade } from "svelte/transition";
  import { fly } from "svelte/transition";
  import { page } from "$app/stores";
  import { afterNavigate } from "$app/navigation";
  let showMenu = false;

  afterNavigate(() => {
    showMenu = false;
  });
</script>

<div class="main">
  <div class="menubar" class:opaque={showMenu}>
    <a href="/">
      <img src={logo} alt="super week logo" width="100" />
    </a>
    <button class="display" on:click={() => (showMenu = !showMenu)}
      >{showMenu ? "close" : "menu"}</button
    >
  </div>
  {#if showMenu}
    <div class="menu-content display" transition:fade={{ duration: 100 }}>
      <a
        transition:fly={{
          duration: 300,
          x: 16,
        }}
        href="/field-trips"
        class="display">field trips</a
      >
      <a
        transition:fly={{
          duration: 300,
          x: -16,
        }}
        href="/workshops"
        class="display">workshops</a
      >
      <a
        transition:fly={{
          duration: 300,
          x: 16,
        }}
        href="/sessions"
        class="display">sessions</a
      >
      <a
        transition:fly={{
          duration: 300,
          x: -16,
        }}
        href="/faq"
        class="display">faq</a
      >
      <a
        transition:fly={{
          duration: 300,
          x: -20,
        }}
        href="/schedule"
        class="display">schedule</a
      >
    </div>
  {/if}
  <div class="content">
    <slot />
  </div>
  {#if $page.url.pathname !== "/"}
    <div class="footer">
      <div class="img-wrapper">
        <img src={footer} alt="super week logo" />
      </div>
      <div class="contact">
        <p>
          for any questions or concerns, email
          <a
            href="mailto:&#x6f;&#x66;&#x66;&#x69;&#x63;&#x65;&#x40;&#x6c;&#x68;&#x66;&#x2e;&#x63;&#x61;"
            ><span>office@l</span><span hidden>SPAM EMAIL BLOCK</span><span
              >hf.ca</span
            ></a
          >
        </p>
        <p>with "SUPER WEEK" in the subject line.</p>
      </div>
    </div>
  {/if}
</div>

<style>
  :global(body) {
    margin: 0;
    background-color: var(--white);
  }

  :global(*) {
    box-sizing: border-box;
    --red: rgb(212, 0, 0);
    --blue: rgb(50, 126, 140);
    --yellow: rgb(250, 202, 1);
    --white: rgb(255, 255, 240);
    font-family: "Inter", sans-serif;
    font-weight: 300;
    color: var(--blue);
  }

  :global(h1, h2, h3, h4, h5, h6) {
    font-family: "Itim", sans-serif;
    color: var(--red);
    font-weight: 500;
    padding-top: 0.5rem;
    line-height: 1;
    margin: 0.5rem 0;
  }

  :global(h1) {
    font-size: 3rem;
  }

  :global(h5) {
    font-size: 1.25rem;
    color: var(--yellow);
    margin-top: -0.75rem;
  }

  :global(h3) {
    font-size: 1.5rem;
  }

  :global(p) {
    margin: 0rem 1rem 0.5rem 1rem;
  }

  :global(a) {
    text-decoration: underline;
    text-decoration-style: dotted;
    text-decoration-color: var(--yellow);
  }

  :global(*::-webkit-scrollbar) {
    background-color: transparent;
  }

  :global(*::-webkit-scrollbar-thumb) {
    background-color: var(--yellow);
    border-radius: 1rem;
    border: 3px solid var(--white);
  }

  :global(*::-webkit-scrollbar) {
    width: 0.75rem;
  }

  .main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 1rem;
    padding-top: 0.25rem;
    min-height: 100vh;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .content {
    max-width: 880px;
    margin-top: 4rem;
    padding-bottom: 2rem;
  }

  .display {
    font-family: "Itim", sans-serif;
  }

  .menubar {
    display: flex;
    justify-content: space-between;
    height: 4rem;
    align-items: center;
    width: 100%;
    padding: 0.5rem 0rem;
    z-index: 20;
    color: var(--blue);
    font-size: 1.5rem;
    position: fixed;
    top: 0;
    padding: 0.5rem 1rem;
    background-color: rgba(255, 255, 240, 0.4);
    backdrop-filter: blur(4px);
    transition: background-color 0.1s;
  }

  .menubar.opaque {
    background-color: rgba(255, 255, 240, 1);
  }

  .menubar a {
    height: min-content;
    padding-bottom: 0.5rem;
  }

  .menu-content a:nth-child(1) {
    margin-left: 2.5rem;
    rotate: 8deg;
  }

  .menu-content a:nth-child(2) {
    margin-right: 3rem;
    rotate: -4deg;
  }

  .menu-content a:nth-child(3) {
    margin-left: 3.5rem;
    rotate: -10deg;
  }

  .menu-content a:nth-child(4) {
    margin-left: 2.5rem;
    rotate: -4deg;
  }

  .menu-content a:nth-child(5) {
    margin-top: -0.25rem;
    margin-right: 0.5rem;
    rotate: 4deg;
  }

  .menu-content {
    display: flex;
    position: fixed;
    top: 4rem;
    left: 0;
    width: 100%;
    height: 100%;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    padding-bottom: 4rem;
    padding-top: 2rem;
    font-size: 2rem;
    z-index: 10;
    background-color: var(--white);
    color: var(--blue);
  }

  .footer {
    display: flex;
    width: 100%;
    justify-content: space-between;
    height: min-content;
  }

  .img-wrapper {
    display: flex;
    align-items: stretch;
    max-width: 45%;
    max-height: 5rem;
  }

  .img-wrapper img {
    height: 100%;
  }
  .contact {
    text-align: right;
    font-size: 0.8rem;
    max-width: 50%;
    letter-spacing: -0.5px;
  }

  .contact p {
    margin: 0.125rem;
  }
</style>
