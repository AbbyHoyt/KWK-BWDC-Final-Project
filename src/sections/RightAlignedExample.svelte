<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    let options = {
        chart: {
            type: "pie",
        },
        title: {
            text: "An Example Pie Chart",
        },
        plotOptions: {
            pie: {
                allowPointSelect: true,
                dataLabels: [
                    {
                        enabled: true,
                        distance: 20,
                    },
                    {
                        enabled: true,
                        distance: -40,
                        format: "{point.percentage:.1f}%",
                        style: {
                            fontSize: "1.2em",
                            textOutline: "none",
                        },
                        filter: {
                            operator: ">",
                            property: "percentage",
                            value: 10,
                        },
                    },
                ],
            },
        },
        series: [
            {
                name: "Group",
                data: [
                    {
                        name: "Group 1",
                        y: 151,
                    },
                    {
                        name: "Group 2",
                        sliced: true,
                        selected: true,
                        y: 180,
                    },
                    {
                        name: "Group 3",
                        y: 32,
                    },
                    {
                        name: "Group 4",
                        y: 103,
                    },
                    {
                        name: "Group 5",
                        y: 77,
                    },
                ],
            },
        ],
    };
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <!--<div class="chart">
                <Chart {options} highcharts={Highcharts} />
            </div>-->
            <!--<p>
                Here's an example chart using
                <a href="https://www.highcharts.com/">Highcharts</a>!
            </p>-->

            <!--<img src="duck.png">-->

            <br>
            <br>

            <h1>Overview</h1>

            <p>
                It's no secret that technology has been thriving and STEM is undoubtedly 
                becoming more and more engrained in everyday life.
            </p>
                
            <p>
                Now more than ever it is important that we step back and think about who
                is included in the future technologically-driven world and who exactly
                we're leaving behind.
            </p>

            <p>
                Regardless of race or gender, everyone deserves to be represented in 
                STEM and have their voice heard.
            </p>

            <p>
                Keep scrolling to learn more about STEM employment rates in the US for those
                with STEM degrees...
            </p>
        {/snippet}

        {#snippet scrolly()}  
            <ArticleText>
                <img class="scrollImage" src="girlAtWhiteboard.jpg" alt="Woman writing on a whiteboard.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/woman-in-white-and-red-polka-dot-long-sleeve-shirt-2Q3Ivd-HsaM" target="_blank">Jeswin Thomas</a> on Unsplash.</p>
            </ArticleText>     

            <ArticleText>
                <img class="scrollImage" src="girlEngineer.jpg" alt="Woman in construction vest and hard hat.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/man-in-white-cap-and-yellow-vest-cdSKgXv2Vz4" target="_blank">ThisIsEngineering</a> on Unsplash.</p>
            </ArticleText>

            <ArticleText>
                <img class="scrollImage" src="scientists.jpg" alt="Man and woman beside microscope in a lab.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/man-in-white-chef-uniform-holding-black-and-silver-power-tool-wTrKloP4UKw" target="_blank">National Cancer Institute</a> on Unsplash.</p>
            </ArticleText>

            <ArticleText>
                <img class="scrollImage" src="graduation.jpg" alt="Woman in dark green graduation cap and gown.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/woman-standing-at-front-of-concrete-fence-wearing-academic-uniform-AQ908FfdAMw" target="_blank">Andre Hunter</a> on Unsplash.</p>
            </ArticleText>

            <ArticleText>
                <img class="scrollImage" src="girlAtComputer.jpg" alt="Girl at computer beside wooden bookshelves.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/woman-in-black-long-sleeve-shirt-using-macbook-4A1pj4_vClA" target="_blank">Annie Spratt</a> on Unsplash.</p>
            </ArticleText>

            <ArticleText>
                <img class="scrollImage" src="girlRobotics.jpg" alt="Woman beside two large robotic arms.">
                <br>
                <p class="caption">Image from <a href="https://unsplash.com/photos/woman-in-blue-sleeveless-shirt-holding-black-and-yellow-power-tool-LzwfKgKUyuw" target="_blank">ThisIsEngineering</a> on Unsplash.</p>
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .chart {
        width: 90%;
        margin: 0px auto;
    }

    img {
        width: 30%;
        margin-right: auto;
        margin-left: auto;
        display: block;
    }

    .scrollImage {
        width: 75%;
        border-radius: 5px;
        /*box-shadow: rgb(150, 86, 161) 0px 0px 0px 4px, rgb(231, 143, 179) 0px 0px 0px 8px;*/
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

    .caption {
        text-align: center;
        color: #fffffe;
        font-family: "Manrope", sans-serif;
        font-weight: 500;
        font-size: 16px;
        margin: 0px;
    }

    a {
        color: #e78fb3;
    } 

    a:hover {
        color: #ffc0ad;
    }
</style>
