<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#160d2b">

<title>Our Little Universe ♡</title>

<style>

/* =========================================================
   BASE
========================================================= */

* {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
}

html {
    scroll-behaviour: smooth;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, "Times New Roman", serif;
    color: var(--text);
    background: var(--background);
    overflow-x: hidden;
    transition:
        background 1s ease,
        color 1s ease;
}

/* =========================================================
   THEMES
========================================================= */

body.theme-galaxy {
    --background:
        radial-gradient(circle at 20% 10%, rgba(255,180,210,.18), transparent 28%),
        radial-gradient(circle at 85% 25%, rgba(120,150,255,.18), transparent 30%),
        radial-gradient(circle at 50% 90%, rgba(180,100,255,.16), transparent 30%),
        linear-gradient(145deg, #08040f, #160b27 45%, #090513);

    --card: rgba(255,255,255,.075);
    --border: rgba(255,255,255,.14);
    --text: #ffffff;
    --muted: rgba(255,255,255,.68);
    --button: #ffffff;
    --buttonText: #251132;
    --accent: #d9c0ff;
}

body.theme-romance {
    --background:
        radial-gradient(circle at 20% 20%, rgba(255,120,150,.35), transparent 30%),
        radial-gradient(circle at 80% 80%, rgba(180,50,90,.28), transparent 35%),
        linear-gradient(145deg, #260817, #4b1026, #16040d);

    --card: rgba(255,220,230,.09);
    --border: rgba(255,190,210,.22);
    --text: #fff5f8;
    --muted: rgba(255,235,240,.72);
    --button: #fff0f5;
    --buttonText: #511328;
    --accent: #ff9bb8;
}

body.theme-spring {
    --background:
        radial-gradient(circle at 20% 15%, rgba(255,180,210,.35), transparent 28%),
        radial-gradient(circle at 80% 20%, rgba(170,255,190,.25), transparent 30%),
        linear-gradient(145deg, #173b2b, #305d43, #152d23);

    --card: rgba(230,255,235,.09);
    --border: rgba(210,255,225,.22);
    --text: #f5fff7;
    --muted: rgba(235,255,240,.72);
    --button: #f1fff5;
    --buttonText: #214b31;
    --accent: #b7f0c4;
}

body.theme-summer {
    --background:
        radial-gradient(circle at 20% 10%, rgba(255,230,130,.4), transparent 28%),
        radial-gradient(circle at 85% 30%, rgba(255,160,100,.3), transparent 30%),
        linear-gradient(145deg, #51351a, #9b552b, #d07a43);

    --card: rgba(255,245,220,.10);
    --border: rgba(255,240,200,.24);
    --text: #fffaf0;
    --muted: rgba(255,248,225,.75);
    --button: #fff5dc;
    --buttonText: #70431c;
    --accent: #ffd77d;
}

body.theme-autumn {
    --background:
        radial-gradient(circle at 20% 10%, rgba(200,90,40,.32), transparent 28%),
        radial-gradient(circle at 80% 40%, rgba(140,55,30,.28), transparent 30%),
        linear-gradient(145deg, #28130d, #542817, #32140d);

    --card: rgba(255,220,180,.08);
    --border: rgba(255,190,130,.2);
    --text: #fff5e8;
    --muted: rgba(255,230,205,.72);
    --button: #fff0dc;
    --buttonText: #63321b;
    --accent: #e89b5c;
}

body.theme-winter {
    --background:
        radial-gradient(circle at 20% 15%, rgba(170,230,255,.3), transparent 30%),
        radial-gradient(circle at 80% 20%, rgba(210,240,255,.25), transparent 30%),
        linear-gradient(145deg, #081a2b, #123b58, #081522);

    --card: rgba(220,245,255,.08);
    --border: rgba(210,245,255,.2);
    --text: #f4fbff;
    --muted: rgba(225,245,255,.72);
    --button: #effaff;
    --buttonText: #15364b;
    --accent: #bcecff;
}

body.theme-day {
    --background:
        radial-gradient(circle at 50% 5%, rgba(255,255,255,.7), transparent 25%),
        linear-gradient(180deg, #70c8ff, #bce9ff 55%, #d9f5ff);

    --card: rgba(255,255,255,.25);
    --border: rgba(255,255,255,.45);
    --text: #12334a;
    --muted: rgba(20,55,75,.7);
    --button: #ffffff;
    --buttonText: #17415a;
    --accent: #65aeda;
}

body.theme-night {
    --background:
        radial-gradient(circle at 70% 15%, rgba(120,150,255,.2), transparent 25%),
        radial-gradient(circle at 20% 60%, rgba(80,100,200,.15), transparent 30%),
        linear-gradient(145deg, #03050f, #09132d, #050712);

    --card: rgba(200,220,255,.06);
    --border: rgba(190,220,255,.16);
    --text: #f5f8ff;
    --muted: rgba(220,230,255,.7);
    --button: #eef4ff;
    --buttonText: #17294d;
    --accent: #a9c7ff;
}

/* =========================================================
   BACKGROUND EFFECTS
========================================================= */

#stars {
    position: fixed;
    inset: 0;
    z-index: -2;
    pointer-events: none;
}

.star {
    position: absolute;
    width: 3px;
    height: 3px;
    border-radius: 50%;
    background: white;
    opacity: .5;
    animation: twinkle 3s infinite alternate;
}

@keyframes twinkle {
    from {
        opacity: .2;
        transform: scale(.7);
    }

    to {
        opacity: 1;
        transform: scale(1.4);
    }
}

/* =========================================================
   CONTAINER
========================================================= */

.container {
    width: min(900px, 92%);
    margin: auto;
    padding-bottom: 70px;
}

/* =========================================================
   HERO
========================================================= */

.hero {
    text-align: center;
    padding: 65px 10px 35px;
}

.hero-icon {
    font-size: 4rem;
    animation: float 4s ease-in-out infinite;
}

@keyframes float {
    0%,100% {
        transform: translateY(0);
    }

    50% {
        transform: translateY(-12px);
    }
}

.hero h1 {
    font-size: clamp(2.7rem, 10vw, 5.5rem);
    margin: 10px 0;
    line-height: 1;
}

.hero p {
    color: var(--muted);
    font-size: 1.1rem;
}

/* =========================================================
   CARDS
========================================================= */

.card {
    margin: 22px 0;
    padding: 28px;
    border-radius: 28px;

    background: var(--card);

    border: 1px solid var(--border);

    box-shadow:
        0 20px 60px rgba(0,0,0,.2);

    backdrop-filter: blur(16px);

    transition:
        background 1s ease,
        border 1s ease;
}

.card h2 {
    margin-top: 0;
    font-size: 1.7rem;
}

/* =========================================================
   SETUP
========================================================= */

.setup {
    text-align: center;
}

.setup h2 {
    font-size: 2rem;
}

.setup input {
    margin-bottom: 12px;
}

/* =========================================================
   THEME SELECTOR
========================================================= */

.theme-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin: 20px 0;
}

.theme-option {
    position: relative;
    border: 2px solid transparent;
    border-radius: 20px;
    padding: 18px 12px;
    cursor: pointer;
    text-align: center;
    transition: .25s;
    overflow: hidden;
}

.theme-option:hover {
    transform: translateY(-3px);
}

.theme-option.selected {
    border-color: white;
    box-shadow:
        0 0 0 3px rgba(255,255,255,.15),
        0 10px 30px rgba(0,0,0,.25);
}

.theme-icon {
    font-size: 2rem;
    display: block;
    margin-bottom: 6px;
}

.theme-name {
    font-weight: bold;
}

.theme-description {
    font-size: .78rem;
    opacity: .7;
    margin-top: 4px;
}

/* Individual theme previews */

.preview-galaxy {
    background:
        radial-gradient(circle at 20% 20%, #b27cff, transparent 30%),
        linear-gradient(135deg,#090014,#29104b,#05030b);
}

.preview-romance {
    background:
        radial-gradient(circle at 30% 20%, #ff8fac, transparent 35%),
        linear-gradient(135deg,#3c081d,#8b2042,#28030f);
}

.preview-spring {
    background:
        radial-gradient(circle at 20% 20%, #ffb8d2, transparent 30%),
        linear-gradient(135deg,#173d2b,#5e9870);
}

.preview-summer {
    background:
        radial-gradient(circle at 50% 10%, #ffe68a, transparent 30%),
        linear-gradient(135deg,#734017,#e68b4c);
}

.preview-autumn {
    background:
        radial-gradient(circle at 20% 20%, #d8793e, transparent 30%),
        linear-gradient(135deg,#28110a,#813c1c);
}

.preview-winter {
    background:
        radial-gradient(circle at 60% 15%, #d7f5ff, transparent 30%),
        linear-gradient(135deg,#07182a,#25618a);
}

.preview-day {
    background:
        radial-gradient(circle at 50% 10%, white, transparent 25%),
        linear-gradient(180deg,#62c6ff,#c9f0ff);
}

.preview-night {
    background:
        radial-gradient(circle at 70% 15%, #9abaff, transparent 20%),
        linear-gradient(135deg,#030511,#11285a);
}

/* =========================================================
   TIMER
========================================================= */

.timer {
    text-align: center;
}

.timer-big {
    font-size: clamp(2rem, 9vw, 4.5rem);
    font-weight: bold;
    margin: 20px 0 5px;
}

.timer-small {
    color: var(--muted);
}

.timer-date {
    margin-top: 20px;
    color: var(--muted);
}

/* =========================================================
   BUTTONS
========================================================= */

button {
    border: none;
    border-radius: 999px;
    padding: 13px 21px;
    margin: 5px;
    font-family: inherit;
    font-size: 1rem;
    cursor: pointer;

    background: var(--button);
    color: var(--buttonText);

    transition:
        transform .2s,
        box-shadow .2s;
}

button:hover {
    transform: translateY(-2px);
    box-shadow:
        0 8px 25px rgba(0,0,0,.15);
}

button:active {
    transform: scale(.96);
}

/* =========================================================
   INPUTS
========================================================= */

input,
textarea {
    width: 100%;
    border: 1px solid var(--border);
    border-radius: 17px;

    background: rgba(0,0,0,.18);

    color: var(--text);

    padding: 15px;

    font-family: inherit;
    font-size: 1rem;

    outline: none;

    margin: 7px 0;
}

input::placeholder,
textarea::placeholder {
    color: var(--muted);
}

textarea {
    min-height: 140px;
    resize: vertical;
}

/* =========================================================
   SECRET MESSAGE
========================================================= */

.secret {
    text-align: center;
}

.secret-box {
    display: none;

    margin-top: 20px;

    padding: 25px;

    border-radius: 20px;

    background: rgba(255,255,255,.08);

    line-height: 1.8;

    animation: reveal .6s ease;
}

.secret-box.show {
    display: block;
}

@keyframes reveal {
    from {
        opacity: 0;
        transform: scale(.94);
    }

    to {
        opacity: 1;
        transform: scale(1);
    }
}

/* =========================================================
   MEMORIES
========================================================= */

.memory {
    margin-top: 15px;
    padding: 20px;

    border-radius: 20px;

    background: rgba(255,255,255,.055);

    border: 1px solid var(--border);
}

.memory h3 {
    margin-top: 0;
}

.memory-date {
    color: var(--muted);
    font-size: .85rem;
    margin-top: 10px;
}

/* =========================================================
   LINK
========================================================= */

.world-link {
    word-break: break-all;

    padding: 15px;

    border-radius: 15px;

    background: rgba(0,0,0,.2);

    color: var(--muted);

    font-size: .85rem;
}

/* =========================================================
   TEXT
========================================================= */

.small {
    font-size: .85rem;
    color: var(--muted);
    line-height: 1.6;
}

.empty {
    text-align: center;
    color: var(--muted);
    padding: 20px;
}

/* =========================================================
   NOTIFICATION
========================================================= */

.notification {
    position: fixed;

    left: 50%;
    bottom: 25px;

    transform:
        translateX(-50%)
        translateY(100px);

    padding: 14px 22px;

    border-radius: 999px;

    background: rgba(20,10,35,.95);

    border: 1px solid rgba(255,255,255,.15);

    transition: .35s;

    z-index: 50;

    opacity: 0;
}

.notification.show {
    transform:
        translateX(-50%)
        translateY(0);

    opacity: 1;
}

/* =========================================================
   FOOTER
========================================================= */

footer {
    text-align: center;
    color: var(--muted);
    padding: 30px;
    font-size: .9rem;
}

/* =========================================================
   MOBILE
========================================================= */

@media (max-width: 600px) {

    .theme-grid {
        grid-template-columns: 1fr 1fr;
    }

    .card {
        padding: 22px;
    }

    .hero {
        padding-top: 45px;
    }

}

</style>
</head>

<body class="theme-galaxy">

<div id="stars"></div>

<div class="container">

<!-- =====================================================
     HERO
===================================================== -->

<section class="hero">

    <div
        id="heroIcon"
        class="hero-icon"
    >
        🌌
    </div>

    <h1>
        Our Little Universe
    </h1>

    <p>
        One little world that belongs to two people.
    </p>

    <div>
        ♡
    </div>

</section>


<!-- =====================================================
     CREATE WORLD
===================================================== -->

<section
    id="setupSection"
    class="card setup"
>

    <h2>
        🌎 Create Your World
    </h2>

    <p>
        Give your shared world a name,
        choose when your story began,
        and choose the atmosphere you want.
    </p>

    <input
        id="universeName"
        placeholder="Our Little Universe"
    >

    <input
        id="startDate"
        type="datetime-local"
    >


    <h3>
        Choose Your Theme
    </h3>

    <div class="theme-grid">

        <div
            class="theme-option preview-galaxy selected"
            data-theme="galaxy"
            onclick="selectTheme('galaxy', this)"
        >
            <span class="theme-icon">🌌</span>

            <div class="theme-name">
                Galaxy
            </div>

            <div class="theme-description">
                Stars & cosmic nights
            </div>
        </div>


        <div
            class="theme-option preview-romance"
            data-theme="romance"
            onclick="selectTheme('romance', this)"
        >
            <span class="theme-icon">💗</span>

            <div class="theme-name">
                Romance
            </div>

            <div class="theme-description">
                Hearts & roses
            </div>
        </div>


        <div
            class="theme-option preview-spring"
            data-theme="spring"
            onclick="selectTheme('spring', this)"
        >
            <span class="theme-icon">🌸</span>

            <div class="theme-name">
                Spring
            </div>

            <div class="theme-description">
                Flowers & new beginnings
            </div>
        </div>


        <div
            class="theme-option preview-summer"
            data-theme="summer"
            onclick="selectTheme('summer', this)"
        >
            <span class="theme-icon">☀️</span>

            <div class="theme-name">
                Summer
            </div>

            <div class="theme-description">
                Golden warmth
            </div>
        </div>


        <div
            class="theme-option preview-autumn"
            data-theme="autumn"
            onclick="selectTheme('autumn', this)"
        >
            <span class="theme-icon">🍂</span>

            <div class="theme-name">
                Autumn
            </div>

            <div class="theme-description">
                Cosy falling leaves
            </div>
        </div>


        <div
            class="theme-option preview-winter"
            data-theme="winter"
            onclick="selectTheme('winter', this)"
        >
            <span class="theme-icon">❄️</span>

            <div class="theme-name">
                Winter
            </div>

            <div class="theme-description">
                Snow & icy nights
            </div>
        </div>


        <div
            class="theme-option preview-day"
            data-theme="day"
            onclick="selectTheme('day', this)"
        >
            <span class="theme-icon">☁️</span>

            <div class="theme-name">
                Day
            </div>

            <div class="theme-description">
                Sky & sunshine
            </div>
        </div>


        <div
            class="theme-option preview-night"
            data-theme="night"
            onclick="selectTheme('night', this)"
        >
            <span class="theme-icon">🌙</span>

            <div class="theme-name">
                Night
            </div>

            <div class="theme-description">
                Moonlight & stars
            </div>
        </div>

    </div>


    <button
        onclick="createUniverse()"
    >
        Create Our World ♡
    </button>

    <p class="small">
        Your selected theme will be saved with this universe.
    </p>

</section>


<!-- =====================================================
     APP
===================================================== -->

<div
    id="app"
    style="display:none;"
>


<!-- TIMER -->

<section class="card timer">

    <h2 id="worldTitle">
        Our Little Universe ♡
    </h2>

    <p>
        We've been us for...
    </p>

    <div
        id="timer"
        class="timer-big"
    >
        0d 0h 0m 0s
    </div>

    <div class="timer-small">
        days • hours • minutes • seconds
    </div>

    <div
        id="startDateDisplay"
        class="timer-date"
    ></div>

</section>


<!-- SECRET -->

<section class="card secret">

    <h2>
        💌 A Secret Message
    </h2>

    <p>
        Someone left something here for you.
    </p>

    <button onclick="openSecret()">
        Open My Secret Message
    </button>

    <div
        id="secretBox"
        class="secret-box"
    ></div>

</section>


<!-- WRITE SECRET -->

<section class="card">

    <h2>
        💗 Leave Something For Me
    </h2>

    <p class="small">
        Write something you want your person
        to find. It will stay hidden until
        they choose to open it.
    </p>

    <textarea
        id="secretInput"
        placeholder="Write something from your heart..."
    ></textarea>

    <button
        onclick="saveSecret()"
    >
        Hide My Message ♡
    </button>

</section>


<!-- MEMORIES -->

<section class="card">

    <h2>
        📖 Our Memories
    </h2>

    <input
        id="memoryTitle"
        placeholder="Memory title"
    >

    <textarea
        id="memoryText"
        placeholder="Write about this moment..."
    ></textarea>

    <button
        onclick="saveMemory()"
    >
        Add Memory ♡
    </button>

    <div id="memories"></div>

</section>


<!-- THEME CHANGE -->

<section class="card">

    <h2>
        🎨 Change Our Theme
    </h2>

    <p class="small">
        You can change the atmosphere of your universe
        whenever you want.
    </p>

    <div class="theme-grid">

        <div
            class="theme-option preview-galaxy"
            onclick="changeTheme('galaxy')"
        >
            🌌<br>
            Galaxy
        </div>

        <div
            class="theme-option preview-romance"
            onclick="changeTheme('romance')"
        >
            💗<br>
            Romance
        </div>

        <div
            class="theme-option preview-spring"
            onclick="changeTheme('spring')"
        >
            🌸<br>
            Spring
        </div>

        <div
            class="theme-option preview-summer"
            onclick="changeTheme('summer')"
        >
            ☀️<br>
            Summer
        </div>

        <div
            class="theme-option preview-autumn"
            onclick="changeTheme('autumn')"
        >
            🍂<br>
            Autumn
        </div>

        <div
            class="theme-option preview-winter"
            onclick="changeTheme('winter')"
        >
            ❄️<br>
            Winter
        </div>

        <div
            class="theme-option preview-day"
            onclick="changeTheme('day')"
        >
            ☁️<br>
            Day
        </div>

        <div
            class="theme-option preview-night"
            onclick="changeTheme('night')"
        >
            🌙<br>
            Night
        </div>

    </div>

</section>


<!-- LINK -->

<section class="card">

    <h2>
        🔗 Our World Link
    </h2>

    <p class="small">
        This is the link for this particular universe.
        Share it with your person.
    </p>

    <div
        id="worldLink"
        class="world-link"
    ></div>

    <button
        onclick="copyWorldLink()"
    >
        Copy Link
    </button>

</section>


<!-- SETTINGS -->

<section class="card">

    <h2>
        🌙 Universe Settings
    </h2>

    <button
        onclick="changeUniverseName()"
    >
        Change Universe Name
    </button>

    <button
        onclick="clearLocalWorld()"
    >
        Reset This Browser
    </button>

</section>

</div>

</div>


<footer>
    Made with love ♡
</footer>


<div
    id="notification"
    class="notification"
></div>


<script>

/* =========================================================
   VARIABLES
========================================================= */

let world = null;

let selectedTheme = "galaxy";


/* =========================================================
   THEME INFORMATION
========================================================= */

const themeInfo = {

    galaxy: {
        icon: "🌌"
    },

    romance: {
        icon: "💗"
    },

    spring: {
        icon: "🌸"
    },

    summer: {
        icon: "☀️"
    },

    autumn: {
        icon: "🍂"
    },

    winter: {
        icon: "❄️"
    },

    day: {
        icon: "☁️"
    },

    night: {
        icon: "🌙"
    }

};


/* =========================================================
   SELECT THEME
========================================================= */

function selectTheme(theme, element) {

    selectedTheme = theme;

    document
        .querySelectorAll(".theme-option")
        .forEach(option => {

            option.classList.remove(
                "selected"
            );

        });

    if (element) {

        element.classList.add(
            "selected"
        );

    }

    applyTheme(theme);
}


/* =========================================================
   APPLY THEME
========================================================= */

function applyTheme(theme) {

    const themes = [
        "galaxy",
        "romance",
        "spring",
        "summer",
        "autumn",
        "winter",
        "day",
        "night"
    ];

    themes.forEach(name => {

        document.body.classList.remove(
            "theme-" + name
        );

    });

    document.body.classList.add(
        "theme-" + theme
    );

    const icon =
        document.getElementById(
            "heroIcon"
        );

    if (icon && themeInfo[theme]) {

        icon.textContent =
            themeInfo[theme].icon;

    }

}


/* =========================================================
   CHANGE EXISTING THEME
========================================================= */

function changeTheme(theme) {

    if (!world)
        return;

    world.theme = theme;

    saveWorld();

    applyTheme(theme);

    notify(
        "Your universe changed its atmosphere ♡"
    );
}


/* =========================================================
   RANDOM WORLD ID
========================================================= */

function generateWorldId() {

    return (
        "world-" +
        Math.random()
            .toString(36)
            .substring(2, 10) +
        "-" +
        Date.now().toString(36)
    );
}


/* =========================================================
   URL WORLD ID
========================================================= */

function getWorldIdFromURL() {

    const params =
        new URLSearchParams(
            window.location.search
        );

    return params.get("world");
}


/* =========================================================
   LOAD WORLD
========================================================= */

function loadWorld() {

    const saved =
        localStorage.getItem(
            "ourUniverseWorld"
        );

    if (!saved) {

        document
            .getElementById("setupSection")
            .style.display = "block";

        return;
    }

    try {

        world =
            JSON.parse(saved);

        if (!world.theme) {

            world.theme =
                "galaxy";

        }

        applyTheme(
            world.theme
        );

        showApp();

    } catch {

        localStorage.removeItem(
            "ourUniverseWorld"
        );

    }

}


/* =========================================================
   CREATE WORLD
========================================================= */

function createUniverse() {

    const name =
        document
            .getElementById(
                "universeName"
            )
            .value
            .trim()
        || "Our Little Universe";

    const date =
        document
            .getElementById(
                "startDate"
            )
            .value;

    if (!date) {

        notify(
            "Choose the date your story began ♡"
        );

        return;
    }


    world = {

        id:
            generateWorldId(),

        name:
            name,

        startDate:
            new Date(date)
                .toISOString(),

        theme:
            selectedTheme,

        secrets:
            [],

        memories:
            []

    };


    saveWorld();


    const url =
        new URL(
            window.location.href
        );

    url.searchParams.set(
        "world",
        world.id
    );

    window.history.replaceState(
        {},
        "",
        url
    );


    applyTheme(
        world.theme
    );


    showApp();


    notify(
        "Your universe has been created ♡"
    );
}


/* =========================================================
   SAVE WORLD
========================================================= */

function saveWorld() {

    localStorage.setItem(
        "ourUniverseWorld",
        JSON.stringify(world)
    );

}


/* =========================================================
   SHOW APP
========================================================= */

function showApp() {

    document
        .getElementById(
            "setupSection"
        )
        .style.display = "none";


    document
        .getElementById(
            "app"
        )
        .style.display = "block";


    document
        .getElementById(
            "worldTitle"
        )
        .textContent =
        world.name + " ♡";


    document
        .getElementById(
            "startDateDisplay"
        )
        .textContent =
        "Since " +
        new Date(
            world.startDate
        ).toLocaleString();


    const shareURL =
        new URL(
            window.location.href
        );

    shareURL.searchParams.set(
        "world",
        world.id
    );


    document
        .getElementById(
            "worldLink"
        )
        .textContent =
        shareURL.toString();


    applyTheme(
        world.theme
    );


    renderMemories();

    startTimer();

}


/* =========================================================
   TIMER
========================================================= */

let timerStarted = false;

function startTimer() {

    if (timerStarted)
        return;

    timerStarted = true;


    function updateTimer() {

        if (!world)
            return;


        const start =
            new Date(
                world.startDate
            ).getTime();


        const now =
            Date.now();


        let difference =
            now - start;


        if (difference < 0)
            difference = 0;


        const totalSeconds =
            Math.floor(
                difference / 1000
            );


        const days =
            Math.floor(
                totalSeconds / 86400
            );


        const hours =
            Math.floor(
                (totalSeconds % 86400)
                / 3600
            );


        const minutes =
            Math.floor(
                (totalSeconds % 3600)
                / 60
            );


        const seconds =
            totalSeconds % 60;


        document
            .getElementById(
                "timer"
            )
            .textContent =
            `${days}d ${hours}h ${minutes}m ${seconds}s`;

    }


    updateTimer();

    setInterval(
        updateTimer,
        1000
    );

}


/* =========================================================
   SAVE SECRET
========================================================= */

function saveSecret() {

    const input =
        document
            .getElementById(
                "secretInput"
            );


    const message =
        input.value.trim();


    if (!message) {

        notify(
            "Write something first ♡"
        );

        return;
    }


    world.secrets.push({

        id:
            Date.now(),

        message:
            message,

        opened:
            false,

        created:
            new Date().toISOString()

    });


    saveWorld();


    input.value = "";


    notify(
        "Your secret message is hidden ♡"
    );

}


/* =========================================================
   OPEN SECRET
========================================================= */

function openSecret() {

    if (
        !world ||
        world.secrets.length === 0
    ) {

        showSecret(
            "There isn't a secret message here yet. ♡"
        );

        return;
    }


    const secret =
        world.secrets.find(
            item =>
                !item.opened
        );


    if (!secret) {

        showSecret(
            "All the secret messages here have already been opened. ♡"
        );

        return;
    }


    secret.opened =
        true;


    saveWorld();


    showSecret(
        secret.message
    );


    notify(
        "Secret message opened ♡"
    );

}


/* =========================================================
   SHOW SECRET
========================================================= */

function showSecret(message) {

    const box =
        document
            .getElementById(
                "secretBox"
            );


    box.textContent =
        message;


    box.classList.add(
        "show"
    );

}


/* =========================================================
   SAVE MEMORY
========================================================= */

function saveMemory() {

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


    if (!title || !text) {

        notify(
            "Add a title and memory first ♡"
        );

        return;
    }


    world.memories.unshift({

        id:
            Date.now(),

        title:
            title,

        text:
            text,

        created:
            new Date().toISOString()

    });


    saveWorld();


    document
        .getElementById(
            "memoryTitle"
        )
        .value = "";


    document
        .getElementById(
            "memoryText"
        )
        .value = "";


    renderMemories();


    notify(
        "Memory saved ♡"
    );

}


/* =========================================================
   RENDER MEMORIES
========================================================= */

function renderMemories() {

    const container =
        document
            .getElementById(
                "memories"
            );


    container.innerHTML = "";


    if (
        !world ||
        world.memories.length === 0
    ) {

        container.innerHTML =
            `
            <div class="empty">
                Your first memory is waiting to be written. ♡
            </div>
            `;

        return;
    }


    world.memories.forEach(
        memory => {

            const div =
                document.createElement(
                    "div"
                );


            div.className =
                "memory";


            const date =
                new Date(
                    memory.created
                ).toLocaleString();


            div.innerHTML = `

                <h3>
                    ${escapeHTML(
                        memory.title
                    )}
                </h3>

                <p>
                    ${escapeHTML(
                        memory.text
                    )}
                </p>

                <div class="memory-date">
                    ${date}
                </div>

            `;


            container.appendChild(
                div
            );

        }
    );

}


/* =========================================================
   COPY LINK
========================================================= */

async function copyWorldLink() {

    const url =
        new URL(
            window.location.href
        );


    url.searchParams.set(
        "world",
        world.id
    );


    try {

        await navigator.clipboard.writeText(
            url.toString()
        );


        notify(
            "World link copied ♡"
        );


    } catch {

        notify(
            "Copy the link shown above."
        );

    }

}


/* =========================================================
   CHANGE NAME
========================================================= */

function changeUniverseName() {

    const name =
        prompt(
            "What would you like to call your universe?",
            world.name
        );


    if (!name)
        return;


    world.name =
        name.trim();


    saveWorld();


    document
        .getElementById(
            "worldTitle"
        )
        .textContent =
        world.name + " ♡";


    notify(
        "Universe name changed ♡"
    );

}


/* =========================================================
   RESET
========================================================= */

function clearLocalWorld() {

    const confirmation =
        confirm(
            "This will remove this universe from this browser. Continue?"
        );


    if (!confirmation)
        return;


    localStorage.removeItem(
        "ourUniverseWorld"
    );


    location.href =
        location.pathname;

}


/* =========================================================
   NOTIFICATION
========================================================= */

function notify(message) {

    const notification =
        document
            .getElementById(
                "notification"
            );


    notification.textContent =
        message;


    notification.classList.add(
        "show"
    );


    setTimeout(
        () => {

            notification.classList.remove(
                "show"
            );

        },
        2500
    );

}


/* =========================================================
   SECURITY
========================================================= */

function escapeHTML(text) {

    const element =
        document.createElement(
            "div"
        );


    element.textContent =
        text;


    return element.innerHTML;

}


/* =========================================================
   STARS
========================================================= */

const starContainer =
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
        Math.random() * 3 + "s";


    star.style.animationDuration =
        (
            2 +
            Math.random() * 4
        ) + "s";


    starContainer.appendChild(
        star
    );

}


/* =========================================================
   START
========================================================= */

loadWorld();

</script>

</body>
</html>
