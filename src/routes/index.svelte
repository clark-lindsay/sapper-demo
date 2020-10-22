<script>
  import fairolinaLogoFull from "../../static/FAIR1.jpg";
  import { onMount } from "svelte";

  onMount(() => {
    if (window.netlifyIdentity) {
      window.netlifyIdentity.on("init", (user) => {
        if (!user) {
          window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
          });
        }
      });
    }
  });
</script>

<style>
  figure,
  figure {
    margin: 1em;
  }

  img {
    width: 100%;
    max-width: 400px;
    margin: 1em;
  }
</style>

<svelte:head>
  <title>Fairolina Demo</title>
</svelte:head>

<figure><img alt="FAIROLINA" src={fairolinaLogoFull} /></figure>

<h1>Welcome to FAIRolina!</h1>
<p>
  We are an organization for students at the University of North Carolina at
  Chapel Hill who are concerned about the democratic institutions of our state
  and our nation. We believe that reform is required in order to ensure the
  fairness and and representative legitimacy of our political system, and that,
  in the absence of this reform, the integrity of our democratic institutions is
  decaying at a dangerous pace. We also believe that a lack of fairness in our
  election systems is at the root of much of the gridlock and partisan
  polarization we see in Raleigh and in Washington. When politicians do not feel
  accountable to voters, they are able to act without considering the needs or
  interests of their constituents. Gerrymandering, registration purges, lack of
  access to polling sites, voter ID laws, poorly defined oversight, corporate
  money in politics, the Electoral College, felon disenfranchisement, and
  foreign interference are just some of the ways the voices American voters are
  diminished or ignored. See our policy page for a specific collection of
  changes we support in order to modernize and improve our democracy!
</p>

