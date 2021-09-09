<template>
    <div class="personalProjects">
        <div class="personalProject">
            <img class="personalProjectImage" src="McCabeThile.png">
            <div class="personalProjectText">
                <h1>The NathanLibrary</h1>
                <h4>Key Words: Python, Chemical Engineering, Algorithm</h4>
                <p>As Chemical Engineering majors, we sure are expected to know a lot about how to code. For a Computer Scientist such as myself this comes naturally, but for a lot of others it can be a major challenge.</p>
                <p>So I've compiled all of the custom functions, classes, algorithms, procedures, etc. that I've written over the course of my time in the Chemical Engineering major into one boilerplate that is easy to import and move around. This is done so that others can have easy access to a variety of problem solving tools while still being able to see how those tools work. That's why I haven't converted the NathanLibrary to a dedcated python module and moved a lot of the heavy computing to C++. Students can see my solution, and use it as a pattern to create their own.</p>
                <p>Additionally, a lot of the libraries we use a Chemical Engineers are not compatible with eachother (e.g. Sympy, pint, numpy, and scipy all have significant limitations in working with eachother). The NathanLibrary is written in a way to make each of these libraries comapible. One example would be the scipy's fsolve function does not work with pint variables. So I've written an explanative wrapper function "pintSolve" to rectify this.</p>
                <p>The library can be found on my <a href="https://github.com/NathanDavisBarrett/NathanLibrary">Github</a>.</p>
            </div>
        </div>

        <div class="personalProject personalProjectRev">
            <img class="personalProjectImageRev" src="deepLearning.jpg">
            <div class="personalProjectText">
                <h1>Material Properties Deep Learning Model</h1>
                <h4>Key Words: Python, PyTorch, Machine Learning, Deep Learning, Materials, Data</h4>
                <p>I love taking the skills that I have and applying them to new fields. This is the case with this project. Deep learning is widely in use throughout the world for purposes such as computer vision, voice recognition, fraud detection, etc. A new up-and-coming application is that of physical property prediction. Here's the problem: We know a lot about chemicals' molecular properties like their shape, size, electron denisty, and characteristics. We know a lot about their macroscopic proerties (melting point, vapor pressure, density...) from empirical evidence. But wouldn't it be cool if we could predict these properties just from their molecular structure? After all, that is where those macroscopic properties originate. But to do this now requires massive MD simulations to even get a glimpse of what these properties could be.</p>
                <p>The Goal of my deep learning model is to use the vast ammounts of data we have about chemicals' macroscopic properties and the separate, but equally vast, amounts of data we have about chemicals' molecular sctructures to train a Deep Learning model to take in a molecular structure and predict it's macroscopic properties <b>without the need of any physical tests</b>.</p>
                <p>If the model works well, it could serve as an extremely useful resource A) to the development of new chemcials since we wouldn't have to run multi-million dollar tests to accurately determine their macroscopic properties and B) to make these properties much more accesible to the public since most macroscopic data can only be found in costly textbooks, institutional databases, or are found with one's own equipment.</p>
                <p>My Model is currently being written using the PyTorch machine learning framework.</p>
            </div>
        </div>

        <div class="personalProject">
            <img class="personalProjectImage" src="NLogo_New_Transparent.png">
            <div class="personalProjectText">
                <h1>Various Web Development Projects</h1>
                <h4>Key Words: Vue, JS, Web Development, Angular</h4>
                <p>What I love about web development is the freedom it allows me to have while still using my talents and skills. I enjoy spending my spare time making great-looking websites. Examples (with their accompanying source code) include <a href="https://www.nathandavisbarrett.com">this website</a> (<a href="https://github.com/NathanDavisBarrett/NathanDavisBarrett.com">code</a>), my wife's website <a href="https://www.catherinabarrett.com">CatherinaBarrett.com</a> (<a href="https://github.com/NathanDavisBarrett/CatherinaBarrett.com">code</a>), our wedding website <a href="https://www.kateandnatebarrett.com">KateAndNateBarrett.com</a> (<a href="https://github.com/NathanDavisBarrett/weddingWebsite">code</a>), and several others that can be found on my <a href="https://github.com/NathanDavisBarrett">Github</a>.</p>
                <p>While most of my experience is with Vue, I'm also currently learning the Angular framework and intend to learn the React framework eventually.</p>
            </div>

        </div>
    </div>
</template>

<style>
.personalProjects {
    width: 100%;
    display: flex;
    flex-direction: column;
    text-align: left;
}

@media only screen and (min-width: 641px) {
    .personalProject {
        width: 100%;
        /* display: flex;
        flex-direction: row; */
        margin-bottom: 40px;
        justify-content: center;
        align-items: center;
    }
    .personalProjectText {
        /* display: flex;
        flex-direction: column;
        flex-grow: 1;
        flex-basis: 0; */
        margin-left: 8px;
        margin-right: 8px;
    }

    .personalProjectText h4 {
        margin-top: 0px;
    }

    .personalProject img {
        margin: 15px;
        height: 200px;
    }

    .personalProjectImage {
        float: left;
    }

    .personalProjectImageRev {
        float: right;
    }
}
@media only screen and (max-width: 640px) {
    .personalProject {
        width: 100%;
        display: flex;
        flex-direction: column-reverse;
        margin-bottom: 40px;
        justify-content: center;
        align-items: center;
    }
    .personalProjectText {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        flex-basis: 0;
        margin-left: 8px;
        margin-right: 8px;
    }
    .personalProjectText h4 {
        margin-top: 0px;
    }

    .personalProject img {
        margin-top: 15px;
        height: 200px;
        flex-grow: 1;
        flex-basis: 0;
    }
}
</style>
