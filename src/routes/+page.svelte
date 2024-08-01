<script>
  import title from "$lib/images/title.png";
</script>

<div class="full">
  <div class="wrapper">
    <img src={title} alt="super week title" class="title" />
  </div>
  <div>
    <div class="between">
      <span>vancouver</span>
      <span>bc</span>
    </div>
    <div class="between es">
      <a href="/field-trips">exposure</a>
      <a href="/sessions">equipping</a>
      <a href="/workshops">education</a>
    </div>
    <div class="between dates">
      <span>2024</span>
      <span>august 11-14</span>
    </div>
    <div class="between roster">
      <span>living hope fellowship</span>
      <span>city on a hill</span>
    </div>
    <div class="between roster">
      <span>bridgeway church</span>
      <span>vaughan community church</span>
    </div>
  </div>
</div>

<style>
  .full {
    padding: 1rem 2rem 0rem 2rem;
    height: calc(100vh - 11rem);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: stretch;
    max-width: 100vw;
  }

  .wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
  }

  .title {
    width: 100%;
    height: auto;
    max-height: 70vh;
  }

  .between {
    display: flex;
    justify-content: space-between;
    gap: 0.25rem;
    margin-bottom: -1rem;
    letter-spacing: 2px;
  }

  .between.es {
    margin-bottom: -0.75rem;
  }

  .between span {
    font-family: "Itim", sans-serif;
    font-size: 3rem;
  }

  .between.es a {
    font-size: 1rem;
    color: var(--red);
		font-family: "Itim", sans-serif;
		letter-spacing: normal;
  }

  .between.dates span {
    font-size: 2rem;
    font-family: "Itim", sans-serif;
    color: var(--yellow);
  }

  .roster span {
    margin-top: 0.5rem;
    font-size: 0.875rem;
    letter-spacing: normal;
  }

  @media (max-width: 600px) {
    .full {
      padding: 1rem 0rem 0rem 0rem;
    }
  }
</style>
