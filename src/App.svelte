<script>
  import LeftAlignedExample from "./sections/LeftAlignedExample.svelte";
  import RightAlignedExample from "./sections/RightAlignedExample.svelte";
  import ImageExample from "./sections/ImageExample.svelte";
  import TitleSection from "./sections/TitleSection.svelte";
  import InteresectionObserverBasicExample from "./sections/InteresectionObserverBasicExample.svelte";
  import IntersectionObserverAlertExample from "./sections/IntersectionObserverAlertExample.svelte";
  import DisappearingDuckExample from "./sections/DisappearingDuckExample.svelte";
  import IntersectionObserverSectionCard from "./sections/IntersectionObserverSectionCard.svelte";
  import IntersectionObserverListExample from "./sections/IntersectionObserverListExample.svelte";
</script>

<main>
  <TitleSection />
  <RightAlignedExample />

  <div class="dividerText">
    <h1>Let's look at the data...</h1>
  </div>

  <LeftAlignedExample />
  <!--<ImageExample />

  <IntersectionObserverSectionCard />
  <InteresectionObserverBasicExample />
  <IntersectionObserverAlertExample />
  <DisappearingDuckExample />
  <IntersectionObserverListExample />-->

  <div class="takeaways">
    <h1>Key Takeaways</h1>

    <br>

    <div class="keyTakeaways">
      <div class="takeawayCard">
        <h1>1</h1>
        <p>Female representation in STEM jobs in the US greatly varies by race. Some racial groups have much 
           bigger gaps in employment between men and women.</p>
      </div>

      <div class="takeawayCard">
        <h1>2</h1>
        <p>
          The number of women in the US who hold STEM degrees and are employed in STEM jobs seems to fluctuate
          not only  among racial groups but also over time.
        </p>
      </div>

      <div class="takeawayCard">
        <h1>3</h1>
        <p>
          Even though there's been an <a href="https://public.tableau.com/app/profile/harsha.mallajosyula5209/viz/shared/DT3RWD9PZ" 
          target="_blank">increase in women attaining STEM degrees</a>, women are still struggling to get employment
          in STEM fields in the US.
        </p>
      </div>
    </div>
  </div>

  <br>

  <div class="resources">
    <h1>Resources to Learn More</h1>

    <br>

    <div class="resourceList">
      <div class="resource">
        <h2>✦</h2>
        <p>The <a href="https://blackwealthdata.org" target="_blank">Black Wealth Data Center</a>, 
          a racial wealth equity database providing insights and visuals at the local and national 
          level about education, employment, and more in terms of wealth in the US.</p>
      </div>

      <div class="resource">
        <h2>✦</h2>
        <p>Digest tables from the <a href="https://nces.ed.gov/programs/digest/current_tables.asp" 
          target="_blank">National Center for Education Statistics</a>, with reports on elementary, 
          secondary, and postsecondary schooling in the US. There's also data on federal
          education funding and education outcomes to explore.</p>
      </div>
    </div>
  </div>
</main>

<style>
  h1 {
    font-family: "Winky Rough", sans-serif;
    color: #ffc0ad;
    margin: 0px;
    font-size: 45px;
    text-align: center;
  }

  p {
    font-family: "Manrope", sans-serif;
    font-weight: 500;
    font-size: 20px;
    color: #fffffe;
  }

  .takeaways, .resources {
    height: 100vh;
    display: table-cell;
    vertical-align: middle;
  }

  .keyTakeaways {
    margin-right: 3%;
    margin-left: 3%;
    width: 90%;
    height: auto;
    display: inline-flex;
    padding: 20px;
    justify-content: center;
    margin-top: -1px;
    align-items: center;
  }

  .takeawayCard {
    width: 25%;
    height: auto;
    margin: 30px;
    padding: 20px;
    text-align: center;
    object-fit: cover;
    align-items: center;
    flex-wrap: wrap;
    background-color: #271c19;
    border-radius: 5px;
    box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;
  }

  .takeawayCard h1 {
    font-size: 90px;
  }

  .resourceList {
    background-color: #271c19;
    border-radius: 5px;
    box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;
    width: 75%;
    margin-right: auto;
    margin-left: auto;
    display: block;
    padding: 20px;
    margin-top: 20px;
  }

  .resource {
    display: flex;
    align-items: center;
  }

  .resource h2 {
    margin: 0px 30px;
    font-family: "Winky Rough", sans-serif;
    color: #ffc0ad;
    font-size: 45px;
  }

  .resource a, .takeawayCard a {
    color: #e78fb3;
  }

  .resource a:hover, .takeawayCard a:hover {
    color: #ffc0ad;
  }

  .dividerText {
    height: 85vh;
  }

  .dividerText h1 {
    background-color: #271c19;
    border-radius: 5px;
    box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;
    width: 75%;
    margin-right: auto;
    margin-left: auto;
    display: block;
    padding: 20px;
    margin-top: 20px;
  }
</style>
