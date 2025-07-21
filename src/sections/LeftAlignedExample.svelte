<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
  import ImageExample from "./ImageExample.svelte";

    const series = [
        {
            name: "Group 1",
            data: [
                [1990, 3],
                [2000, 4],
                [2010, 1],
                [2020, 1],
            ],
            color: "#8427c9",
        },
        {
            name: "Group 2",
            data: [
                [1990, 2],
                [2000, 5],
                [2010, -2],
                [2020, 2],
            ],
            color: "#ff99fc",
        },
        {
            name: "Group 3",
            data: [
                [1990, 4],
                [2000, 3],
                [2010, 0],
                [2020, 3],
            ],
            color: "#4096fa",
        },
    ];

    let chart;
    let thirdSeriesVisible = false;

    let options = {
        chart: {
            type: "spline",
            backgroundColor: "#e3ff00",
            borderColor: "#007052",
            borderWidth: 5,
            borderRadius: 20,
        },
        title: {
            text: "Another Example Chart",
        },
        subtitle: {
            text: "With a subtitle! And styling!",
        },
        series: [series[0], series[1]],
    };

    function toggleThirdSeries() {
        const existingSeries = chart.series.find((s) => s.name === "Group 3");

        if (existingSeries) {
            existingSeries.remove();
            thirdSeriesVisible = false;
        } else {
            chart.addSeries(series[2]);
            thirdSeriesVisible = true;
        }
    }               
</script>

<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <!--<div class="chart">
                <Chart bind:chart {options} highcharts={Highcharts} />
            </div>
            <button on:click={toggleThirdSeries} class="toggle-button">
                {thirdSeriesVisible ? "Remove Group 3" : "Add Group 3"}
            </button>
            <div>-
                <p>
                    You can use Svelte to add and remove data from a Highcharts
                    chart.
                </p>
                <p>
                    When you click the button above, a third group is toggled in
                    the chart. Check out the source code to see how it's done.
                </p>
                <p>
                    <strong
                        >🤔 How might you use other HTML elements, like
                        checkboxes or radio buttons, in a similar way to filter
                        data?</strong
                    >
                </p>
            </div>-->

            <img src="girlWritingMath.jpg">

            <br>

            <p>
               The <a href="https://blackwealthdata.org" target="_blank">Black Wealth Data Center</a>'s 
               visual on STEM vs. Non-STEM Employment Rates Among 25-34 Year Olds With a STEM Degree.
            </p>

            <p>
                Scroll through my noticings or explore the data on your own by visiting the
                <a href="https://public.tableau.com/app/profile/harsha.mallajosyula5209/viz/BWDC-PersonLevel-V1/STEMEmployment"
                target="_blank">Tableau page</a> for this data set.
            </p>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <div class="dataNoticing">
                    <h2>1</h2>
                    <p>Regardless of race, women with STEM degrees are employed less than men with STEM degrees.</p>
                </div>
            </ArticleText>

            <ArticleText>
                <div class="dataNoticing">
                    <h2>2</h2>
                    <p>Only <i class="dataText">20.7%</i> of Black women with STEM degrees were employed in STEM as of 2021, making them the least represented group.</p>
                </div>
            </ArticleText>

            <ArticleText>
                <div class="dataNoticing">
                    <h2>3</h2>
                    <p>As of 2021, Asians have the smallest gender gap for STEM employment rates, with a difference of <i class="dataText">14.6%</i> between men and women who hold STEM degrees.</p>
                </div>
            </ArticleText>

            <ArticleText>
                <div class="dataNoticing">
                    <h2>4</h2>
                    <p>Between 2019 and 2021 STEM employment for black women in the US with STEM degrees dropped from <i class="dataText">25.0%</i> to <i class="dataText">20.7%</i>.</p>
                </div>
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .chart {
        width: 90%;
        margin: 0px auto;
    }

    /*.toggle-button {
        margin: 20px;
        padding: 20px;
        color: #007052;
        background-color: #0bd956;
        border: solid 2px #007052;
        border-radius: 16px;
        font-size: large;
        cursor: pointer;
        transition: all 0.2s ease;
        box-shadow: 0 4px 0 #007052;
    }

    .toggle-button:active {
        transform: translateY(2px);
        box-shadow: 0 2px 0 #007052;
    }*/

    img {
        width: 85%;
        margin-right: auto;
        margin-left: auto;
        display: block;
    }

    h1 {
        font-family: "Winky Rough", sans-serif;
        color: #ffc0ad;
        margin: 0px;
        font-size: 45px;
        /*background-color: #271c19;
        border-radius: 5px;
        padding: 5px 10px;
        box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;*/
    }

    p {
        font-family: "Manrope", sans-serif;
        font-weight: 500;
        font-size: 20px;
        color: #fffffe;
    }

    a {
        color: #e78fb3;
    } 

    a:hover {
        color: #ffc0ad;
    }

    .dataNoticing {
        display: flex;
        align-items: center;
    }

    .dataNoticing h2 {
        margin: 0px 30px;
        font-family: "Winky Rough", sans-serif;
        color: #ffc0ad;
        font-size: 90px;
    }

    .dataText {
        font-family: "Winky Rough", sans-serif;
        color: #e78fb3;
    }
</style>
