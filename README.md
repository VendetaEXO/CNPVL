
<html lang="ro">

<head>

    <meta charset="UTF-8">
    <title>Colegiul Național Pedagogic „Vasile Lupu” Iași</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
.navbar {
    transition: top 0.4s cubic-bezier(.4,0,.2,1), opacity 0.3s;
}
.navbar.hide-navbar {
    top: -70px;
    opacity: 0;
    pointer-events: none;
}
.navbar.show-navbar {
    top: 0;
    opacity: 1;
    pointer-events: auto;
}
.navbar:hover {
    top: 0 !important;
    opacity: 1 !important;
    pointer-events: auto !important;
}

body {
    padding-top: 60px;
}

        :root {
            --main-bg: linear-gradient(120deg, #181818 0%, #232526 100%);
            --main-border: #888;
            --main-radius: 18px;
            --container-bg: rgba(24, 24, 24, 0.98);
            --container-radius: 14px;
            --accent: #f3c623;
            --accent2: #3e8ed0;
            --accent3: #e94560;
            --text-main: #f3f3f3;
            --text-muted: #bdbdbd;
            --shadow: 0 8px 32px #000b, 0 2px 0 #444 inset;
        }

        html, body {
            height: 100%;
        }
        body {
            background: var(--main-bg);
            margin: 0;
            min-height: 100vh;
            font-family: 'Segoe UI', Arial, sans-serif;
        }

        .navbar {
            width: 100%;
            background: #232526e6;
            box-shadow: 0 2px 12px #0006;
            padding: 0.5em 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .navbar ul {
            display: flex;
            justify-content: center;
            gap: 2em;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        .navbar a {
            color: var(--text-main);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1em;
            padding: 0.5em 1em;
            border-radius: 8px;
            transition: background 0.2s;
        }

        .navbar a:hover, .navbar a.active {
            background: var(--accent2);
            color: #fff;
        }

        .border-frame {
            border: 1.5px solid var(--main-border);
            border-radius: var(--main-radius);
            margin: 18px auto 0 auto;
            max-width: 98vw;
            padding: 0;
            background: transparent;
            box-shadow: 0 2px 16px #0004;
        }

        .container {
            background: var(--container-bg);
            border-radius: var(--container-radius);
            margin: 0 auto;
            max-width: 1200px;
            padding: 38px 36px 30px 36px;
            color: var(--text-main);
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: "";
            position: absolute;
            inset: 0;
            border-radius: var(--container-radius);
            pointer-events: none;
            box-shadow: 0 0 0 6px #23252655 inset;
        }

        h1 {
            margin-top: 0;
            font-size: 2.3rem;
            color: #fafafa;
            letter-spacing: 1.5px;
            font-weight: 700;
            text-shadow: 0 2px 10px #0007;
            text-align: center;
        }

        h2 {
            margin-top: 0.5em;
            font-size: 1.18rem;
            font-weight: 400;
            color: var(--text-muted);
            letter-spacing: 0.5px;
            margin-bottom: 1.7em;
            text-align: center;
        }

        .morph-img {
            display: block;
            width: 100%;
            max-width: 420px;
            margin: 0 auto 2em auto;
            border-radius: 60% 40% 40% 60% / 50% 60% 40% 50%;
            transition: border-radius 1.2s cubic-bezier(.68,-0.55,.27,1.55), box-shadow 0.6s;
            box-shadow: 0 6px 36px #000a, 0 0 0 5px #444a;
            border: 2.5px solid #5a5a5a;
            background: #222;
        }

        .morph-img:hover {
            border-radius: 0% 100% 0% 100% / 0% 100% 0% 100%;
            box-shadow: 0 12px 48px #000c, 0 0 0 8px #444a;
        }

        .section {
            margin: 2.5em 0 2em 0;
            padding: 1.5em 1em;
            background: #232526cc;
            border-radius: 12px;
            box-shadow: 0 2px 12px #0003;
        }

        .section-title {
            color: var(--accent2);
            font-size: 1.3em;
            margin-bottom: 0.7em;
            text-align: center;
            letter-spacing: 1px;
        }

        .prof-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5em;
            justify-content: center;
            margin: 1em 0 0 0;
        }

        .prof-card {
            background: #181818e6;
            border-radius: 10px;
            box-shadow: 0 2px 8px #0005;
            padding: 1em 1.2em;
            min-width: 160px;
            max-width: 200px;
            text-align: center;
            color: #e0e0e0;
            transition: transform 0.2s;
        }

        .prof-card:hover {
            transform: translateY(-6px) scale(1.04);
            box-shadow: 0 8px 24px #0007;
        }

        .prof-card .prof-name {
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 0.3em;
        }

        .prof-card .prof-role {
            font-size: 0.98em;
            color: var(--accent2);
        }

        .timeline {
            border-left: 3px solid var(--accent3);
            margin: 1.5em 0 0 1.5em;
            padding-left: 1.5em;
        }

        .timeline-event {
            margin-bottom: 1.2em;
            position: relative;
        }

        .timeline-event::before {
            content: "";
            position: absolute;
            left: -1.7em;
            top: 0.2em;
            width: 1em;
            height: 1em;
            background: var(--accent3);
            border-radius: 50%;
            box-shadow: 0 2px 8px #0006;
        }

        .timeline-year {
            font-weight: bold;
            color: var(--accent3);
        }

        .timeline-desc {
            color: #e0e0e0;
            margin-left: 0.2em;
        }

        /* Amintiri */
        .memories-section {
            margin: 2.5em 0 2em 0;
            padding: 1.5em 1em;
            background: #181818e6;
            border-radius: 14px;
            box-shadow: 0 2px 12px #0003;
        }

        .memories-title {
            color: var(--accent);
            font-size: 1.3em;
            margin-bottom: 1.2em;
            text-align: center;
            letter-spacing: 1px;
        }

        .memories-carousel {
            display: flex;
            overflow-x: auto;
            gap: 2em;
            padding-bottom: 1em;
            scroll-snap-type: x mandatory;
        }

        .memory-card {
            background: #232526cc;
            border-radius: 12px;
            box-shadow: 0 2px 12px #0003;
            min-width: 320px;
            max-width: 340px;
            flex: 0 0 auto;
            padding: 1em;
            margin-bottom: 1em;
            scroll-snap-align: start;
            display: flex;
            flex-direction: column;
            align-items: center;
            transition: transform 0.2s;
        }

        .memory-card:hover {
            transform: scale(1.03) rotate(-1deg);
            box-shadow: 0 8px 24px #0007;
        }

        .memory-img {
            width: 100%;
            max-width: 300px;
            border-radius: 10px;
            margin-bottom: 1em;
            box-shadow: 0 2px 12px #0005;
        }

        .memory-text {
            color: #e0e0e0;
            font-size: 1.05em;
            text-align: center;
        }

        .farewell-section {
            margin: 2.5em 0 2em 0;
            padding: 1.5em 1em;
            background: #232526cc;
            border-radius: 14px;
            box-shadow: 0 2px 12px #0003;
        }

        .farewell-title {
            color: var(--accent3);
            font-size: 1.3em;
            margin-bottom: 1.2em;
            text-align: center;
            letter-spacing: 1px;
        }

        .farewell-list {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5em;
            justify-content: center;
        }

        .farewell-card {
            background: #181818e6;
            border-radius: 12px;
            box-shadow: 0 2px 12px #0005;
            min-width: 220px;
            max-width: 300px;
            padding: 1.2em 1em;
            margin-bottom: 1em;
            text-align: center;
            color: #f3f3f3;
            border: 1.5px solid var(--accent3);
            transition: box-shadow 0.2s, border 0.2s;
        }

        .farewell-card:hover {
            box-shadow: 0 8px 24px #e9456080;
            border: 2.5px solid var(--accent3);
        }

        .farewell-card .farewell-name {
            font-weight: 700;
            color: var(--accent3);
            margin-bottom: 0.3em;
            font-size: 1.1em;
        }

        .farewell-card .farewell-message {
            font-size: 1em;
            color: #e0e0e0;
        }

        .comments-section {
            margin-top: 2.5em;
            background: #232526cc;
            border-radius: 12px;
            box-shadow: 0 2px 12px #0003;
            padding: 1.5em 1em;
        }

        .comments-title {
            color: var(--accent2);
            font-size: 1.2em;
            margin-bottom: 1em;
            text-align: center;
        }

        .comment-form {
            display: flex;
            flex-direction: column;
            gap: 0.7em;
            margin-bottom: 1.5em;
        }

        .comment-form input, .comment-form textarea {
            background: #181818;
            border: 1px solid #444;
            color: #f3f3f3;
            border-radius: 7px;
            padding: 0.7em;
            font-size: 1em;
            resize: none;
        }

        .comment-form button {
            background: var(--accent2);
            color: #fff;
            border: none;
            border-radius: 7px;
            padding: 0.7em 1.2em;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.2s;
        }

        .comment-form button:hover {
            background: var(--accent3);
        }

        .comment-list {
            margin: 0;
            padding: 0;
            list-style: none;
        }

        .comment-item {
            background: #181818e6;
            border-radius: 8px;
            margin-bottom: 1em;
            padding: 1em 1em 0.7em 1em;
            box-shadow: 0 2px 8px #0003;
            position: relative;
        }

        .comment-user {
            font-weight: 600;
            color: var(--accent);
        }

        .comment-date {
            font-size: 0.9em;
            color: #aaa;
            float: right;
        }

        .comment-text {
            margin: 0.7em 0 0 0;
            color: #e0e0e0;
            white-space: pre-line;
        }

        .feedback-section {
            margin: 2.5em 0 2em 0;
            padding: 1.5em 1em;
            background: #181818e6;
            border-radius: 14px;
            box-shadow: 0 2px 12px #0003;
        }

        .feedback-title {
            color: var(--accent);
            font-size: 1.2em;
            margin-bottom: 1em;
            text-align: center;
        }

        .feedback-form {
            display: flex;
            flex-direction: column;
            gap: 0.7em;
            align-items: center;
            margin-bottom: 1.5em;
        }

        .stars {
            display: flex;
            gap: 0.3em;
            font-size: 2em;
            cursor: pointer;
        }

        .star {
            color: #444;
            transition: color 0.2s;
        }

        .star.selected,
        .star:hover,
        .star:hover ~ .star {
            color: var(--accent);
        }

        .feedback-form textarea {
            width: 100%;
            max-width: 400px;
            min-width: 200px;
            min-height: 60px;
        }

        .feedback-form button {
            background: var(--accent2);
            color: #fff;
            border: none;
            border-radius: 7px;
            padding: 0.7em 1.2em;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.2s;
        }

        .feedback-form button:hover {
            background: var(--accent3);
        }

        .feedback-list {
            margin: 0;
            padding: 0;
            list-style: none;
        }

        .feedback-item {
            background: #232526cc;
            border-radius: 8px;
            margin-bottom: 1em;
            padding: 1em 1em 0.7em 1em;
            box-shadow: 0 2px 8px #0003;
            position: relative;
        }

        .feedback-stars {
            color: var(--accent);
            font-size: 1.1em;
        }

        .feedback-date {
            font-size: 0.9em;
            color: #aaa;
            float: right;
        }

        .feedback-text {
            margin: 0.7em 0 0 0;
            color: #e0e0e0;
            white-space: pre-line;
        }

        .footer {
            margin-top: 2.5em;
            text-align: center;
            color: #888;
            font-size: 1.05rem;
            letter-spacing: 0.2px;
            padding-bottom: 1.5em;
        }

        @media (max-width: 1200px) {
            .container {
                max-width: 98vw;
            }
        }

        @media (max-width: 900px) {
            .border-frame, .container {
                max-width: 99vw;
            }
            .memory-card, .farewell-card {
                min-width: 220px;
                max-width: 98vw;
            }
        }

        @media (max-width: 700px) {
            .container {
                padding: 14px 2vw 14px 2vw;
                max-width: 99vw;
            }
            .morph-img {
                max-width: 98vw;
            }
            .prof-list, .farewell-list {
                flex-direction: column;
                align-items: center;
            }
            .memories-carousel {
                gap: 1em;
            }
        }


    </style>

</head>

<body>

<nav class="navbar animated-navbar" id="mainNavbar">
    <ul>
        <li><a href="#" class="active">Acasă</a></li>
        <li><a href="#istoric">Istoric</a></li>
        <li><a href="#profesori">Profesori</a></li>
        <li><a href="#amintiri">Amintiri</a></li>
        <li><a href="#farewell">Comentarii de la colegi</a></li>
        <li><a href="#comentarii">Comentarii</a></li>
        <li><a href="#feedback">Feedback</a></li>
    </ul>
</nav>
    <div class="border-frame">
        <div class="container">
            <h1>Colegiul Național Pedagogic „Vasile Lupu” Iași</h1>
            <h2>O scoala de proveste</h2>
            <img 
                src="Colegiul-pedagogic-iasi-foto-primaria-iasi.jpg" 
                alt="Colegiul Național Pedagogic Vasile Lupu Iași" 
                class="morph-img hoverzoom"
                style="margin: 0 auto;"
            >
            <div class="section" id="prezentare">
    <div class="section-title">Prezentare generală</div>
    <p>
        Colegiul Național Pedagogic „Vasile Lupu” din Iași reprezintă un veritabil pilon al educației românești, fiind recunoscut pentru tradiția, profesionalismul și rezultatele sale remarcabile. Fondat în secolul al XIX-lea, colegiul a evoluat constant, adaptându-se cerințelor societății moderne și promovând valori fundamentale precum respectul, responsabilitatea și excelența academică.<br><br>
        Instituția oferă un mediu educațional stimulativ, în care elevii sunt încurajați să-și dezvolte atât competențele intelectuale, cât și abilitățile sociale și civice. Programele școlare sunt concepute pentru a răspunde nevoilor diverse ale elevilor, punând accent pe formarea gândirii critice, creativității și spiritului de inițiativă.<br><br>
        Cadrele didactice, cu o vastă experiență și o pregătire de excepție, se implică activ în procesul instructiv-educativ, oferind sprijin individualizat și promovând metode moderne de predare. Relația profesor-elev este una deschisă, bazată pe dialog, încredere și colaborare.<br><br>
        Colegiul dispune de laboratoare moderne, bibliotecă bogată, săli multimedia și facilități sportive, toate menite să susțină dezvoltarea armonioasă a elevilor. Activitățile extracurriculare, precum cluburile de lectură, atelierele de robotică, proiectele de voluntariat și schimburile internaționale, completează formarea tinerilor și le oferă oportunități de afirmare.<br><br>
        De-a lungul timpului, instituția a format generații de profesori, pedagogi și specialiști care s-au remarcat prin profesionalism și implicare în comunitate. Absolvenții colegiului sunt apreciați atât în țară, cât și în străinătate, pentru competențele dobândite și pentru valorile morale solide.<br><br>
        Colegiul Național Pedagogic „Vasile Lupu” promovează egalitatea de șanse, diversitatea și incluziunea, asigurând un climat sigur și prietenos pentru toți elevii. Prin parteneriate cu instituții de prestigiu, universități și organizații non-guvernamentale, colegiul oferă acces la resurse educaționale de calitate și la experiențe formative relevante.<br><br>
        Rezultatele obținute la olimpiade, concursuri și examene naționale reflectă nivelul ridicat de pregătire al elevilor și dedicarea profesorilor. Instituția se implică activ în viața comunității, organizând evenimente culturale, acțiuni caritabile și campanii de informare.<br><br>
        Misiunea colegiului este de a forma tineri autonomi, responsabili și creativi, capabili să se adapteze provocărilor societății contemporane și să contribuie la dezvoltarea acesteia. Valorile fundamentale care ghidează activitatea școlii sunt respectul față de tradiție, deschiderea către inovație și promovarea excelenței.<br><br>
        Colegiul Național Pedagogic „Vasile Lupu” rămâne un reper al educației ieșene, un spațiu al performanței, al prieteniei și al dezvoltării personale. Fiecare generație de elevi adaugă o nouă filă în istoria bogată a instituției, ducând mai departe prestigiul și valorile acesteia.<br><br>
        Prin implicarea activă a tuturor membrilor comunității școlare, colegiul își propune să ofere fiecărui elev șansa de a-și descoperi și valorifica potențialul, pregătindu-l pentru succesul academic, profesional și personal.
    </p>
</div>
           <div class="section" id="istoric">
    <div class="section-title">Istoric</div>
    <div class="timeline">
        <div class="timeline-event">
            <span class="timeline-year">1855</span>
            <span class="timeline-desc">- Fondarea Școlii Normale „Vasile Lupu”.</span>
            <div style="color:#bdbdbd; font-size:0.98em; margin-top:0.3em;">
                În contextul dezvoltării sistemului educațional românesc, a fost înființată instituția cu scopul de a pregăti viitori învățători și profesori dedicați.
            </div>
        </div>
        <div class="timeline-event">
            <span class="timeline-year">1891</span>
            <span class="timeline-desc">- Inaugurarea clădirii actuale, simbol al educației ieșene.</span>
            <div style="color:#bdbdbd; font-size:0.98em; margin-top:0.3em;">
                Clădirea emblematică a fost construită pentru a oferi un spațiu modern și adecvat procesului instructiv-educativ, devenind un reper arhitectural și cultural.
            </div>
        </div>
        <div class="timeline-event">
            <span class="timeline-year">1948</span>
            <span class="timeline-desc">- Transformarea în liceu pedagogic.</span>
            <div style="color:#bdbdbd; font-size:0.98em; margin-top:0.3em;">
                Reforma educațională a determinat adaptarea curriculei și extinderea specializărilor, consolidând rolul instituției în formarea cadrelor didactice.
            </div>
        </div>
        <div class="timeline-event">
            <span class="timeline-year">2000</span>
            <span class="timeline-desc">- Dobândirea statutului de colegiu național pedagogic.</span>
            <div style="color:#bdbdbd; font-size:0.98em; margin-top:0.3em;">
                Recunoașterea performanțelor academice și a tradiției a condus la acordarea titlului de colegiu național, marcând o nouă etapă de excelență.
            </div>
        </div>
        <div class="timeline-event">
            <span class="timeline-year">2020+</span>
            <span class="timeline-desc">- Modernizare continuă și rezultate remarcabile la nivel național și internațional.</span>
            <div style="color:#bdbdbd; font-size:0.98em; margin-top:0.3em;">
                Instituția investește constant în infrastructură, tehnologie și dezvoltarea profesională a cadrelor, obținând premii și recunoaștere la concursuri și olimpiade.
            </div>
        </div>
    </div>
</div>


            <div class="section" id="profesori">
                <div class="section-title">Profesori de prestigiu</div>
                <div class="prof-list">
                    <div class="prof-card">
                        <div class="prof-name">Prof. Elena Manuca</div>
                        <div class="prof-role">Limba și literatura română</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Laura Stanciu</div>
                        <div class="prof-role">Matematică</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Toderica Luminita</div>
                        <div class="prof-role">Fizica</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Adumitroai Marius</div>
                        <div class="prof-role">Istorie</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Lazarescu Ada</div>
                        <div class="prof-role">Biologie</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Hristodor Claudia</div>
                        <div class="prof-role">Chimie</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Coman Dana</div>
                        <div class="prof-role">Geografie</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Durac Nicoleta</div>
                        <div class="prof-role">Ed. fizica</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Pauliuc Mihai</div>
                        <div class="prof-role">Matematica(optional)</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Rusu Liliana</div>
                        <div class="prof-role">L. franceza</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Barsan Sorina</div>
                        <div class="prof-role">Ed. plastica</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Argeanu Claudia</div>
                        <div class="prof-role">Matematica plus</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Boroda Simona</div>
                        <div class="prof-role">Ed. muzicala</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Gavrilas Roxana</div>
                        <div class="prof-role">L. engleza</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Iacob Magda</div>
                        <div class="prof-role">Ed. sociala</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Cret Daniela</div>
                        <div class="prof-role">Informatică</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Prof. Mariana Busuioc</div>
                        <div class="prof-role">Ed. tehnoogica</div>
                    </div>
                    <div class="prof-card">
                        <div class="prof-name">Si multi alti profesori</div>
                        <div class="prof-role">Carora le suntem recunoscatori</div>
            </div>


<div class="memories-section" id="amintiri">
    <div class="memories-title">Amintiri de neuitat</div>
    <div class="memories-carousel" id="memoriesCarousel" style="background:#111; border-radius:12px; padding:1em 0;">
        <div class="memory-card">
            <img src="Poza-Bibleoteca.jpg" class="memory-img" alt="Excursie la munte">
            <div class="memory-text">Vizita Bibliotecii "Mihai Eminescu"</div>
        </div>
        <div class="memory-card">
            <img src="Poza-Gradina.jpg" class="memory-img" alt="Balul bobocilor">
            <div class="memory-text">Gradina botanica</div>
        </div>
        <div class="memory-card">
            <img src="Poza-Pogor.jpg" class="memory-img" alt="Ultimul clopoțel">
            <div class="memory-text">Casa Pogor</div>
        </div>
        <div class="memory-card">
            <img src="Poza-Intalnire.jpg" class="memory-img" alt="">
            <div class="memory-text">Iesirea pentru a o vizita pe stranepoata lui Ion Creanga</div>
        </div>
    </div>
</div>

<style>

.memories-slider-controls {
    gap: 1.5em;
}

.memories-arrow {
    background: #111;
    color: #fff;
    border: 2px solid #444;
    border-radius: 50%;
    width: 2.5em;
    height: 2.5em;
    font-size: 1.5em;
    cursor: pointer;
    transition: background 0.2s, border 0.2s;
    margin: 0 0.5em;
    box-shadow: 0 2px 8px #0006;
}

.memories-arrow:hover {
    background: #232526;
    border: 2px solid var(--accent2);
}

.memories-carousel {
    display: flex;
    overflow: hidden;
    gap: 2em;
    scroll-behavior: smooth;
}

</style>

<div class="farewell-section" id="galerie-video">
    <div class="farewell-title">Galerie video – Evenimente și activități</div>
    <div class="farewell-list" style="flex-wrap: wrap;">
        <div class="farewell-card" style="max-width:420px;">
            <div class="farewell-name">Prezentarea scolii CNPVL</div>
            <div class="farewell-message">
                <iframe width="100%" height="215" src="https://www.youtube.com/embed/Dv5HePse6BU" title="Serbare" frameborder="0" allowfullscreen></iframe>
                <br>Un videoclip despre o scoala cu prestigiu
            </div>
        </div>
        <div class="farewell-card" style="max-width:420px;">
            <div class="farewell-name">Intoarcerea "acasa"</div>
            <div class="farewell-message">
                <iframe width="100%" height="215" src="https://www.youtube.com/embed/jH3hOT0tG-0" title="Excursie" frameborder="0" allowfullscreen></iframe>
                <br>Un moment important pentru elevi si profesori
            </div>
        </div>
    </div>
    <div style="text-align:center;margin-top:1em;">
        <button onclick="window.open('https://www.youtube.com/results?search_query=colegiul+vasile+lupu+iasi','_blank')" class="btn-accent">Vezi mai multe videoclipuri</button>
    </div>
</div>


<div class="farewell-section" id="premii">
    <div class="farewell-title">Premii obținute de-a lungul anilor</div>
    <div class="farewell-list">
        <div class="farewell-card">
            <div class="farewell-name">"Prolectura"</div>
            <div class="farewell-message">
                Diploma de gradul II (etapa internationala) – Henea Rares ; Premiul mare – Bumbes Alexia, Condrea Maya; Prof. coordonator Manuca Elena/Barsan Sorina<br>
                <button class="btn-accent" onclick="alert('In anul 2022, editia a 4-a')">Detalii</button>
            </div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">"Spune-mi o poveste pentru suflet, editia XVI,XVII,XX"</div>
            <div class="farewell-message">
                Premiul I – Henea Rares ; Prof. coordonator Elena Manuca ; "LuminaMath International" – Premiul III ; Prof. coordonator Laura Stanciu<br>
                <button class="btn-accent" onclick="alert('In anul 2021,2022')">Detalii</button>
            </div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Turneu de football</div>
            <div class="farewell-message">
                Match amical 3-2 – Thundiparambil Ashyln; Prof. coordonator Durac Nicoleta
                <button class="btn-accent" onclick="alert('In Anul 2024')">Detalii</button>
            </div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Olimpiada de Istorie</div>
            <div class="farewell-message">
                Mentiune – Citireag Andrei, Suhan David; Prof. coordonator Adumitroaei Marius<br>
                <button class="btn-accent" onclick="alert('Anul 2024 | Felicitări pentru pasiunea pentru istorie!')">Detalii</button>
            </div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">"European Money Quiz"</div>
            <div class="farewell-message">
                Permiul III – Azamfirei Mihai, Lungu Cristian; Prof. coordonator Argeanu Claudia
                <button class="btn-accent" onclick="alert('Anul 2025')">Detalii</button>
            </div>
      </div>
</div>

<div class="farewell-section" id="activitati">
    <div class="farewell-title">Activități extracurriculare</div>
    <div class="farewell-list">
        <div class="farewell-card">
            <div class="farewell-name">Clubul de lectură</div>
            <div class="farewell-message">Participă la întâlniri săptămânale și descoperă plăcerea lecturii alături de colegi pasionați.</div>
            <button class="btn-accent" onclick="alert('Mai multe detalii pe site-ul official al CNPVL')">Înscrie-te</button>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Atelier de programare</div>
            <div class="farewell-message">Construiește și programează siteuri, dezvoltând abilități in domeniul informaticii.</div>
            <button class="btn-accent" onclick="alert('Mai multe detalii pe site-ul official al CNPVL')">Înscrie-te</button>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Voluntariat</div>
            <div class="farewell-message">Implică-te în proiecte sociale și fă diferența în comunitatea ta.</div>
            <button class="btn-accent" onclick="alert('Mai multe detalii pe site-ul official al CNPVL')">Înscrie-te</button>
        </div>
    </div>
</div>

<div class="farewell-section" id="resurse">
    <div class="farewell-title">Resurse utile pentru elevi și părinți</div>
    <div class="farewell-list">
        <div class="farewell-card">
            <div class="farewell-name">Regulamentul școlar</div>
            <div class="farewell-message">Consultă <a href="#" style="color:var(--accent2);text-decoration:underline;">regulamentul intern</a> pentru a fi mereu informat.</div>
            <button class="btn-accent" onclick="window.open('https://edu.ro','_blank')">Descarcă PDF</button>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Calendarul anului școlar</div>
            <div class="farewell-message">Află datele importante ale anului școlar curent.</div>
            <button class="btn-accent" onclick="window.open('https://www.edu.ro/calendar-an-scolar','_blank')">Vezi calendar</button>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Contact secretariat</div>
            <div class="farewell-message">Pentru orice întrebare administrativă, contactează secretariatul colegiului.</div>
            <button class="btn-accent" onclick="window.location='mailto:secretariat@cnpvl-iasi.ro'">Trimite email</button>
        </div>
    </div>
</div>

<div class="farewell-section" id="testimoniale">
    <div class="farewell-title">Testimoniale de la premianti</div>
    <div class="farewell-list">
        <div class="farewell-card">
            <div class="farewell-name">Henea Rares</div>
            <div class="farewell-message">„Anii de gimnaziu la CNPVL au fost baza formării mele ca om și profesionist.”</div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Pintilie Ema</div>
            <div class="farewell-message">„Profesorii m-au inspirat să îmi urmez visurile. Mulțumesc!”</div>
        </div>
        <div class="farewell-card">
            <div class="farewell-name">Zamfir Silvia</div>
            <div class="farewell-message">„Recomand cu drag această școală tuturor celor care vor să crească frumos.”</div>
        </div>
    </div>
</div>


<style>
.btn-accent {
    background: var(--accent2);
    color: #fff;
    border: none;
    border-radius: 7px;
    padding: 0.6em 1.3em;
    font-size: 1em;
    font-weight: 600;
    margin-top: 1em;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
    box-shadow: 0 2px 8px #0003;
}

.btn-accent:hover {
    background: var(--accent3);
    transform: scale(1.06);
}

</style>
            <div class="farewell-section" id="farewell">
                <div class="farewell-title">Comentarii de final de clasa a VIII-a</div>
                <div class="farewell-list">
                    <div class="farewell-card">
                        <div class="farewell-name">Condrea Maya</div>
                        <div class="farewell-message">„Anii petrecuți aici mi-au oferit prieteni adevărați și amintiri de neuitat. Mulțumesc profesorilor pentru răbdare și inspirație!”</div>
                    </div>
                    <div class="farewell-card">
                        <div class="farewell-name">Sarghi Gabriel</div>
                        <div class="farewell-message">„Clasa a VIII-a a fost o aventură! Am învățat, am râs, am crescut. Succes tuturor pe mai departe!”</div>
                    </div>
                    <div class="farewell-card">
                        <div class="farewell-name">Neculau Alexia</div>
                        <div class="farewell-message">„Colegiul acesta va rămâne mereu în sufletul meu. La revedere, profesori minunați!”</div>
                    </div>
                    <div class="farewell-card">
                        <div class="farewell-name">Nedelcu Alex</div>
                        <div class="farewell-message">„Fiecare zi a fost o lecție, fiecare coleg un prieten. Drum bun, generație 2025!”</div>
                    </div>
                </div>
            </div>
<div class="comments-section" id="comentarii">
    <div class="comments-title">Comentarii vizitatori</div>
    <form class="comment-form" id="commentForm">
        <input type="text" id="username" placeholder="Nume (opțional)" maxlength="32">
        <textarea id="commentText" rows="3" placeholder="Scrie un comentariu..." required></textarea>
        <button type="submit">Trimite comentariul</button>
    </form>
    <ul class="comment-list" id="commentList"></ul>
</div>

<div class="feedback-section" id="feedback" style="margin-top: 1.5em;">
    <div class="feedback-title">Feedback vizitatori</div>
    <form class="feedback-form" id="feedbackForm">
        <div class="stars" id="starRating">
            <span class="star" data-value="1">&#9733;</span>
            <span class="star" data-value="2">&#9733;</span>
            <span class="star" data-value="3">&#9733;</span>
            <span class="star" data-value="4">&#9733;</span>
            <span class="star" data-value="5">&#9733;</span>
        </div>
        <textarea id="feedbackText" rows="3" placeholder="Lasă-ne un feedback..." required></textarea>
        <button type="submit">Trimite feedback</button>
    </form>
    <ul class="feedback-list" id="feedbackList"></ul>
</div>

<div class="footer" style="margin-top: 1.5em;">
    &copy; 2025 Colegiul Național Pedagogic „Vasile Lupu” Iași.<br>
    Toate drepturile rezervate.<br>
    <span style="font-size:0.95em;color:#aaa;">Site realizat de H. Rareș | Contact: henearares1@gmail.com</span>
</div>
        </div>
    </div>
<style>
.btn-accent {
    background: var(--accent2);
    color: #fff;
    border: none;
    border-radius: 7px;
    padding: 0.6em 1.3em;
    font-size: 1em;
    font-weight: 600;
    margin-top: 1em;
    cursor: pointer;
    transition: background 0.2s, transform 0.2s;
    box-shadow: 0 2px 8px #0003;
}

.btn-accent:hover {
    background: var(--accent3);
    transform: scale(1.06);
}

.comments-section,
.feedback-section,
.footer {
    width: 100%;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
    display: block;
    clear: both;
}

@media (max-width: 800px) {
    .comments-section,
    .feedback-section,
    .footer {
        max-width: 98vw;
        padding-left: 0.5em;
        padding-right: 0.5em;
    }
}

</style>

<style>
    .hoverzoom {
    transition: transform 0.5s cubic-bezier(.4,0,.2,1), box-shadow 0.4s;
}
.hoverzoom:hover {
    transform: scale(1.08) rotate(-2deg);
    box-shadow: 0 12px 48px #000c, 0 0 0 8px var(--accent2, #3e8ed0);
    z-index: 2;
}

.morph-img {
    border-radius: 12px !important;
    display: block;
    margin-left: auto;
    margin-right: auto;
    max-width: 790px;
    width: 96%;
    aspect-ratio: 16/7;
    object-fit: cover;
    transition: 
        transform 0.45s cubic-bezier(.4,0,.2,1), 
        box-shadow 0.4s, 
        filter 0.4s;
    box-shadow: 0 6px 36px #000a, 0 0 0 5px #444a;
    filter: brightness(0.98) contrast(1.04);
    will-change: transform, box-shadow, filter;
}

.hoverzoom:hover {
    transform: scale(1.045);
    box-shadow: 0 16px 48px #000b, 0 0 0 10px var(--accent2, #3e8ed0);
    filter: brightness(1.04) contrast(1.08);
}

</style>

<style>
.theme-selector {
    display: flex;
    justify-content: center;
    gap: 1em;
    margin: 1.5em 0 0.5em 0;
}
.theme-btn {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    border: 2.5px solid #444;
    cursor: pointer;
    outline: none;
    transition: border 0.2s, box-shadow 0.2s;
    box-shadow: 0 2px 8px #0004;
    display: inline-block;
}
.theme-btn.selected, .theme-btn:focus {
    border: 3px solid var(--accent2);
    box-shadow: 0 0 0 4px var(--accent2)44;
}

</style>
<style>
theme-selector {
    position: relative;
    justify-content: flex-start;
    overflow-x: visible;
    min-height: 48px;
}
.theme-btn {
    position: absolute;
    left: 0;
    z-index: 10;
    margin: 0;
    box-shadow: 0 2px 8px #0004;
    transition:
        left 0.45s cubic-bezier(.4,0,.2,1),
        box-shadow 0.2s,
        border 0.2s,
        z-index 0s;
}
.theme-btn:not(:first-child) {
    z-index: 9;
}
.theme-selector:hover .theme-btn,
.theme-selector:focus-within .theme-btn {
    transition-delay: 0s;
}
.theme-selector .theme-btn {
    pointer-events: auto;
}
.theme-selector:not(:hover):not(:focus-within) .theme-btn {
    left: 0;
}

.theme-btn.animated {
    animation: themePreviewAnim 3s linear infinite;
    background-size: 300% 300% !important;
}

@keyframes themePreviewAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.theme-btn[title="Fire"].animated {
    background: linear-gradient(120deg, #ff512f, #f09819, #ffe53b, #ff512f);
    background-size: 300% 300% !important;
    animation: fireAnim 3.5s linear infinite;
}
@keyframes fireAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.theme-btn[title="Galaxy"].animated {
    background: linear-gradient(120deg, #000428, #004e92, #6a3093, #000428);
    background-size: 300% 300% !important;
    animation: galaxyAnim 4s linear infinite;
}
@keyframes galaxyAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.theme-btn[title="Aqua"].animated {
    background: linear-gradient(120deg, #43cea2, #185a9d, #43cea2, #43cea2);
    background-size: 300% 300% !important;
    animation: aquaAnim 3.5s linear infinite;
}
@keyframes aquaAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.theme-btn[title="Aurora"].animated {
    background: linear-gradient(120deg, #ffff1c, #00c3ff, #38ef7d, #ffff1c);
    background-size: 300% 300% !important;
    animation: auroraAnim 4s linear infinite;
}
@keyframes auroraAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.theme-btn[title="Waves"].animated {
    background: linear-gradient(120deg, #2193b0, #6dd5ed, #2193b0, #6dd5ed);
    background-size: 300% 300% !important;
    animation: wavesAnim 3.5s linear infinite;
}
@keyframes wavesAnim {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}


body, .container, .section, .prof-card, .farewell-card, .memory-card, 
.comments-section, .feedback-section, .footer, .navbar, .timeline-event, 
.memory-text, .farewell-message, .farewell-name, .prof-name, .prof-role,
.comment-user, .comment-date, .comment-text, .feedback-title, .feedback-text, .feedback-date, .feedback-stars {
    color: #fff !important;
}

a, a:visited {
    color: #fff !important;
}

.memories-carousel {
    display: flex;
    overflow-x: auto;
    gap: 4em;
    scroll-behavior: smooth;
    scroll-snap-type: x mandatory;
}
.memory-card {
    scroll-snap-align: start;
}

</style>

<style>

.memories-carousel {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2em;
    overflow: visible;
    background: #111;
    border-radius: 12px;
    padding-bottom: 1em;
}
.memory-card {
    flex: 1 1 220px;
    max-width: 260px;
    min-width: 180px;
    margin-bottom: 1em;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #232526cc;
    border-radius: 12px;
    box-shadow: 0 2px 12px #0003;
    padding: 1em;
}
.memory-img {
    width: 100%;
    max-width: 220px;
    aspect-ratio: 4/3;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 1em;
    box-shadow: 0 2px 12px #0005;
}
</style>

<style>

.animated-navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    z-index: 1000;
    background: rgba(35,37,38,0.96);
    box-shadow: 0 2px 16px #0007;
    transition:
        opacity 0.5s cubic-bezier(.4,0,.2,1),
        top 0.5s cubic-bezier(.4,0,.2,1),
        background 0.3s;
    opacity: 1;
    pointer-events: auto;
}
.animated-navbar.hide-navbar {
    opacity: 0;
    pointer-events: none;
    top: -80px;
}
.animated-navbar.show-navbar {
    opacity: 1;
    pointer-events: auto;
    top: 0;
}
.animated-navbar:hover {
    opacity: 1 !important;
    pointer-events: auto !important;
    top: 0 !important;
    background: rgba(35,37,38,0.99);
}
.animated-navbar ul {
    display: flex;
    justify-content: center;
    gap: 2em;
    list-style: none;
    margin: 0;
    padding: 0.7em 0 0.7em 0;
}
.animated-navbar a {
    color: var(--text-main, #fff);
    text-decoration: none;
    font-weight: 500;
    font-size: 1.1em;
    padding: 0.5em 1.1em;
    border-radius: 8px;
    transition: background 0.2s, color 0.2s;
    position: relative;
    z-index: 2;
}
.animated-navbar a:hover, .animated-navbar a.active {
    background: var(--accent2, #3e8ed0);
    color: #fff;
}
@media (max-width: 900px) {
    .animated-navbar ul {
        gap: 0.7em;
        font-size: 0.98em;
    }
    .animated-navbar a {
        padding: 0.5em 0.7em;
    }
}
body {
    padding-top: 64px !important;
}

.prof-card .prof-name {
    font-weight: 600;
    color: #ff002b; /* roșu accentuat */
    margin-bottom: 0.3em;
    text-shadow: 0 0 8px #ff002b80, 0 2px 8px #0006;

}
.prof-card:hover .prof-name {
    text-shadow: 0 0 18px #ff002bcc, 0 2px 12px #ff002b70, 0 2px 8px #0008;
    color: #ff002f;
}


</style>

<style>
.theme-transition-overlay {
    position: fixed;
    inset: 0;
    z-index: 99999;
    pointer-events: none;
    background: var(--main-bg, #232526);
    opacity: 0;
    transition: opacity 0.7s cubic-bezier(.4,0,.2,1);
    filter: blur(0px) brightness(1.1);
}
.theme-transition-overlay.active {
    opacity: 1;
    filter: blur(8px) brightness(1.2);
}

:root, body, .container, .section, .prof-card, .farewell-card, .memory-card,
.comments-section, .feedback-section, .footer, .navbar {
    transition:
        background 0.7s cubic-bezier(.4,0,.2,1),
        color 0.7s cubic-bezier(.4,0,.2,1),
        box-shadow 0.7s cubic-bezier(.4,0,.2,1),
        border-color 0.7s cubic-bezier(.4,0,.2,1),
        filter 0.7s cubic-bezier(.4,0,.2,1);
}

</style>

    <script>

        function getComments() {
            return JSON.parse(localStorage.getItem('cnpvl_comments') || "[]");
        }
        function saveComments(comments) {
            localStorage.setItem('cnpvl_comments', JSON.stringify(comments));
        }
        function renderComments() {
            const list = document.getElementById('commentList');
            list.innerHTML = "";
            const comments = getComments();
            if (comments.length === 0) {
                list.innerHTML = "<li style='color:#aaa;text-align:center;'>Fii primul care comentează!</li>";
                return;
            }
            comments.forEach(c => {
                const li = document.createElement('li');
                li.className = "comment-item";
                li.innerHTML = `
                    <span class="comment-user">${c.user ? c.user : "Anonim"}</span>
                    <span class="comment-date">${c.date}</span>
                    <div class="comment-text">${c.text.replace(/</g,"&lt;").replace(/>/g,"&gt;")}</div>
                `;
                list.appendChild(li);
            });
        }
        document.getElementById('commentForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const user = document.getElementById('username').value.trim();
            const text = document.getElementById('commentText').value.trim();
            if (!text) return;
            const date = new Date().toLocaleString('ro-RO', { dateStyle: 'short', timeStyle: 'short' });
            const comments = getComments();
            comments.unshift({ user, text, date });
            saveComments(comments);
            renderComments();
            this.reset();
        });
        window.addEventListener('DOMContentLoaded', renderComments);

        function getFeedbacks() {
            return JSON.parse(localStorage.getItem('cnpvl_feedbacks') || "[]");
        }
        function saveFeedbacks(feedbacks) {
            localStorage.setItem('cnpvl_feedbacks', JSON.stringify(feedbacks));
        }
        function renderFeedbacks() {
            const list = document.getElementById('feedbackList');
            list.innerHTML = "";
            const feedbacks = getFeedbacks();
            if (feedbacks.length === 0) {
                list.innerHTML = "<li style='color:#aaa;text-align:center;'>Fii primul care lasă feedback!</li>";
                return;
            }
            feedbacks.forEach(f => {
                const li = document.createElement('li');
                li.className = "feedback-item";
                li.innerHTML = `
                    <span class="feedback-stars">${"&#9733;".repeat(f.stars)}${"&#9734;".repeat(5-f.stars)}</span>
                    <span class="feedback-date">${f.date}</span>
                    <div class="feedback-text">${f.text.replace(/</g,"&lt;").replace(/>/g,"&gt;")}</div>
                `;
                list.appendChild(li);
            });
        }

        let selectedStars = 0;
        const stars = document.querySelectorAll('#starRating .star');
        stars.forEach(star => {
            star.addEventListener('mouseover', function() {
                const val = parseInt(this.dataset.value);
                stars.forEach((s, i) => {
                    s.classList.toggle('selected', i < val);
                });
            });
            star.addEventListener('mouseout', function() {
                stars.forEach((s, i) => {
                    s.classList.toggle('selected', i < selectedStars);
                });
            });
            star.addEventListener('click', function() {
                selectedStars = parseInt(this.dataset.value);
                stars.forEach((s, i) => {
                    s.classList.toggle('selected', i < selectedStars);
                });
            });
        });
        document.getElementById('feedbackForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const text = document.getElementById('feedbackText').value.trim();
            if (!text || selectedStars === 0) return;
            const date = new Date().toLocaleString('ro-RO', { dateStyle: 'short', timeStyle: 'short' });
            const feedbacks = getFeedbacks();
            feedbacks.unshift({ stars: selectedStars, text, date });
            saveFeedbacks(feedbacks);
            renderFeedbacks();
            this.reset();
            selectedStars = 0;
            stars.forEach(s => s.classList.remove('selected'));
        });
        window.addEventListener('DOMContentLoaded', renderFeedbacks);
        let lastScrollY = window.scrollY;
let navbar = document.querySelector('.navbar');
let hideTimeout = null;

function handleNavbar() {
    if (window.scrollY > lastScrollY && window.scrollY > 80) {
        navbar.classList.add('hide-navbar');
        navbar.classList.remove('show-navbar');
    } else {
        navbar.classList.remove('hide-navbar');
        navbar.classList.add('show-navbar');
    }
    lastScrollY = window.scrollY;
}
window.addEventListener('scroll', handleNavbar);

document.addEventListener('mousemove', function(e) {
    if (e.clientY < 80) {
        navbar.classList.remove('hide-navbar');
        navbar.classList.add('show-navbar');
        if (hideTimeout) clearTimeout(hideTimeout);
    } else if (!navbar.matches(':hover')) {
        if (hideTimeout) clearTimeout(hideTimeout);
        hideTimeout = setTimeout(() => {
            navbar.classList.add('hide-navbar');
            navbar.classList.remove('show-navbar');
        }, 800);
    }
});

const THEMES = [
    {
        name: "Dark",
        vars: {
            "--main-bg": "linear-gradient(120deg, #181818 0%, #232526 100%)",
            "--container-bg": "rgba(24, 24, 24, 0.98)",
            "--accent": "#f3c623",
            "--accent2": "#3e8ed0",
            "--accent3": "#e94560",
            "--text-main": "#f3f3f3",
            "--text-muted": "#bdbdbd"
        },
        preview: "linear-gradient(120deg, #181818 0%, #232526 100%)"
    },
    {
        name: "Ocean",
        vars: {
            "--main-bg": "linear-gradient(120deg, #0f2027 0%, #2c5364 100%)",
            "--container-bg": "rgba(20, 34, 54, 0.98)",
            "--accent": "#00c3ff",
            "--accent2": "#005bea",
            "--accent3": "#00d2ff",
            "--text-main": "#e0f7fa",
            "--text-muted": "#b2ebf2"
        },
        preview: "linear-gradient(120deg, #0f2027 0%, #2c5364 100%)"
    },
    {
        name: "Emerald",
        vars: {
            "--main-bg": "linear-gradient(120deg, #134e5e 0%, #71b280 100%)",
            "--container-bg": "rgba(19, 78, 94, 0.98)",
            "--accent": "#a8e063",
            "--accent2": "#56ab2f",
            "--accent3": "#38ef7d",
            "--text-main": "#eaffea",
            "--text-muted": "#b2f2bb"
        },
        preview: "linear-gradient(120deg, #134e5e 0%, #71b280 100%)"
    },
    {
        name: "Sunset",
        vars: {
            "--main-bg": "linear-gradient(120deg, #ff512f 0%, #dd2476 100%)",
            "--container-bg": "rgba(255, 81, 47, 0.92)",
            "--accent": "#ffe53b",
            "--accent2": "#ff2525",
            "--accent3": "#ff512f",
            "--text-main": "#fff8e1",
            "--text-muted": "#ffd6a0"
        },
        preview: "linear-gradient(120deg, #ff512f 0%, #dd2476 100%)"
    },
    {
        name: "Royal",
        vars: {
            "--main-bg": "linear-gradient(120deg, #141e30 0%, #243b55 100%)",
            "--container-bg": "rgba(36, 59, 85, 0.98)",
            "--accent": "#f7971e",
            "--accent2": "#ffd200",
            "--accent3": "#f7971e",
            "--text-main": "#f3f3f3",
            "--text-muted": "#bdbdbd"
        },
        preview: "linear-gradient(120deg, #141e30 0%, #243b55 100%)"
    },
    {
        name: "Lavender",
        vars: {
            "--main-bg": "linear-gradient(120deg, #b993d6 0%, #8ca6db 100%)",
            "--container-bg": "rgba(185, 147, 214, 0.92)",
            "--accent": "#fcb69f",
            "--accent2": "#a770ef",
            "--accent3": "#fcb69f",
            "--text-main": "#2d2d2d",
            "--text-muted": "#6d6d6d"
        },
        preview: "linear-gradient(120deg, #b993d6 0%, #8ca6db 100%)"
    },
    {
        name: "Forest",
        vars: {
            "--main-bg": "linear-gradient(120deg, #5a3f37 0%, #2c7744 100%)",
            "--container-bg": "rgba(44, 119, 68, 0.96)",
            "--accent": "#b7e778",
            "--accent2": "#4e9a51",
            "--accent3": "#2c7744",
            "--text-main": "#eaffea",
            "--text-muted": "#b2f2bb"
        },
        preview: "linear-gradient(120deg, #5a3f37 0%, #2c7744 100%)"
    },
    {
        name: "Rose",
        vars: {
            "--main-bg": "linear-gradient(120deg, #ffafbd 0%, #ffc3a0 100%)",
            "--container-bg": "rgba(255, 175, 189, 0.92)",
            "--accent": "#ff6f91",
            "--accent2": "#ff9671",
            "--accent3": "#ffc3a0",
            "--text-main": "#2d2d2d",
            "--text-muted": "#6d6d6d"
        },
        preview: "linear-gradient(120deg, #ffafbd 0%, #ffc3a0 100%)"
    },
    {
        name: "Night Sky",
        vars: {
            "--main-bg": "linear-gradient(120deg, #232526 0%, #414345 100%)",
            "--container-bg": "rgba(35, 37, 38, 0.98)",
            "--accent": "#00c6fb",
            "--accent2": "#005bea",
            "--accent3": "#232526",
            "--text-main": "#e0f7fa",
            "--text-muted": "#b2ebf2"
        },
        preview: "linear-gradient(120deg, #232526 0%, #414345 100%)"
    },
    {
        name: "Candy",
        vars: {
            "--main-bg": "linear-gradient(120deg, #f7971e 0%, #ffd200 100%)",
            "--container-bg": "rgba(255, 210, 0, 0.92)",
            "--accent": "#f7971e",
            "--accent2": "#ffd200",
            "--accent3": "#f7971e",
            "--text-main": "#2d2d2d",
            "--text-muted": "#6d6d6d"
        },
        preview: "linear-gradient(120deg, #f7971e 0%, #ffd200 100%)"
    },

    {
        name: "Galaxy",
        vars: {
            "--main-bg": "linear-gradient(120deg, #000428 0%, #004e92 100%)",
            "--container-bg": "rgba(0, 4, 40, 0.96)",
            "--accent": "#00c6fb",
            "--accent2": "#004e92",
            "--accent3": "#000428",
            "--text-main": "#e0f7fa",
            "--text-muted": "#b2ebf2"
        },
        preview: "radial-gradient(circle at 30% 30%, #fff 2px, transparent 40%), linear-gradient(120deg, #000428 0%, #004e92 100%)",
        animated: true
    },
    {
        name: "Aqua",
        vars: {
            "--main-bg": "linear-gradient(120deg, #43cea2 0%, #185a9d 100%)",
            "--container-bg": "rgba(67, 206, 162, 0.92)",
            "--accent": "#185a9d",
            "--accent2": "#43cea2",
            "--accent3": "#185a9d",
            "--text-main": "#e0f7fa",
            "--text-muted": "#b2ebf2"
        },
        preview: "repeating-linear-gradient(135deg, #43cea2, #185a9d 40%, #43cea2 80%)",
        animated: true
    },
    {
        name: "Fire",
        vars: {
            "--main-bg": "linear-gradient(120deg, #ff512f 0%, #f09819 100%)",
            "--container-bg": "rgba(255, 81, 47, 0.92)",
            "--accent": "#ffe53b",
            "--accent2": "#ff2525",
            "--accent3": "#ff512f",
            "--text-main": "#fff8e1",
            "--text-muted": "#ffd6a0"
        },
        preview: "linear-gradient(120deg, #ff512f 0%, #f09819 100%)",
        animated: true
    },
    {
        name: "Aurora",
        vars: {
            "--main-bg": "linear-gradient(120deg, #00c3ff 0%, #ffff1c 100%)",
            "--container-bg": "rgba(0, 195, 255, 0.92)",
            "--accent": "#ffff1c",
            "--accent2": "#00c3ff",
            "--accent3": "#ffff1c",
            "--text-main": "#2d2d2d",
            "--text-muted": "#6d6d6d"
        },
        preview: "linear-gradient(120deg, #00c3ff 0%, #ffff1c 100%)",
        animated: true
    },
    {
        name: "Waves",
        vars: {
            "--main-bg": "linear-gradient(120deg, #2193b0 0%, #6dd5ed 100%)",
            "--container-bg": "rgba(33, 147, 176, 0.92)",
            "--accent": "#6dd5ed",
            "--accent2": "#2193b0",
            "--accent3": "#6dd5ed",
            "--text-main": "#e0f7fa",
            "--text-muted": "#b2ebf2"
        },
        preview: "repeating-linear-gradient(90deg, #2193b0, #6dd5ed 40%, #2193b0 80%)",
        animated: true
    }
];

function applyTheme(idx) {
    const theme = THEMES[idx];
    for (const key in theme.vars) {
        document.documentElement.style.setProperty(key, theme.vars[key]);
    }
    localStorage.setItem('cnpvl_theme', idx);
    document.querySelectorAll('.theme-btn').forEach((btn, i) => {
        btn.classList.toggle('selected', i === idx);
    });
}

window.addEventListener('DOMContentLoaded', () => {
});
    const btn = document.createElement('button');
    btn.className = 'theme-btn' + (theme.animated ? ' animated' : '');
    btn.style.background = theme.preview;
    btn.title = theme.name;
    btn.onclick = () => applyTheme(idx);
    selector.appendChild(btn);
    themeBtns.push(btn);

const carousel = document.getElementById('memoriesCarousel');
const prevBtn = document.getElementById('memoriesPrev');
const nextBtn = document.getElementById('memoriesNext');
const cards = Array.from(carousel.querySelectorAll('.memory-card'));
let currentIndex = 0;

function showCard(idx) {
    if (idx < 0) idx = 0;
    if (idx > cards.length - 1) idx = cards.length - 1;
    currentIndex = idx;
    cards.forEach((card, i) => {
        card.style.display = (i === currentIndex) ? 'flex' : 'none';
    });
}

prevBtn.addEventListener('click', () => {
    showCard(currentIndex - 1);
});

nextBtn.addEventListener('click', () => {
    showCard(currentIndex + 1);
});


window.addEventListener('DOMContentLoaded', () => {
    showCard(0);
});

</script>

<script>
const zoomOverlay = document.createElement('div');
zoomOverlay.setAttribute('role', 'dialog');
zoomOverlay.setAttribute('aria-modal', 'true');
zoomOverlay.style.position = 'fixed';
zoomOverlay.style.top = 0;
zoomOverlay.style.left = 0;
zoomOverlay.style.width = '100vw';
zoomOverlay.style.height = '100vh';
zoomOverlay.style.background = 'radial-gradient(ellipse at center, rgba(120,120,120,0.38) 0%, rgba(10,10,20,0.65) 100%)';
zoomOverlay.style.display = 'flex';
zoomOverlay.style.alignItems = 'center';
zoomOverlay.style.justifyContent = 'center';
zoomOverlay.style.zIndex = 9999;
zoomOverlay.style.cursor = 'zoom-out';
zoomOverlay.style.transition = 'opacity 0.7s cubic-bezier(.4,0,.2,1)';
zoomOverlay.style.opacity = 0;
zoomOverlay.style.pointerEvents = 'none';
zoomOverlay.style.backdropFilter = 'blur(5px) brightness(0.98) grayscale(0.06)';
zoomOverlay.tabIndex = -1;


const zoomContainer = document.createElement('div');
zoomContainer.style.position = 'relative';
zoomContainer.style.display = 'inline-block';


const closeBtn = document.createElement('button');
closeBtn.innerHTML = '&times;';
closeBtn.setAttribute('aria-label', 'Închide imagine mărită');
closeBtn.style.position = 'absolute';
closeBtn.style.top = '-18px';
closeBtn.style.right = '-18px';
closeBtn.style.fontSize = '2.1em';
closeBtn.style.background = 'rgba(30,30,30,0.7)';
closeBtn.style.color = '#fff';
closeBtn.style.border = 'none';
closeBtn.style.borderRadius = '50%';
closeBtn.style.width = '1.2em';
closeBtn.style.height = '1.2em';
closeBtn.style.cursor = 'pointer';
closeBtn.style.boxShadow = '0 2px 12px #0007';
closeBtn.style.transition = 'background 0.2s, color 0.2s, transform 0.2s';
closeBtn.style.zIndex = 10001;
closeBtn.addEventListener('mouseenter', () => {
    closeBtn.style.background = '#bbb';
    closeBtn.style.color = '#222';
    closeBtn.style.transform = 'scale(1.12)';
});
closeBtn.addEventListener('mouseleave', () => {
    closeBtn.style.background = 'rgba(30,30,30,0.7)';
    closeBtn.style.color = '#fff';
    closeBtn.style.transform = 'scale(1)';
});
closeBtn.addEventListener('click', hideZoom);

const zoomImg = document.createElement('img');
zoomImg.style.maxWidth = '92vw';
zoomImg.style.maxHeight = '92vh';
zoomImg.style.borderRadius = '22px';
zoomImg.style.boxShadow = '0 0 32px 8px #8887, 0 4px 24px #0007';
zoomImg.style.transition = 'transform 0.9s cubic-bezier(.4,0,.2,1), box-shadow 0.9s, filter 0.9s, opacity 0.7s';
zoomImg.style.filter = 'drop-shadow(0 0 10px #8887) brightness(1.04) contrast(1.04)';
zoomImg.style.background = 'linear-gradient(120deg, #232526 0%, #888 100%)';
zoomImg.style.opacity = 0;
zoomImg.style.margin = '0 auto';
zoomImg.style.display = 'block';
zoomImg.setAttribute('alt', '');

zoomContainer.appendChild(zoomImg);
zoomContainer.appendChild(closeBtn);
zoomOverlay.appendChild(zoomContainer);
document.body.appendChild(zoomOverlay);

let zoomActive = false;
let lastFocused = null;

function showZoom(src, alt) {
    lastFocused = document.activeElement;
    zoomImg.src = src;
    zoomImg.alt = alt || '';
    zoomOverlay.style.opacity = 1;
    zoomOverlay.style.pointerEvents = 'auto';
    document.body.style.overflow = 'hidden';
    zoomImg.style.opacity = 0;
    zoomImg.style.transform = 'scale(0.92)';
    setTimeout(() => {
        zoomImg.style.opacity = 1;
        zoomImg.style.transform = 'scale(1.08)';
        zoomImg.style.boxShadow = '0 0 48px 16px #888a, 0 12px 48px #000a';
        zoomImg.style.filter = 'drop-shadow(0 0 18px #888a) brightness(1.10) contrast(1.10)';
        closeBtn.focus();
    }, 40);
    zoomActive = true;
}
function hideZoom() {
    zoomImg.style.transform = 'scale(0.92)';
    zoomImg.style.boxShadow = '0 0 32px 8px #8887, 0 4px 24px #0007';
    zoomImg.style.filter = 'drop-shadow(0 0 10px #8887) brightness(1.04) contrast(1.04)';
    zoomImg.style.opacity = 0;
    setTimeout(() => {
        zoomOverlay.style.opacity = 0;
        zoomOverlay.style.pointerEvents = 'none';
        document.body.style.overflow = '';
        zoomActive = false;
        if (lastFocused) lastFocused.focus();
    }, 700);
}
zoomOverlay.addEventListener('click', function(e) {
    if (e.target === zoomOverlay) hideZoom();
});


window.addEventListener('keydown', function(e) {
    if (zoomActive && (e.key === "Escape" || e.key === "Esc")) {
        hideZoom();
    }
});

const memoryImgs = Array.from(document.querySelectorAll('.memory-img'));
let currentZoomIdx = -1;
function showZoomByIdx(idx) {
    if (idx < 0 || idx >= memoryImgs.length) return;
    currentZoomIdx = idx;
    const img = memoryImgs[idx];
    showZoom(img.src, img.alt);
}
window.addEventListener('keydown', function(e) {
    if (!zoomActive) return;
    if (e.key === "ArrowLeft" && currentZoomIdx > 0) {
        showZoomByIdx(currentZoomIdx - 1);
    }
    if (e.key === "ArrowRight" && currentZoomIdx < memoryImgs.length - 1) {
        showZoomByIdx(currentZoomIdx + 1);
    }
});

memoryImgs.forEach((img, idx) => {
    img.style.cursor = 'zoom-in';
    img.addEventListener('click', e => {
        showZoomByIdx(idx);
    });
});
</script>

<script>

let fadeoutTimeout = null;

function handleNavbar() {
    if (window.scrollY > lastScrollY && window.scrollY > 80) {
        navbar.classList.add('hide-navbar');
        navbar.classList.remove('show-navbar');
        if (fadeoutTimeout) clearTimeout(fadeoutTimeout);
    } else {
        navbar.classList.remove('hide-navbar');
        navbar.classList.add('show-navbar');
        if (fadeoutTimeout) clearTimeout(fadeoutTimeout);
        fadeoutTimeout = setTimeout(() => {
            navbar.classList.add('hide-navbar');
            navbar.classList.remove('show-navbar');
        }, 2000);
    }
    lastScrollY = window.scrollY;
}
window.addEventListener('scroll', handleNavbar);

document.addEventListener('mousemove', function(e) {
    if (e.clientY < 80) {
        navbar.classList.remove('hide-navbar');
        navbar.classList.add('show-navbar');
        if (hideTimeout) clearTimeout(hideTimeout);
        if (fadeoutTimeout) clearTimeout(fadeoutTimeout);
    } else if (!navbar.matches(':hover')) {
        if (hideTimeout) clearTimeout(hideTimeout);
        hideTimeout = setTimeout(() => {
            navbar.classList.add('hide-navbar');
            navbar.classList.remove('show-navbar');
        }, 800);
    }
});
</script>

<script>

window.addEventListener('DOMContentLoaded', () => {
    const selector = document.createElement('div');
    selector.className = 'theme-selector';
    selector.title = "Alege tema vizuală";
    selector.tabIndex = 0;
    selector.setAttribute('role', 'listbox');
    selector.setAttribute('aria-label', 'Selectează tema vizuală');
    let expanded = false;
    let blurTimeout = null;

    const hoverBox = document.createElement('div');
    hoverBox.style.position = 'absolute';
    hoverBox.style.pointerEvents = 'auto';
    hoverBox.style.top = '-1em';
    hoverBox.style.left = '-1em';
    hoverBox.style.right = '-1em';
    hoverBox.style.bottom = '-1em';
    hoverBox.style.zIndex = 100;
    hoverBox.style.background = 'transparent';
    hoverBox.style.display = 'none';

    const themeBtns = [];
    THEMES.forEach((theme, idx) => {
        const btn = document.createElement('button');
        btn.className = 'theme-btn' + (theme.animated ? ' animated' : '');
        btn.style.background = theme.preview;
        btn.title = theme.name;
        btn.setAttribute('role', 'option');
        btn.setAttribute('aria-label', theme.name);
        btn.tabIndex = -1;
        btn.onclick = (e) => {
            e.stopPropagation();
            applyTheme(idx);
            closeThemes();
        };
        btn.addEventListener('focus', () => openThemes());
        themeBtns.push(btn);
        selector.appendChild(btn);
    });

    selector.style.position = 'relative';
    selector.appendChild(hoverBox);

    const navbar = document.querySelector('.navbar');
    navbar.parentNode.insertBefore(selector, navbar.nextSibling);

    function arrangeThemes(expanded) {
        themeBtns.forEach((btn, i) => {
            if (!expanded) {
                btn.style.left = "0px";
                btn.style.zIndex = (themeBtns.length - i).toString();
                btn.tabIndex = -1;
            } else {
                btn.style.left = (i * 48) + "px";
                btn.style.zIndex = (themeBtns.length - i).toString();
                btn.tabIndex = 0;
            }
        });
    }

    function openThemes() {
        expanded = true;
        selector.classList.add('expanded');
        arrangeThemes(true);
        selector.setAttribute('aria-expanded', 'true');
        // Afișează hoverBox DOAR dacă mouse-ul e pe primul buton
        if (selector.matches(':hover') && themeBtns[0].matches(':hover')) {
            hoverBox.style.display = 'block';
        }
    }
    function closeThemes() {
        expanded = false;
        selector.classList.remove('expanded');
        arrangeThemes(false);
        selector.setAttribute('aria-expanded', 'false');
        hoverBox.style.display = 'none';
    }

    selector.addEventListener('mouseenter', openThemes);
    selector.addEventListener('focusin', openThemes);
    selector.addEventListener('click', (e) => {
        if (!expanded) openThemes();
        else closeThemes();
        e.stopPropagation();
    });

    themeBtns[0].addEventListener('mouseenter', () => {
        openThemes();
        hoverBox.style.display = 'block';
    });

    hoverBox.addEventListener('mouseenter', () => {
        openThemes();
        hoverBox.style.display = 'block';
    });
    hoverBox.addEventListener('mouseleave', () => {
        blurTimeout = setTimeout(closeThemes, 120);
    });

    selector.addEventListener('mouseleave', () => {
        blurTimeout = setTimeout(closeThemes, 120);
    });
    selector.addEventListener('focusout', () => {
        blurTimeout = setTimeout(closeThemes, 120);
    });

    selector.addEventListener('mouseenter', () => {
        if (blurTimeout) clearTimeout(blurTimeout);
    });
    selector.addEventListener('focusin', () => {
        if (blurTimeout) clearTimeout(blurTimeout);
    });

    document.addEventListener('mousedown', (e) => {
        if (!selector.contains(e.target)) closeThemes();
    });

    selector.addEventListener('keydown', (e) => {
        if (e.key === "Escape") {
            closeThemes();
            selector.blur();
        }
    });

    selector.addEventListener('keydown', (e) => {
        if (!expanded) return;
        const idx = themeBtns.findIndex(btn => btn === document.activeElement);
        if (e.key === "ArrowRight" && idx < themeBtns.length - 1) {
            themeBtns[idx + 1].focus();
            e.preventDefault();
        }
        if (e.key === "ArrowLeft" && idx > 0) {
            themeBtns[idx - 1].focus();
            e.preventDefault();
        }
        if (e.key === "Home") {
            themeBtns[0].focus();
            e.preventDefault();
        }
        if (e.key === "End") {
            themeBtns[themeBtns.length - 1].focus();
            e.preventDefault();
        }
    });

    arrangeThemes(false);
    let idx = parseInt(localStorage.getItem('cnpvl_theme'));
    if (isNaN(idx) || idx < 0 || idx >= THEMES.length) idx = 0;
    applyTheme(idx);
});

window.addEventListener('DOMContentLoaded', () => {
    const navLinks = document.querySelectorAll('.navbar a, .animated-navbar a');
    const sections = [
        { id: '', link: navLinks[0] }, // Acasă
        { id: 'istoric', link: navLinks[1] },
        { id: 'profesori', link: navLinks[2] },
        { id: 'amintiri', link: navLinks[3] },
        { id: 'farewell', link: navLinks[4] },
        { id: 'comentarii', link: navLinks[5] },
        { id: 'feedback', link: navLinks[6] }
    ];

    function updateActiveNav() {
        let found = false;
        for (let i = sections.length - 1; i >= 0; i--) {
            const sec = sections[i].id ? document.getElementById(sections[i].id) : document.body;
            if (sec && window.scrollY + 120 >= sec.offsetTop) {
                navLinks.forEach(a => a.classList.remove('active'));
                sections[i].link.classList.add('active');
                found = true;
                break;
            }
        }
        if (!found) {
            navLinks.forEach(a => a.classList.remove('active'));
            navLinks[0].classList.add('active');
        }
    }

    window.addEventListener('scroll', updateActiveNav, { passive: true });
    window.addEventListener('resize', updateActiveNav);
    updateActiveNav();

    navLinks.forEach(link => {
        link.addEventListener('click', function(e) {
            const href = this.getAttribute('href');
            if (href && href.startsWith('#')) {
                const target = document.getElementById(href.slice(1));
                if (target) {
                    e.preventDefault();
                    window.scrollTo({
                        top: target.offsetTop - 60,
                        behavior: 'smooth'
                    });
                }
            }
        });
    });
});

</script>

<script>
const themeOverlay = document.createElement('div');
themeOverlay.className = 'theme-transition-overlay';
document.body.appendChild(themeOverlay);

function applyTheme(idx) {
    themeOverlay.classList.add('active');
    setTimeout(() => {
        const theme = THEMES[idx];
        for (const key in theme.vars) {
            document.documentElement.style.setProperty(key, theme.vars[key]);
        }
        localStorage.setItem('cnpvl_theme', idx);
        document.querySelectorAll('.theme-btn').forEach((btn, i) => {
            btn.classList.toggle('selected', i === idx);
        });
        setTimeout(() => themeOverlay.classList.remove('active'), 700);
    }, 200);
}

</script>
