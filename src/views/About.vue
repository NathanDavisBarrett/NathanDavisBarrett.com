<template>
    <div class="about">
        <h1>Overview</h1>
        <div class="aboutSection">
            <div class="aboutSectionTextWrapper">
                <p>Nothing thrills me more than the feeling I get when my projects make a difference for the people around me. Whether it be a new computer algorithm, a breakthrough approach to solving a difficult homework problem with friends, or even a musical piece I preform for a few of my loved ones. This is what drives me to be a great engineer, researcher, student, husband, friend, and community member.</p>
            </div>
            <img src="DSCF4625_crop.png">

        </div>

        <h1>Personal Philosophies</h1>
        <div class="philSection">
            <div class="philPoint">
                <h3>Life, Liberty, and the Persuit of Happiness</h3>
                <p>I beleive that life is worth living. Each and <b>every person has immense potential and should be free to realize it</b>, if they choose to work towards it. Similarly, I beleive that happiness is found in living a good, honest, diligent, involved, and aware life.</p>
            </div>

            <div class="philPoint">
                <h3>Kindness and Respect</h3>
                <p><b>The happiest way to live life is to be kind to yourself and others.</b> Many of the hardest parts of life can be made better simply be being kind. I try to conciously realize that virtually all people are doing their best. Getting worked up when things don't go as you'd like almost never makes the situation better. The best way to handle the best and worst times in life are to be respectful and kind.</p>
            </div>

            <div class="philPoint">
                <h3>Reasonability</h3>
                <p>When decision making, everyone should <b>take a moment to think, consider various aspects of a situation, ask for valuable advice, and reflect</b>. Rushed, thoughtless, or careless decisions often lead regrets and mistakes. Aspects such as logical reasonablness, emotional awareness of yourself and others, external factors, and eventual outcomes should all be considered.</p>
            </div>

            <div class="philPoint">
                <h3>Appropriate Confidence, and Humility</h3>
                <p>I beleive <b>experts should be experts</b>, and we should let them be. When you are the expert, and you have reason to be confident, you should not be afraid to assert it. However, there are many instances where overconfidence has lead to misinformation, accidents, and heartache. When appropriate, we should not be ashamed or too arragant to receive help and input from others.</p>
            </div>

            <div class="philPoint">
                <h3>Hard Work and Not Being Complacent</h3>
                <p>With nearly all things in life, <b>the greater the reward, the higher the price to get it</b>. So if you want a lot out of life, you should expect to work for it. Complacency robs people of the greatest and most fulfilling aspects of life.</p>
            </div>
        </div>

        <h1>Family Life</h1>
        <div class="aboutSection">
            <img src="Kate_and_Nate_Formals_058.JPG">
            <div class="aboutSectionTextWrapper">
                <p>I was born an raised in a small town in rural Colorado. With both of my parents being school teachers, I quickly gained a love of learning and creating. </p>
                <p>After years of studying, countless extracirricular activites, work, and play, I chose to study Chemical Engineering at Brigham Young Univeristy.</p>
                <p>There I met and married my inspiring, beautiful, and caring wife Catherina. While I might know how to make great things for the world, she knows how to make the world great. For the time being we are still living in Provo until we both go to graduate school.</p>
            </div>
        </div>

        <h1>Hobbies / Interests</h1>
        <div class="aboutSection">
            <div class="aboutSectionTextWrapper">
                <h3>Music</h3>
                <p>Music has been a large part of my life ever since I very young. It's pushed me to try my hardest, to love what I do, and to love sharing my talents with others.</p>
                <p>I've been involved in a variety of ensembles (The U.S. Army All-American Marching Band, The BYU Cougar Marching/Pep Bands, The Colorado All-State Band, The Western Colorado Honor Chior, various Jazz ensebles, etc.) and loved each one.</p>
                <p>For me, music is a way to connect with myself in a different way than I can in other aspects of living.</p>
            </div>
            <img src="Saxastar.png">
        </div>

        <div class="aboutSection aboutSectionRev">
            <img src="mission.jpg">
            <div class="aboutSectionTextWrapper">
                <h3>Church</h3>
                <p>Church service has always been very important to me. As a young person, I was very active in my youth group and in my congregation. I also served a two year full-time mission for <a href="https://www.churchofjesuschrist.org/comeuntochrist">The Church of Jesus Christ of Latter-Day Saints</a> in Indiana.</p>
                <p>My mission and other church service taught me the importance of putting others' needs above my own and importance of loving every part of my life.</p>
            </div>
        </div>

        <div class="aboutSection">
            <div class="aboutSectionTextWrapper">
                <h3>Philosophical Discussion</h3>
                <p>I love discussing ideas about the universe with anyone who's willing to to stretch and be stretched. My wife and I love to talk about our ideas over our favotire foods: Pizza, Pizza, and Pizza.</p>
            </div>
            <img src="pizza.jpg">
        </div>

        <div class="aboutSection aboutSectionRev">
            <img src="triathalon.jpg">
            <div class="aboutSectionTextWrapper">
                <h3>Cycling</h3>
                <p>Whenever we get the chance, my wife and I love getting out on our bikes. We're lucky to live in a place with plenty of bike trials near our house that we ride of frequently. We also have competed in a triathalon and plan on racing in more in the future.</p>
            </div>
        </div>
    </div>
</template>

<style scooped>
.about {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
}

@media only screen and (min-width: 601px) {
    .aboutSection {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;

        flex: 1;
    }

    .aboutSectionTextWrapper {
        text-align: left;
        flex-grow: 1;
        flex-basis: 0;
        margin-left: 30px;
        margin-right: 30px;
    }

    .aboutSection img {
        max-width: 50%;
        max-height: 400px;
        flex-basis: 0;
    }
}
@media only screen and (max-width: 600px) {
    .aboutSection {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        flex: 1;
    }

    .aboutSectionTextWrapper {
        text-align: left;
        margin-left: 30px;
        margin-right: 30px;
    }

    .aboutSection img {
        margin-top: 15px;
        margin-bottom: 15px;
        max-height: 400px;
        max-width: 100%;
    }

    .aboutSectionRev {
        flex-direction: column-reverse;
    }
}

.philSection {
    width: 100%;
    display: flex;
    flex-direction: column;
}

.philPoint {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    margin-left: 30px;
}

.philPoint p {
    text-align: left;
    margin-left: 30px;
}
</style>
