<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#160d2b">

<title>Our Little Universe ♡</title>

<style>
* {
    box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    min-height: 100vh;
    font-family: Georgia, "Times New Roman", serif;
    color: #fff;
    background:
        radial-gradient(circle at 20% 10%, rgba(255,180,210,.18), transparent 28%),
        radial-gradient(circle at 85% 25%, rgba(120,150,255,.16), transparent 30%),
        radial-gradient(circle at 50% 90%, rgba(180,100,255,.15), transparent 30%),
        linear-gradient(145deg, #08040f, #160b27 45%, #090513);
    overflow-x: hidden;
}

/* STARS */

#stars {
    position: fixed;
    inset: 0;
    z-index: -1;
    pointer-events: none;
}

.star {
    position: absolute;
    width: 3px;
    height: 3px;
    border-radius: 50%;
    background: white;
    opacity: .4;
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

/* MAIN */

.container {
    width: min(900px, 92%);
    margin: auto;
    padding-bottom: 70px;
}

.hero {
    text-align: center;
    padding: 70px 10px 35px;
}

.moon {
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
    font-size: 1.1rem;
    opacity: .75;
}

/* CARDS */

.card {
    margin: 22px 0;
    padding: 28px;
    border-radius: 28px;
    background: rgba(255,255,255,.075);
    border: 1px solid rgba(255,255,255,.14);
    box-shadow: 0 20px 60px rgba(0,0,0,.25);
    backdrop-filter: blur(16px);
}

.card h2 {
    margin-top: 0;
    font-size: 1.7rem;
}

/* TIMER */

.timer {
    text-align: center;
}

.timer-big {
    font-size: clamp(2rem, 9vw, 4.5rem);
    font-weight: bold;
    margin: 20px 0 5px;
}

.timer-small {
    opacity: .65;
}

.timer-date {
    margin-top: 20px;
    opacity: .7;
}

/* BUTTONS */

button {
    border: none;
    border-radius: 999px;
    padding: 13px 21px;
    margin: 5px;
    font-family: inherit;
    font-size: 1rem;
    cursor: pointer;
    background: rgba(255,255,255,.95);
    color: #251132;
    transition: transform .2s, box-shadow .2s;
}

button:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(255,255,255,.12);
}

button:active {
    transform: scale(.96);
}

.primary {
    background: linear-gradient(135deg, #fff, #e9dfff);
}

/* INPUTS */

input,
textarea {
    width: 100%;
    border: 1px solid rgba(255,255,255,.15);
    border-radius: 17px;
    background: rgba(0,0,0,.25);
    color: white;
    padding: 15px;
    font-family: inherit;
    font-size: 1rem;
    outline: none;
}

input:focus,
textarea:focus {
    border-color: rgba(255,255,255,.45);
}

textarea {
    min-height: 140px;
    resize: vertical;
}

/* SECRET */

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

/* MEMORY */

.memory {
    margin-top: 15px;
    padding: 20px;
    border-radius: 20px;
    background: rgba(255,255,255,.055);
    border: 1px solid rgba(255,255,255,.08);
}

.memory-date {
    opacity: .5;
    font-size: .85rem;
    margin-top: 10px;
}

/* HEART */

.heart {
    display: inline-block;
    animation: heartbeat 1.6s infinite;
}

@keyframes heartbeat {
    0%,100% {
        transform: scale(1);
    }
    15% {
        transform: scale(1.2);
    }
    30% {
        transform: scale(1);
    }
}

/* WORLD ID */

.world-link {
    word-break: break-all;
    padding: 15px;
    border-radius: 15px;
    background: rgba(0,0,0,.25);
    font-size: .85rem;
    opacity: .8;
}

/* SETUP */

.setup {
    text-align: center;
}

.setup input {
    margin-bottom: 10px;
}

.small {
    font-size: .85rem;
    opacity: .6;
    line-height: 1.6;
}

/* NOTIFICATION */

.notification {
    position: fixed;
    left: 50%;
    bottom: 25px;
    transform: translateX(-50%) translateY(100px);
    padding: 14px 22px;
    border-radius: 999px;
    background: rgba(20,10,35,.95);
    border: 1px solid rgba(255,255,255,.15);
    transition: .35s;
    z-index: 50;
    opacity: 0;
}

.notification.show {
    transform: translateX(-50%) translateY(0);
    opacity: 1;
}

/* EMPTY */

.empty {
    text-align: center;
    opacity: .55;
    padding: 20px;
}

/* FOOTER */

footer {
    text-align: center;
    opacity: .45;
    padding: 30px;
    font-size: .9rem;
}
</style>
</head>

<body>

<div id="stars"></div>

<div class="container">

    <!-- HERO -->

    <section class="hero">

        <div class="moon">🌙</div>

        <h1>Our Little Universe</h1>

        <p>
            One little world that belongs to two people.
        </p>

        <div>
            <span class="heart">♡</span>
        </div>

    </section>


    <!-- SETUP -->

    <section class="card setup" id="setupSection">

        <h2>🌌 Create Your Universe</h2>

        <p>
            Give your little universe a name and choose
            the moment your story began.
        </p>

        <input
            id="universeName"
            placeholder="Our Little Universe"
        >

        <input
            id="startDate"
            type="datetime-local"
        >

        <button
            class="primary"
            onclick="createUniverse()"
        >
            Create Our World ♡
        </button>

        <p class="small">
            Your world is saved in this browser.
        </p>

    </section>


    <!-- APP -->

    <div id="app" style="display:none;">

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


        <!-- SECRET MESSAGE -->

        <section class="card secret">

            <h2>💌 A Secret Message</h2>

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

            <h2>💗 Leave Something For Me</h2>

            <p class="small">
                Write something you want your person to find.
                It will stay hidden until they choose to open it.
            </p>

            <textarea
                id="secretInput"
                placeholder="Write something from your heart..."
            ></textarea>

            <button
                class="primary"
                onclick="saveSecret()"
            >
                Hide My Message ♡
            </button>

        </section>


        <!-- MEMORIES -->

        <section class="card">

            <h2>📖 Our Memories</h2>

            <input
                id="memoryTitle"
                placeholder="Memory title"
            >

            <textarea
                id="memoryText"
                placeholder="Write about this moment..."
            ></textarea>

            <button onclick="saveMemory()">
                Add Memory ♡
            </button>

            <div id="memories"></div>

        </section>


        <!-- WORLD LINK -->

        <section class="card">

            <h2>🔗 Our World Link</h2>

            <p class="small">
                This is the link to this particular universe.
                Share it with your person.
            </p>

            <div
                id="worldLink"
                class="world-link"
            ></div>

            <button onclick="copyWorldLink()">
                Copy Link
            </button>

        </section>


        <!-- RESET -->

        <section class="card">

            <h2>🌙 Universe Settings</h2>

            <button onclick="changeUniverseName()">
                Change Universe Name
            </button>

            <button onclick="clearLocalWorld()">
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
   WORLD STORAGE
   ========================================================= */

let world = null;


/* =========================================================
   CREATE RANDOM WORLD ID
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
   GET WORLD ID FROM URL
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

    const urlWorld =
        getWorldIdFromURL();

    const savedWorld =
        localStorage.getItem("ourUniverseWorld");

    if (savedWorld) {

        const parsed =
            JSON.parse(savedWorld);

        /*
        If the URL contains a world ID,
        make sure this browser is opening
        that particular world.
        */

        if (
            !urlWorld ||
            parsed.id === urlWorld
        ) {

            world = parsed;

            showApp();

            return;
        }
    }

    /*
    If there is no existing world,
    show setup.
    */

    document.getElementById("setupSection")
        .style.display = "block";
}


/* =========================================================
   CREATE WORLD
   ========================================================= */

function createUniverse() {

    const name =
        document.getElementById("universeName")
            .value.trim()
        || "Our Little Universe";

    const date =
        document.getElementById("startDate")
            .value;

    if (!date) {

        notify(
            "Choose the date your story began ♡"
        );

        return;
    }

    world = {

        id: generateWorldId(),

        name: name,

        startDate:
            new Date(date).toISOString(),

        secrets: [],

        memories: []

    };

    saveWorld();

    /*
    Add the world ID to the link.
    */

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

    document.getElementById("setupSection")
        .style.display = "none";

    document.getElementById("app")
        .style.display = "block";

    document.getElementById("worldTitle")
        .textContent =
        world.name + " ♡";

    document.getElementById("startDateDisplay")
        .textContent =
        "Since " +
        new Date(world.startDate)
            .toLocaleString();

    const shareURL =
        new URL(
            window.location.href
        );

    shareURL.searchParams.set(
        "world",
        world.id
    );

    document.getElementById("worldLink")
        .textContent =
        shareURL.toString();

    renderMemories();

    startTimer();
}


/* =========================================================
   TIMER
   ========================================================= */

function startTimer() {

    function update() {

        if (!world) return;

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
                (totalSeconds % 86400) / 3600
            );

        const minutes =
            Math.floor(
                (totalSeconds % 3600) / 60
            );

        const seconds =
            totalSeconds % 60;

        document.getElementById("timer")
            .textContent =
            `${days}d ${hours}h ${minutes}m ${seconds}s`;
    }

    update();

    setInterval(
        update,
        1000
    );
}


/* =========================================================
   SAVE SECRET
   ========================================================= */

function saveSecret() {

    const input =
        document.getElementById("secretInput");

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

    /*
    Find the first unopened message.
    */

    const secret =
        world.secrets.find(
            item => !item.opened
        );

    if (!secret) {

        showSecret(
            "All the secret messages here have already been opened. ♡"
        );

        return;
    }

    secret.opened = true;

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
        document.getElementById("secretBox");

    box.textContent =
        message;

    box.classList.add("show");
}


/* =========================================================
   SAVE MEMORY
   ========================================================= */

function saveMemory() {

    const title =
        document.getElementById("memoryTitle")
            .value.trim();

    const text =
        document.getElementById("memoryText")
            .value.trim();

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

    document.getElementById("memoryTitle")
        .value = "";

    document.getElementById("memoryText")
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
        document.getElementById("memories");

    container.innerHTML = "";

    if (
        !world ||
        world.memories.length === 0
    ) {

        container.innerHTML =
            `<div class="empty">
                Your first memory is waiting to be written. ♡
            </div>`;

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
                <h3>${escapeHTML(memory.title)}</h3>
                <p>${escapeHTML(memory.text)}</p>
                <div class="memory-date">
                    ${date}
                </div>
            `;

            container.appendChild(div);
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

    document.getElementById("worldTitle")
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
        document.getElementById(
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
        document.createElement("div");

    element.textContent =
        text;

    return element.innerHTML;
}


/* =========================================================
   GENERATE STARS
   ========================================================= */

const starContainer =
    document.getElementById("stars");

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
        (2 + Math.random() * 4) + "s";

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
