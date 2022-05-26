<template>
  <div id="whyCont" class="whyCont">
    <svg
      class="backgroundPath"
      xmlns="http://www.w3.org/2000/svg"
      width="1921.218"
      height="907.823"
      viewBox="0 0 1921.218 907.823"
    >
      <path
        d="M-229.894,51.316s218.919-30.789,369.73,145.737S362,648.631,611.727,784.1s450.81,2.052,656.756,110.842,421.622,28.737,421.622,28.737"
        transform="translate(230.243 -46.756)"
      />
    </svg>

    <h2>Why the 413 Doesn't Work</h2>
    <div class="reason">
      <h3 class="reasonHeading">Climate Change</h3>
      <p>
        It will add over 17 million tonnes of greenhouse gas emissions by 2050 - resulting in $1.4 billion in damages
        from pollution - when cutting emissions is more urgent than ever.
      </p>
    </div>

    <div class="reason">
      <h3 class="reasonHeading">Farmland & Biodiversity</h3>
      <p>
        Highway 413 would be 59 km long and would pave over 400 acres of the Greenbelt and over 2,000 acres of Class 1
        and Class 2 farmland - among Ontario's most productive farmland.
      </p>
    </div>

    <div class="reason">
      <h3 class="reasonHeading">Congestion Stays</h3>
      <p>
        Building new highways usually does nothing to relieve congestion over time. An expert panel study found Highway
        413 would only save drivers in the region <i>30-60 seconds</i> per trip
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.whyCont {
  position: relative;
  font-size: 1.5em;
  background: var(--secondary);
  min-height: 100vh;
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  flex-wrap: wrap;
  color: var(--light);

  h2 {
    font-size: 3em;
    text-align: center;
    width: 100%;
    text-decoration: underline solid 2px var(--highlight);
    font-family: var(--customFont);
    z-index: 5;
		margin: 10px 0px;
  }

  .reason {
    text-align: center;
    box-sizing: border-box;
    padding: 25px;
    width: 500px;
    max-width: 100%;
    z-index: 5;

    .reasonHeading {
      margin-bottom: 10px;
      font-size: 1.5em;
      font-weight: bold;
    }

    p {
      margin: 0;
      font-weight: 100;
    }
  }

  .backgroundPath {
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0.5;
    z-index: 0;

    path {
      fill: none;
      stroke: #0e3e4c;
      stroke-width: 5px;
      stroke-dasharray: 20;
      animation: path 10s linear infinite;
    }
  }

  @keyframes path {
    from {
      stroke-dashoffset: 100%;
    }

    to {
      stroke-dashoffset: 0%;
    }
  }
}
</style>
