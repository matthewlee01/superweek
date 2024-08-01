<script>
  import { ExternalLink } from "lucide-svelte";
</script>

<div>
  <h1>exposure</h1>
  <h5>(field trips)</h5>
  <p>
    the internet and social media influence us towards our confirmation biases
    and our filter bubbles.
  </p>
  <p>
    to help go beyond that, and gain a bigger perspective of God, we will be
    going on day trips to various ministries in the greater vancouver area to
    see what God is doing outside of our normal bubbles.
  </p>
  <h3>ministry info</h3>
  <div class="ministries">
    <a href="https://promisevancouver.ca/" class="ministry" target="_blank"
      >promise vancouver
      <ExternalLink size="16" />
    </a>
    <a href="https://ugm.ca/" class="ministry" target="_blank"
      >union gospel mission
      <ExternalLink size="16" />
    </a>
    <a href="https://nightshiftministries.org/" class="ministry" target="_blank"
      >nightshift
      <ExternalLink size="16" />
    </a>
    <a href="https://journeyhomecommunity.ca/" class="ministry" target="_blank"
      >journey home community
      <ExternalLink size="16" />
    </a>
    <a
      href="https://soundofthelordmission.com/"
      class="ministry"
      target="_blank"
      >sound of the Lord mission
      <ExternalLink size="16" />
    </a>
  </div>
  <h3>details</h3>
  <p class="q">what are "exposure trips"?</p>
  <p>
    each group will visit various ministries in the greater vancouver area to
    see what God is doing outside of our normal bubbles.
  </p>
  <p class="q">how will we get there?</p>
  <p>by transit. if you do not have a transit pass, we will buy one for you.</p>
  <p class="q">when are we going?</p>
  <p>
    the B+Y will be visiting on 8/12 (mon). the HS will be visiting on 8/13
    (tue). participants will be split up in groups of 7-10.
  </p>
</div>

<style>
  .ministries {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-top: 0.25rem;
  }

  .ministry {
    margin: 0.25rem 1rem;
    padding: 0.25rem 0.5rem;
    border: 2px solid var(--yellow);
    border-radius: 0.5rem;
    width: fit-content;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .q {
    font-weight: 500;
    margin-bottom: 0rem;
  }
</style>
