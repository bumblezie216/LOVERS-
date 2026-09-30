<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Our Little Universe ♡</title>

<style>

/* =====================================================
   BASIC
===================================================== */

* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --text: #ffffff;
    --card: rgba(255,255,255,.12);
    --border: rgba(255,255,255,.22);
    --shadow: 0 20px 50px rgba(0,0,0,.25);
}

html {
    scroll-behavior: smooth;
}

body {
    font-family:
        Georgia,
        "Times New Roman",
        serif;

    color: var(--text);

    min-height: 100vh;

    overflow-x: hidden;

    transition:
        background 1s ease;
}


/* =====================================================
   BACKGROUND
===================================================== */

.background {
    position: fixed;

    inset: 0;

    z-index: -10;

    overflow: hidden;

    transition:
        all 1s ease;
}

.background::after {
    content: "";

    position: absolute;

    inset: 0;

    background:
        radial-gradient(
            circle at center,
            transparent 0%,
            rgba(0,0,0,.20) 100%
        );
}


/* =====================================================
   GALAXY
===================================================== */

.theme-galaxy .background {

    background:
        radial-gradient(
            circle at 20% 30%,
            rgba(164,87,255,.45),
            transparent 25%
        ),

        radial-gradient(
            circle at 80% 20%,
            rgba(78,130,255,.35),
            transparent 25%
        ),

        radial-gradient(
            circle at 60% 80%,
            rgba(244,94,188,.30),
            transparent 30%
        ),

        linear-gradient(
            135deg,
            #080015,
            #13052d 45%,
            #03030d
        );
}


/* =====================================================
   ROMANCE
===================================================== */

.theme-romance .background {

    background:
        radial-gradient(
            circle at 20% 20%,
            rgba(255,185,210,.7),
            transparent 25%
        ),

        radial-gradient(
            circle at 80% 70%,
            rgba(255,111,160,.4),
            transparent 30%
        ),

        linear-gradient(
            135deg,
            #3a071d,
            #8e234c,
            #210511
        );
}


/* =====================================================
   SPRING
===================================================== */

.theme-spring .background {

    background:
        radial-gradient(
            circle at 15% 20%,
            #ffd9e8,
            transparent 25%
        ),

        radial-gradient(
            circle at 80% 30%,
            #d8ffd9,
            transparent 25%
        ),

        linear-gradient(
            135deg,
            #5e9274,
            #a9d8a8,
            #e4c8d5
        );
}


/* =====================================================
   SUMMER
===================================================== */

.theme-summer .background {

    background:
        radial-gradient(
            circle at 50% 20%,
            #fff2a8,
            transparent 22%
        ),

        linear-gradient(
            180deg,
            #45b8e8,
            #8ee4ed 55%,
            #f8c978
        );
}


/* =====================================================
   AUTUMN
===================================================== */

.theme-autumn .background {

    background:
        radial-gradient(
            circle at 20% 20%,
            #f6b15b,
            transparent 25%
        ),

        radial-gradient(
            circle at 80% 50%,
            #a44b2a,
            transparent 30%
        ),

        linear-gradient(
            135deg,
            #30130b,
            #7d351c,
            #d17c36
        );
}


/* =====================================================
   WINTER
===================================================== */

.theme-winter .background {

    background:
        radial-gradient(
            circle at 50% 10%,
            #e7f8ff,
            transparent 20%
        ),

        linear-gradient(
            160deg,
            #102b49,
            #315d7e,
            #b8d7e8
        );
}


/* =====================================================
   DAY
===================================================== */

.theme-day .background {

    background:
        radial-gradient(
            circle at 70% 15%,
            #fff7bc,
            transparent 18%
        ),

        linear-gradient(
            #67c9f2,
            #c7efff 55%,
            #8ecf8c
        );
}


/* =====================================================
   NIGHT
===================================================== */

.theme-night .background {

    background:
        radial-gradient(
            circle at 70% 20%,
            #ffffff44,
            transparent 12%
        ),

        linear-gradient(
            180deg,
            #030514,
            #101d42,
            #182b55
        );
}


/* =====================================================
   NORTHERN LIGHTS
===================================================== */

.theme-northern .background {

    background:
        radial-gradient(
            ellipse at 20% 20%,
            rgba(43,255,207,.32),
            transparent 30%
        ),

        radial-gradient(
            ellipse at 75% 25%,
            rgba(102,104,255,.35),
            transparent 35%
        ),

        linear-gradient(
            180deg,
            #020b17,
            #061e2d 55%,
            #02070d
        );
}


.aurora {

    display: none;

    position: absolute;

    width: 130%;
    height: 55%;

    left: -15%;
    top: 5%;

    filter:
        blur(25px);

    opacity: .65;

    background:
        radial-gradient(
            ellipse at 30% 60%,
            rgba(45,255,198,.7),
            transparent 35%
        ),

        radial-gradient(
            ellipse at 60% 40%,
            rgba(93,116,255,.65),
            transparent 38%
        ),

        radial-gradient(
            ellipse at 75% 70%,
            rgba(200,70,255,.35),
            transparent 30%
        );

    animation:
        auroraMove 10s ease-in-out infinite alternate;
}

.theme-northern .aurora {
    display: block;
}

@keyframes auroraMove {

    from {
        transform:
            translateX(-4%)
            skewX(-4deg)
            scale(1);
    }

    to {
        transform:
            translateX(5%)
            skewX(5deg)
            scale(1.08);
    }
}


/* =====================================================
   SNOWY MOUNTAINS
===================================================== */

.mountains {

    display: none;

    position: absolute;

    bottom: 0;

    width: 100%;

    height: 40%;
}

.theme-snow .mountains {
    display: block;
}

.mountain {

    position: absolute;

    bottom: 0;

    width: 0;
    height: 0;

    border-left:
        170px solid transparent;

    border-right:
        170px solid transparent;

    border-bottom:
        270px solid rgba(30,55,76,.75);
}

.mountain.one {
    left: -70px;
}

.mountain.two {

    left: 25%;

    border-left-width: 220px;
    border-right-width: 220px;
    border-bottom-width: 340px;

    opacity: .8;
}

.mountain.three {

    right: -100px;

    border-left-width: 240px;
    border-right-width: 240px;
    border-bottom-width: 300px;

    opacity: .65;
}

.mountain::before {

    content: "";

    position: absolute;

    left: -70px;
    top: 0;

    width: 0;
    height: 0;

    border-left:
        70px solid transparent;

    border-right:
        70px solid transparent;

    border-bottom:
        120px solid rgba(240,250,255,.8);
}


/* =====================================================
   BEACH
===================================================== */

.beach {

    display: none;

    position: absolute;

    inset: 0;
}

.theme-beach .beach {
    display: block;
}

.beach-sun {

    position: absolute;

    width: 130px;
    height: 130px;

    border-radius: 50%;

    background:
        #fff2b5;

    box-shadow:
        0 0 70px rgba(255,240,170,.6);

    top: 13%;
    right: 15%;
}

.ocean {

    position: absolute;

    bottom: 0;

    width: 100%;

    height: 48%;

    background:

        repeating-linear-gradient(
            175deg,
            transparent 0 22px,
            rgba(255,255,255,.14) 23px 26px
        ),

        linear-gradient(
            #168db5,
            #075d82
        );
}

.sand {

    position: absolute;

    bottom: 0;

    height: 18%;

    width: 100%;

    background:
        linear-gradient(
            #e8d0a3,
            #d8b982
        );

    clip-path:
        polygon(
            0 30%,
            100% 0,
            100% 100%,
            0 100%
        );
}


/* =====================================================
   SUNSET
===================================================== */

.theme-sunset .background {

    background:
        linear-gradient(
            180deg,
            #39205e 0%,
            #a34d6d 30%,
            #ee8b63 55%,
            #ffc879 70%,
            #5d3443 100%
        );
}

.sunset-sun {

    display: none;

    position: absolute;

    width: 160px;
    height: 160px;

    border-radius: 50%;

    background:
        #ffd28b;

    box-shadow:
        0 0 90px rgba(255,170,80,.65);

    left: 50%;
    top: 25%;

    transform:
        translateX(-50%);
}

.theme-sunset .sunset-sun {
    display: block;
}


/* =====================================================
   STARS
===================================================== */

.stars {

    position: fixed;

    inset: 0;

    pointer-events: none;

    z-index: -2;
}

.star {

    position: absolute;

    width: 3px;
    height: 3px;

    background: white;

    border-radius: 50%;

    opacity: .8;

    animation:
        twinkle 3s infinite alternate;
}

@keyframes twinkle {

    from {
        opacity: .2;
        transform: scale(.7);
    }

    to {
        opacity: 1;
        transform: scale(1.3);
    }
}


/* =====================================================
   MAIN
===================================================== */

.app {

    width:
        min(1100px,92%);

    margin:
        auto;

    padding:
        35px 0 70px;
}

.glass {

    background:
        var(--card);

    border:
        1px solid var(--border);

    backdrop-filter:
        blur(18px);

    -webkit-backdrop-filter:
        blur(18px);

    border-radius:
        28px;

    box-shadow:
        var(--shadow);
}


/* =====================================================
   HEADER
===================================================== */

header {

    text-align: center;

    padding:
        50px 25px;

    margin-bottom:
        25px;
}

.logo {

    font-size:
        4rem;

    margin-bottom:
        10px;

    animation:
        floating 4s ease-in-out infinite;
}

@keyframes floating {

    50% {
        transform:
            translateY(-8px);
    }
}

h1 {

    font-size:
        clamp(
            2.4rem,
            7vw,
            5rem
        );

    margin-bottom:
        10px;
}

.subtitle {

    opacity:
        .85;

    font-size:
        1.1rem;
}


/* =====================================================
   CARDS
===================================================== */

.card {

    padding:
        28px;

    margin:
        22px 0;
}

.card h2 {

    margin-bottom:
        18px;

    font-size:
        1.8rem;
}

.center {
    text-align: center;
}

.small {

    opacity:
        .65;

    font-size:
        .85rem;

    line-height:
        1.5;
}


/* =====================================================
   FORMS
===================================================== */

input,
textarea,
select {

    width:
        100%;

    padding:
        14px 16px;

    border-radius:
        15px;

    border:
        1px solid var(--border);

    background:
        rgba(255,255,255,.12);

    color:
        white;

    outline:
        none;

    margin-top:
        8px;

    margin-bottom:
        15px;

    font-family:
        inherit;
}

select option {
    color:
        #222;
}

textarea {

    min-height:
        120px;

    resize:
        vertical;
}

label {

    display:
        block;

    margin-top:
        10px;
}

button {

    border:
        none;

    border-radius:
        50px;

    padding:
        13px 21px;

    background:
        rgba(255,255,255,.2);

    border:
        1px solid rgba(255,255,255,.3);

    color:
        white;

    cursor:
        pointer;

    font-family:
        inherit;

    font-size:
        .95rem;

    transition:
        .25s;
}

button:hover {

    transform:
        translateY(-2px);

    background:
        rgba(255,255,255,.3);
}

.primary {

    background:
        rgba(255,220,240,.25);
}

.row {

    display:
        grid;

    grid-template-columns:
        1fr 1fr;

    gap:
        15px;
}


/* =====================================================
   TIMER
===================================================== */

.timer {

    display:
        grid;

    grid-template-columns:
        repeat(4,1fr);

    gap:
        12px;

    margin-top:
        20px;
}

.time-box {

    padding:
        20px 10px;

    text-align:
        center;

    background:
        rgba(255,255,255,.09);

    border-radius:
        20px;
}

.time-box strong {

    display:
        block;

    font-size:
        2rem;
}

.time-box span {

    opacity:
        .7;

    font-size:
        .8rem;
}


/* =====================================================
   THEMES
===================================================== */

.theme-grid {

    display:
        grid;

    grid-template-columns:
        repeat(
            auto-fit,
            minmax(130px,1fr)
        );

    gap:
        12px;
}

.theme-choice {

    padding:
        20px 10px;

    border-radius:
        18px;

    text-align:
        center;

    cursor:
        pointer;

    border:
        2px solid transparent;

    background:
        rgba(255,255,255,.08);

    transition:
        .25s;
}

.theme-choice:hover {

    transform:
        translateY(-3px);
}

.theme-choice.active {

    border-color:
        white;

    background:
        rgba(255,255,255,.18);
}

.theme-preview {

    height:
        65px;

    border-radius:
        12px;

    margin-bottom:
        9px;
}

.preview-galaxy {
    background:
        radial-gradient(
            circle,
            #a84cff,
            #090018
        );
}

.preview-romance {
    background:
        linear-gradient(
            135deg,
            #ff9abb,
            #68112f
        );
}

.preview-spring {
    background:
        linear-gradient(
            135deg,
            #d9ffc9,
            #e8b8d0
        );
}

.preview-summer {
    background:
        linear-gradient(
            #4bc5ee,
            #f9cf77
        );
}

.preview-autumn {
    background:
        linear-gradient(
            135deg,
            #a94620,
            #e39a42
        );
}

.preview-winter {
    background:
        linear-gradient(
            135deg,
            #bde5fa,
            #274766
        );
}

.preview-day {
    background:
        linear-gradient(
            #65d2ff,
            #9bd58e
        );
}

.preview-night {
    background:
        linear-gradient(
            #080b24,
            #253f70
        );
}

.preview-northern {
    background:
        linear-gradient(
            135deg,
            #051d24,
            #48e0bc,
            #24366e
        );
}

.preview-snow {
    background:
        linear-gradient(
            #bde6ff,
            #506f8c
        );
}

.preview-beach {
    background:
        linear-gradient(
            #58d1ed 50%,
            #e6c58e 50%
        );
}

.preview-sunset {
    background:
        linear-gradient(
            #44245f,
            #ff9b68,
            #ffd080
        );
}


/* =====================================================
   OUR SONG
===================================================== */

.song-player {

    margin-top:
        22px;

    overflow:
        hidden;

    border-radius:
        20px;

    box-shadow:
        0 15px 35px rgba(0,0,0,.25);
}

.song-player iframe {

    display:
        block;

    width:
        100%;

    min-height:
        220px;

    border:
        none;
}

.song-empty {

    padding:
        25px;

    border-radius:
        18px;

    background:
        rgba(255,255,255,.07);

    margin-top:
        20px;
}


/* =====================================================
   WISH NOTES
===================================================== */

.wishes {

    display:
        grid;

    grid-template-columns:
        repeat(
            auto-fill,
            minmax(220px,1fr)
        );

    gap:
        18px;

    margin-top:
        22px;
}

.note {

    color:
        #392a32;

    padding:
        24px 20px;

    min-height:
        170px;

    position:
        relative;

    box-shadow:
        0 12px 25px rgba(0,0,0,.2);

    transform:
        rotate(var(--rotation));

    transition:
        .3s;

    overflow-wrap:
        anywhere;
}

.note:hover {

    transform:
        rotate(0deg)
        translateY(-5px);
}

.note:nth-child(4n+1) {
    background:
        #fff1a8;
}

.note:nth-child(4n+2) {
    background:
        #ffd6e7;
}

.note:nth-child(4n+3) {
    background:
        #d9f4ff;
}

.note:nth-child(4n+4) {
    background:
        #e0ffd8;
}

.note::before {

    content:
        "♡";

    position:
        absolute;

    top:
        8px;

    right:
        12px;

    font-size:
        22px;

    opacity:
        .5;
}

.note-date {

    font-size:
        .75rem;

    opacity:
        .6;

    margin-bottom:
        12px;
}

.note-text {

    font-family:
        "Comic Sans MS",
        "Bradley Hand",
        cursive;

    line-height:
        1.5;

    font-size:
        1.05rem;
}

.note-author {

    position:
        absolute;

    bottom:
        12px;

    right:
        15px;

    font-size:
        .8rem;

    opacity:
        .65;

    font-style:
        italic;
}

.delete-note {

    position:
        absolute;

    bottom:
        8px;

    left:
        10px;

    padding:
        4px 9px;

    font-size:
        .7rem;

    background:
        rgba(0,0,0,.08);

    color:
        #392a32;
}


/* =====================================================
   PHOTO
===================================================== */

.photo-box {

    border:
        2px dashed rgba(255,255,255,.3);

    border-radius:
        22px;

    padding:
        25px;

    text-align:
        center;

    margin-top:
        15px;
}

.photo-preview {

    margin-top:
        20px;
}

.photo-preview img {

    max-width:
        100%;

    max-height:
        500px;

    border-radius:
        20px;

    box-shadow:
        0 15px 40px rgba(0,0,0,.3);
}


/* =====================================================
   MEMORIES
===================================================== */

.memory {

    padding:
        18px;

    border-radius:
        18px;

    background:
        rgba(255,255,255,.08);

    margin-bottom:
        12px;
}

.memory small {
    opacity:
        .6;
}

.memory p {

    margin-top:
        8px;

    line-height:
        1.5;
}


/* =====================================================
   FOOTER
===================================================== */

footer {

    text-align:
        center;

    opacity:
        .7;

    padding:
        30px;
}

.hidden {
    display:
        none !important;
}


/* =====================================================
   MOBILE
===================================================== */

@media(max-width:700px) {

    .timer {

        grid-template-columns:
            repeat(2,1fr);
    }

    .row {

        grid-template-columns:
            1fr;
    }

    .card {

        padding:
            21px;
    }

    header {

        padding:
            40px 18px;
    }

    .logo {

        font-size:
            3rem;
    }

    .song-player iframe {

        min-height:
            200px;
    }
}

</style>
</head>


<body class="theme-galaxy">


<!-- =====================================================
     BACKGROUND ELEMENTS
===================================================== -->

<div class="background">

    <div class="aurora"></div>

    <div class="mountains">

        <div class="mountain one"></div>

        <div class="mountain two"></div>

        <div class="mountain three"></div>

    </div>

    <div class="beach">

        <div class="beach-sun"></div>

        <div class="ocean"></div>

        <div class="sand"></div>

    </div>

    <div class="sunset-sun"></div>

</div>


<div
    class="stars"
    id="stars"
></div>


<!-- =====================================================
     APP
===================================================== -->

<main class="app">


<!-- =====================================================
     HEADER
===================================================== -->

<header class="glass">

    <div class="logo">
        ♡
    </div>

    <h1 id="title">
        Our Little Universe
    </h1>

    <p
        class="subtitle"
        id="subtitle"
    >
        A little place that belongs to us.
    </p>

</header>


<!-- =====================================================
     SETUP
===================================================== -->

<section
    class="card glass"
    id="setup"
>

    <h2>
        ✨ Create Our Universe
    </h2>

    <div class="row">

        <div>

            <label>
                Your name
            </label>

            <input
                id="yourName"
                placeholder="Your name"
            >

        </div>


        <div>

            <label>
                Their name
            </label>

            <input
                id="theirName"
                placeholder="Their name"
            >

        </div>

    </div>


    <label>
        When did your story begin?
    </label>

    <input
        type="datetime-local"
        id="startDate"
    >


    <h3
        style="
            margin:15px 0
        "
    >
        Choose our atmosphere
    </h3>


    <div class="theme-grid">


        <div
            class="theme-choice active"
            data-theme="galaxy"
        >

            <div
                class="theme-preview preview-galaxy"
            ></div>

            🌌 Galaxy

        </div>


        <div
            class="theme-choice"
            data-theme="romance"
        >

            <div
                class="theme-preview preview-romance"
            ></div>

            💗 Romance

        </div>


        <div
            class="theme-choice"
            data-theme="spring"
        >

            <div
                class="theme-preview preview-spring"
            ></div>

            🌸 Spring

        </div>


        <div
            class="theme-choice"
            data-theme="summer"
        >

            <div
                class="theme-preview preview-summer"
            ></div>

            ☀️ Summer

        </div>


        <div
            class="theme-choice"
            data-theme="autumn"
        >

            <div
                class="theme-preview preview-autumn"
            ></div>

            🍂 Autumn

        </div>


        <div
            class="theme-choice"
            data-theme="winter"
        >

            <div
                class="theme-preview preview-winter"
            ></div>

            ❄️ Winter

        </div>


        <div
            class="theme-choice"
            data-theme="day"
        >

            <div
                class="theme-preview preview-day"
            ></div>

            🌤️ Day

        </div>


        <div
            class="theme-choice"
            data-theme="night"
        >

            <div
                class="theme-preview preview-night"
            ></div>

            🌙 Night

        </div>


        <div
            class="theme-choice"
            data-theme="northern"
        >

            <div
                class="theme-preview preview-northern"
            ></div>

            🌌 Northern Lights

        </div>


        <div
            class="theme-choice"
            data-theme="snow"
        >

            <div
                class="theme-preview preview-snow"
            ></div>

            🏔️ Snowy Mountains

        </div>


        <div
            class="theme-choice"
            data-theme="beach"
        >

            <div
                class="theme-preview preview-beach"
            ></div>

            🏖️ Beach

        </div>


        <div
            class="theme-choice"
            data-theme="sunset"
        >

            <div
                class="theme-preview preview-sunset"
            ></div>

            🌅 Sunset

        </div>

    </div>


    <br>


    <button
        class="primary"
        onclick="createUniverse()"
    >
        Create Our Universe ♡
    </button>

</section>


<!-- =====================================================
     UNIVERSE
===================================================== -->

<div
    id="universe"
    class="hidden"
>


<!-- =====================================================
     TIMER
===================================================== -->

<section
    class="card glass center"
>

    <h2>
        ♡ We've Been Us For ♡
    </h2>


    <div class="timer">


        <div class="time-box">

            <strong id="days">
                0
            </strong>

            <span>
                Days
            </span>

        </div>


        <div class="time-box">

            <strong id="hours">
                0
            </strong>

            <span>
                Hours
            </span>

        </div>


        <div class="time-box">

            <strong id="minutes">
                0
            </strong>

            <span>
                Minutes
            </span>

        </div>


        <div class="time-box">

            <strong id="seconds">
                0
            </strong>

            <span>
                Seconds
            </span>

        </div>

    </div>

</section>


<!-- =====================================================
     OUR SONG
===================================================== -->

<section
    class="card glass center"
>

    <h2>
        🎵 Our Song
    </h2>


    <p class="small">
        Add the song that feels like us ♡
    </p>


    <input
        type="url"
        id="songLink"
        placeholder="Paste a YouTube link here..."
    >


    <button
        class="primary"
        onclick="saveSong()"
    >
        Save Our Song ♡
    </button>


    <div
        id="songPlayer"
    ></div>

</section>


<!-- =====================================================
     WISHES
===================================================== -->

<section
    class="card glass"
>

    <h2>
        💌 Wishes For Us
    </h2>


    <p class="small">

        Write down the little things you wish for
        your future together. Dreams, places you want
        to visit, things you want to do, promises,
        silly ideas or anything your heart wants.

    </p>


    <textarea
        id="wishText"
        placeholder="One day I wish we could..."
    ></textarea>


    <input
        id="wishAuthor"
        placeholder="Your name"
    >


    <button
        class="primary"
        onclick="addWish()"
    >
        Pin This Wish ♡
    </button>


    <div
        class="wishes"
        id="wishes"
    ></div>

</section>


<!-- =====================================================
     PHOTO
===================================================== -->

<section
    class="card glass"
>

    <h2>
        📸 A Little Piece Of Us
    </h2>


    <p class="small">

        Upload a favourite picture and keep it here
        in your universe.

    </p>


    <div class="photo-box">

        <input
            type="file"
            id="photoInput"
            accept="image/*"
        >


        <div
            id="photoPreview"
            class="photo-preview"
        ></div>

    </div>


    <br>


    <button
        onclick="removePhoto()"
    >
        Remove Picture
    </button>


    <p
        class="small"
        style="
            margin-top:15px
        "
    >

        Your uploaded picture is saved on this
        device in this version.

    </p>

</section>


<!-- =====================================================
     MEMORIES
===================================================== -->

<section
    class="card glass"
>

    <h2>
        📖 Our Memories
    </h2>


    <input
        id="memoryTitle"
        placeholder="Memory title"
    >


    <textarea
        id="memoryText"
        placeholder="Write about this memory..."
    ></textarea>


    <button
        class="primary"
        onclick="addMemory()"
    >
        Save Memory ♡
    </button>


    <div
        id="memories"
        style="
            margin-top:20px
        "
    ></div>

</section>


<!-- =====================================================
     CHANGE THEME
===================================================== -->

<section
    class="card glass"
>

    <h2>
        🎨 Change Our World
    </h2>


    <div class="theme-grid">


        <div
            class="theme-choice"
            data-theme="galaxy"
        >

            <div
                class="theme-preview preview-galaxy"
            ></div>

            🌌 Galaxy

        </div>


        <div
            class="theme-choice"
            data-theme="romance"
        >

            <div
                class="theme-preview preview-romance"
            ></div>

            💗 Romance

        </div>


        <div
            class="theme-choice"
            data-theme="spring"
        >

            <div
                class="theme-preview preview-spring"
            ></div>

            🌸 Spring

        </div>


        <div
            class="theme-choice"
            data-theme="summer"
        >

            <div
                class="theme-preview preview-summer"
            ></div>

            ☀️ Summer

        </div>


        <div
            class="theme-choice"
            data-theme="autumn"
        >

            <div
                class="theme-preview preview-autumn"
            ></div>

            🍂 Autumn

        </div>


        <div
            class="theme-choice"
            data-theme="winter"
        >

            <div
                class="theme-preview preview-winter"
            ></div>

            ❄️ Winter

        </div>


        <div
            class="theme-choice"
            data-theme="day"
        >

            <div
                class="theme-preview preview-day"
            ></div>

            🌤️ Day

        </div>


        <div
            class="theme-choice"
            data-theme="night"
        >

            <div
                class="theme-preview preview-night"
            ></div>

            🌙 Night

        </div>


        <div
            class="theme-choice"
            data-theme="northern"
        >

            <div
                class="theme-preview preview-northern"
            ></div>

            🌌 Northern Lights

        </div>


        <div
            class="theme-choice"
            data-theme="snow"
        >

            <div
                class="theme-preview preview-snow"
            ></div>

            🏔️ Snowy Mountains

        </div>


        <div
            class="theme-choice"
            data-theme="beach"
        >

            <div
                class="theme-preview preview-beach"
            ></div>

            🏖️ Beach

        </div>


        <div
            class="theme-choice"
            data-theme="sunset"
        >

            <div
                class="theme-preview preview-sunset"
            ></div>

            🌅 Sunset

        </div>

    </div>

</section>


<!-- =====================================================
     RESET
===================================================== -->

<section
    class="card glass center"
>

    <button
        onclick="resetUniverse()"
    >
        Start A New Universe
    </button>

</section>


</div>


<footer>
    Made with love ♡
</footer>


</main>


<script>

/* =====================================================
   STAR FIELD
===================================================== */

const stars =
    document.getElementById(
        "stars"
    );

for (
    let i = 0;
    i < 120;
    i++
) {

    const star =
        document.createElement(
            "div"
        );

    star.className =
        "star";

    star.style.left =
        Math.random() * 100 + "%";

    star.style.top =
        Math.random() * 100 + "%";

    star.style.animationDelay =
        Math.random() * 4 + "s";

    star.style.opacity =
        Math.random() * .8 + .2;

    stars.appendChild(
        star
    );
}


/* =====================================================
   LOAD SAVED UNIVERSE
===================================================== */

let world = null;

try {

    const saved =
        localStorage.getItem(
            "ourLittleUniverse"
        );

    if (saved) {

        world =
            JSON.parse(
                saved
            );

    }

} catch (error) {

    console.log(
        "Could not load saved universe.",
        error
    );

}


let selectedTheme =
    world?.theme ||
    "galaxy";


/* =====================================================
   SAVE UNIVERSE
===================================================== */

function saveWorld() {

    if (!world) return;

    try {

        localStorage.setItem(
            "ourLittleUniverse",
            JSON.stringify(
                world
            )
        );

    } catch (error) {

        console.error(
            "Could not save universe:",
            error
        );

        alert(
            "Your browser may be running out of storage space. Try removing an old picture."
        );

    }

}


/* =====================================================
   SETUP INPUTS
===================================================== */

const yourNameInput =
    document.getElementById(
        "yourName"
    );

const theirNameInput =
    document.getElementById(
        "theirName"
    );

const startDateInput =
    document.getElementById(
        "startDate"
    );


/* =====================================================
   SAVE SETUP WHILE TYPING
===================================================== */

function saveSetupAsYouType() {

    if (world) return;

    const setup = {

        yourName:
            yourNameInput.value,

        theirName:
            theirNameInput.value,

        startDate:
            startDateInput.value,

        theme:
            selectedTheme

    };

    try {

        localStorage.setItem(
            "ourLittleUniverseSetup",
            JSON.stringify(
                setup
            )
        );

    } catch (error) {

        console.log(
            "Could not save setup.",
            error
        );

    }

}


yourNameInput.addEventListener(
    "input",
    saveSetupAsYouType
);

theirNameInput.addEventListener(
    "input",
    saveSetupAsYouType
);

startDateInput.addEventListener(
    "input",
    saveSetupAsYouType
);


/* =====================================================
   RESTORE SETUP
===================================================== */

function restoreSetup() {

    if (world) return;

    try {

        const savedSetup =
            localStorage.getItem(
                "ourLittleUniverseSetup"
            );

        if (!savedSetup) return;

        const setup =
            JSON.parse(
                savedSetup
            );

        yourNameInput.value =
            setup.yourName ||
            "";

        theirNameInput.value =
            setup.theirName ||
            "";

        startDateInput.value =
            setup.startDate ||
            "";

        if (setup.theme) {

            selectedTheme =
                setup.theme;

            applyTheme(
                selectedTheme,
                false
            );

            updateThemeButtons();

        }

    } catch (error) {

        console.log(
            "Could not restore setup.",
            error
        );

    }

}


/* =====================================================
   THEME BUTTONS
===================================================== */

document
.querySelectorAll(
    ".theme-choice"
)
.forEach(
    choice => {

        choice.addEventListener(
            "click",
            () => {

                selectedTheme =
                    choice.dataset.theme;

                applyTheme(
                    selectedTheme,
                    true
                );

                updateThemeButtons();

            }
        );

    }
);


function updateThemeButtons() {

    document
    .querySelectorAll(
        ".theme-choice"
    )
    .forEach(
        choice => {

            choice.classList.toggle(
                "active",
                choice.dataset.theme ===
                selectedTheme
            );

        }
    );

}


function applyTheme(
    theme,
    save = true
) {

    document.body.className =
        "theme-" +
        theme;

    selectedTheme =
        theme;

    if (
        world &&
        save
    ) {

        world.theme =
            theme;

        saveWorld();

    }

}


/* =====================================================
   CREATE UNIVERSE
===================================================== */

function createUniverse() {

    const yourName =
        yourNameInput
        .value
        .trim();

    const theirName =
        theirNameInput
        .value
        .trim();

    const startDate =
        startDateInput.value;


    if (
        !yourName ||
        !theirName ||
        !startDate
    ) {

        alert(
            "Please fill in both names and your beginning date ♡"
        );

        return;

    }


    world = {

        yourName:
            yourName,

        theirName:
            theirName,

        startDate:
            startDate,

        theme:
            selectedTheme,

        song:
            null,

        wishes:
            [],

        memories:
            [],

        photo:
            null

    };


    saveWorld();


    localStorage.removeItem(
        "ourLittleUniverseSetup"
    );


    showUniverse();

}


/* =====================================================
   SHOW UNIVERSE
===================================================== */

function showUniverse() {

    document
    .getElementById(
        "setup"
    )
    .classList.add(
        "hidden"
    );


    document
    .getElementById(
        "universe"
    )
    .classList.remove(
        "hidden"
    );


    document
    .getElementById(
        "title"
    )
    .textContent =
        world.yourName +
        " ♡ " +
        world.theirName;


    document
    .getElementById(
        "subtitle"
    )
    .textContent =
        "Our little universe, made for " +
        world.yourName +
        " and " +
        world.theirName +
        ".";


    selectedTheme =
        world.theme ||
        "galaxy";


    applyTheme(
        selectedTheme,
        false
    );


    updateThemeButtons();


    renderWishes();

    renderMemories();

    loadPhoto();

    renderSong();

    updateTimer();

}


/* =====================================================
   TIMER
===================================================== */

function updateTimer() {

    if (!world) return;


    const start =
        new Date(
            world.startDate
        ).getTime();


    const now =
        Date.now();


    let difference =
        now - start;


    if (
        difference < 0
    ) {

        difference = 0;

    }


    const totalSeconds =
        Math.floor(
            difference / 1000
        );


    const days =
        Math.floor(
            totalSeconds /
            86400
        );


    const hours =
        Math.floor(
            (
                totalSeconds %
                86400
            ) / 3600
        );


    const minutes =
        Math.floor(
            (
                totalSeconds %
                3600
            ) / 60
        );


    const seconds =
        totalSeconds %
        60;


    document
    .getElementById(
        "days"
    )
    .textContent =
        days;


    document
    .getElementById(
        "hours"
    )
    .textContent =
        hours;


    document
    .getElementById(
        "minutes"
    )
    .textContent =
        minutes;


    document
    .getElementById(
        "seconds"
    )
    .textContent =
        seconds;

}


setInterval(
    updateTimer,
    1000
);


/* =====================================================
   OUR SONG
===================================================== */

function getYouTubeID(
    url
) {

    try {

        const parsed =
            new URL(
                url
            );


        if (
            parsed.hostname
            .includes(
                "youtube.com"
            )
        ) {

            const id =
                parsed
                .searchParams
                .get("v");


            if (id) {

                return id;

            }

        }


        if (
            parsed.hostname
            .includes(
                "youtu.be"
            )
        ) {

            return parsed
                .pathname
                .replace(
                    "/",
                    ""
                )
                .split(
                    "?"
                )[0];

        }


        if (
            parsed.pathname
            .includes(
                "/embed/"
            )
        ) {

            return parsed
                .pathname
                .split(
                    "/embed/"
                )[1]
                .split(
                    "?"
                )[0];

        }

    } catch (error) {

        return null;

    }


    return null;

}


function saveSong() {

    const link =
        document
        .getElementById(
            "songLink"
        )
        .value
        .trim();


    if (!link) {

        alert(
            "Paste a YouTube link first ♡"
        );

        return;

    }


    const videoID =
        getYouTubeID(
            link
        );


    if (!videoID) {

        alert(
            "That doesn't look like a valid YouTube link ♡"
        );

        return;

    }


    world.song = {

        link:
            link,

        videoID:
            videoID

    };


    saveWorld();

    renderSong();

}


function renderSong() {

    const player =
        document
        .getElementById(
            "songPlayer"
        );


    const input =
        document
        .getElementById(
            "songLink"
        );


    if (
        !world ||
        !world.song
    ) {

        player.innerHTML = `

            <div class="song-empty">

                <div class="small">

                    Our song hasn't been chosen yet ♡

                </div>

            </div>

        `;

        return;

    }


    input.value =
        world.song.link;


    player.innerHTML = `

        <div class="song-player">

            <iframe

                src="https://www.youtube.com/embed/${world.song.videoID}"

                title="Our Song"

                frameborder="0"

                allow="
                    accelerometer;
                    autoplay;
                    clipboard-write;
                    encrypted-media;
                    gyroscope;
                    picture-in-picture;
                    web-share
                "

                allowfullscreen>

            </iframe>

        </div>


        <br>


        <button
            onclick="removeSong()"
        >

            Change Our Song

        </button>

    `;

}


function removeSong() {

    if (
        !confirm(
            "Do you want to choose a different song?"
        )
    ) {

        return;

    }


    world.song =
        null;


    saveWorld();


    document
    .getElementById(
        "songLink"
    )
    .value =
        "";


    renderSong();

}


/* =====================================================
   WISHES
===================================================== */

function addWish() {

    const text =
        document
        .getElementById(
            "wishText"
        )
        .value
        .trim();


    const author =
        document
        .getElementById(
            "wishAuthor"
        )
        .value
        .trim();


    if (!text) {

        alert(
            "Write a little wish first ♡"
        );

        return;

    }


    world.wishes =
        world.wishes ||
        [];


    world.wishes.unshift({

        text:
            text,

        author:
            author ||
            world.yourName,

        date:
            new Date()
            .toLocaleDateString(
                undefined,
                {
                    day:
                        "numeric",

                    month:
                        "short",

                    year:
                        "numeric"
                }
            )

    });


    saveWorld();


    document
    .getElementById(
        "wishText"
    )
    .value =
        "";


    document
    .getElementById(
        "wishAuthor"
    )
    .value =
        "";


    renderWishes();

}


function renderWishes() {

    const container =
        document
        .getElementById(
            "wishes"
        );


    container.innerHTML =
        "";


    world.wishes =
        world.wishes ||
        [];


    if (
        !world.wishes.length
    ) {

        container.innerHTML = `

            <div class="small">

                Your little wishes
                will live here ♡

            </div>

        `;

        return;

    }


    world.wishes.forEach(
        (
            wish,
            index
        ) => {

            const note =
                document
                .createElement(
                    "div"
                );


            note.className =
                "note";


            note.style.setProperty(
                "--rotation",
                (
                    Math.random() *
                    4 -
                    2
                ) + "deg"
            );


            note.innerHTML = `

                <div class="note-date">

                    ${escapeHTML(
                        wish.date
                    )}

                </div>


                <div class="note-text">

                    ${escapeHTML(
                        wish.text
                    )}

                </div>


                <div class="note-author">

                    — ${escapeHTML(
                        wish.author
                    )}

                </div>


                <button

                    class="delete-note"

                    onclick="
                        deleteWish(${index})
                    "

                >

                    remove

                </button>

            `;


            container.appendChild(
                note
            );

        }
    );

}


function deleteWish(
    index
) {

    if (
        !confirm(
            "Remove this little wish?"
        )
    ) {

        return;

    }


    world.wishes.splice(
        index,
        1
    );


    saveWorld();

    renderWishes();

}


/* =====================================================
   PHOTO
===================================================== */

document
.getElementById(
    "photoInput"
)
.addEventListener(
    "change",
    function(event) {

        const file =
            event
            .target
            .files[0];


        if (!file) return;


        if (
            file.size >
            8 *
            1024 *
            1024
        ) {

            alert(
                "That picture is a little too large. Please choose one under 8MB ♡"
            );

            return;

        }


        const reader =
            new FileReader();


        reader.onload =
            function(e) {

                world.photo =
                    e.target.result;


                saveWorld();

                loadPhoto();

            };


        reader.readAsDataURL(
            file
        );

    }
);


function loadPhoto() {

    const preview =
        document
        .getElementById(
            "photoPreview"
        );


    if (
        !world ||
        !world.photo
    ) {

        preview.innerHTML =
            "";

        return;

    }


    preview.innerHTML = `

        <img

            src="${world.photo}"

            alt="Our favourite picture"

        >

    `;

}


function removePhoto() {

    if (
        !world.photo
    ) {

        return;

    }


    if (
        !confirm(
            "Remove this picture from your universe?"
        )
    ) {

        return;

    }


    world.photo =
        null;


    saveWorld();


    document
    .getElementById(
        "photoInput"
    )
    .value =
        "";


    loadPhoto();

}


/* =====================================================
   MEMORIES
===================================================== */

function addMemory() {

    const title =
        document
        .getElementById(
            "memoryTitle"
        )
        .value
        .trim();


    const text =
        document
        .getElementById(
            "memoryText"
        )
        .value
        .trim();


    if (
        !title ||
        !text
    ) {

        alert(
            "Give your memory a title and a little story ♡"
        );

        return;

    }


    world.memories =
        world.memories ||
        [];


    world.memories.unshift({

        title:
            title,

        text:
            text,

        date:
            new Date()
            .toLocaleDateString(
                undefined,
                {
                    day:
                        "numeric",

                    month:
                        "long",

                    year:
                        "numeric"
                }
            )

    });


    saveWorld();


    document
    .getElementById(
        "memoryTitle"
    )
    .value =
        "";


    document
    .getElementById(
        "memoryText"
    )
    .value =
        "";


    renderMemories();

}


function renderMemories() {

    const container =
        document
        .getElementById(
            "memories"
        );


    container.innerHTML =
        "";


    world.memories =
        world.memories ||
        [];


    if (
        !world.memories.length
    ) {

        container.innerHTML = `

            <p class="small">

                Your memories
                will appear here ♡

            </p>

        `;

        return;

    }


    world.memories.forEach(
        (
            memory,
            index
        ) => {

            const div =
                document
                .createElement(
                    "div"
                );


            div.className =
                "memory";


            div.innerHTML = `

                <strong>

                    ${escapeHTML(
                        memory.title
                    )}

                </strong>


                <br>


                <small>

                    ${escapeHTML(
                        memory.date
                    )}

                </small>


                <p>

                    ${escapeHTML(
                        memory.text
                    )}

                </p>


                <button

                    onclick="
                        deleteMemory(${index})
                    "

                    style="
                        margin-top:10px
                    "

                >

                    Remove

                </button>

            `;


            container.appendChild(
                div
            );

        }
    );

}


function deleteMemory(
    index
) {

    if (
        !confirm(
            "Remove this memory?"
        )
    ) {

        return;

    }


    world.memories.splice(
        index,
        1
    );


    saveWorld();

    renderMemories();

}


/* =====================================================
   RESET EVERYTHING
===================================================== */

function resetUniverse() {

    if (
        !confirm(
            "This will erase everything saved for your universe on this device. Continue?"
        )
    ) {

        return;

    }


    localStorage.removeItem(
        "ourLittleUniverse"
    );


    localStorage.removeItem(
        "ourLittleUniverseSetup"
    );


    location.reload();

}


/* =====================================================
   ESCAPE TEXT
===================================================== */

function escapeHTML(
    value
) {

    return String(
        value
    )

    .replace(
        /&/g,
        "&amp;"
    )

    .replace(
        /</g,
        "&lt;"
    )

    .replace(
        />/g,
        "&gt;"
    )

    .replace(
        /"/g,
        "&quot;"
    )

    .replace(
        /'/g,
        "&#039;"
    );

}


/* =====================================================
   START
===================================================== */

if (world) {

    showUniverse();

} else {

    restoreSetup();

}


updateTimer();

</script>

</body>
</html>
