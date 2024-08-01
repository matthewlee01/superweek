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
      <span>exposure</span>
      <span>equipping</span>
      <span>education</span>
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
    height: calc(100vh - 10rem);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: stretch;
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
    gap: 1rem;
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

  .between.es span {
    font-size: 1.5rem;
    color: var(--red);
    margin-bottom: -0.125rem;
  }

  .between.dates span {
    font-size: 2rem;
    font-family: "Itim", sans-serif;
    color: var(--yellow);
  }

  .roster span {
    margin-top: 0.5rem;
    font-size: 1rem;
    letter-spacing: normal;
  }
</style>
