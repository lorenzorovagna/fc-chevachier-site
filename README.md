
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>FC Chevachier - Club Amateur de Briançon</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        /* Variables de couleurs */
        :root {
            --bleu: #0066cc;
            --noir: #1a1a1a;
            --blanc: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: var(--noir);
            color: var(--blanc);
            overflow-x: hidden; /* Évite le défilement horizontal */
        }

        /* ========= ACCUEIL (PAGE D'ENTRÉE) ========= */
        #home {
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(to bottom right, var(--bleu), var(--noir));
            cursor: pointer;
            position: relative;
        }

        #main-logo {
            width: 280px;
            max-width: 80vw; /* Pour la réactivité sur petits écrans */
            transition: transform 0.3s;
        }

        #main-logo:hover {
            transform: scale(1.1);
        }

        /* ========= MENU FLOTTANT ========= */
        #menu {
            display: none; /* Masqué par défaut */
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(0, 0, 0, 0.95);
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            z-index: 1000;
            box-shadow: 0 0 10px rgba(0,0,0,0.7);
            animation: fadeIn 0.5s ease forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -60%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }

        .menu-item {
            color: var(--blanc);
            text-decoration: none;
            display: block;
            margin: 1rem 0;
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .menu-item:hover {
            color: var(--bleu);
        }

        /* ========= SECTIONS ========= */
        .section {
            display: none; /* Masqué par défaut, on l'affiche dynamiquement via JS */
            padding: 4rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            animation: fadeSection 0.5s ease forwards;
        }

        /* Animation pour faire apparaître la section en fondu */
        @keyframes fadeSection {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h2 {
            color: var(--bleu);
            margin-bottom: 2rem;
            text-align: center;
        }

        /* ========= RESPONSIVE ========= */
        @media (max-width: 768px) {
            #main-logo {
                width: 200px;
            }
            .section {
                padding: 2rem 1rem;
            }
        }

        /* ========= FOOTER ========= */
        footer {
            background: var(--noir);
            padding: 2rem;
            text-align: center;
            border-top: 2px solid var(--bleu);
        }

        .social-links {
            margin-top: 1rem;
        }

        .social-links a {
            color: var(--blanc);
            margin: 0 0.5rem;
            text-decoration: none;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--bleu);
        }

        /* Petit bouton pour fermer le menu (optionnel) */
        .close-menu {
            position: absolute;
            top: 10px;
            right: 10px;
            background: none;
            border: none;
            color: var(--blanc);
            font-size: 1.2rem;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <!-- ========= ACCUEIL ========= -->
    <section id="home" onclick="toggleMenu()">
        <img src="c:\Users\info\Downloads\WhatsApp_Image_2025-03-24_at_17.07.59-removebg-preview.png" alt="Logo FC Chevachier" id="main-logo">
    </section>

    <!-- ========= MENU FLOTTANT ========= -->
    <div id="menu">
        <button class="close-menu" onclick="toggleMenu()">X</button>
        <a href="#equipe" class="menu-item" onclick="showSection('equipe')">L'Équipe</a>
        <a href="#matchs" class="menu-item" onclick="showSection('matchs')">Les Matchs</a>
        <a href="#maillots" class="menu-item" onclick="showSection('maillots')">Les Maillots</a>
        <a href="#projets" class="menu-item" onclick="showSection('projets')">Les Projets</a>
        <a href="#historique" class="menu-item" onclick="showSection('historique')">Historique</a>
        <a href="#sponsors" class="menu-item" onclick="showSection('sponsors')">Sponsors</a>
        <a href="#contact" class="menu-item" onclick="showSection('contact')">Contact</a>
    </div>

    <!-- ========= SECTIONS ========= -->
    <section id="equipe" class="section">
        <h2>Notre Équipe</h2>
        <p>
            Gardiens : Ethan Petit, Titouan Devars <br>
            Défenseurs : Lorenzo Rovagna, Florian Levalois, Jules Lemaitre, Sacha Ndiaye, Rémi Baridon, Julien Speelers <br>
            Milieux : Noé Scala, Alexis Fine, Yanis <br>
            Attaquants : Axel Girousse, Oliwier Kusmierczyk, Zakaryia Elariak, Matthieu Caille, Andre Marques, Jamil <br>
        </p>
    </section>

    <section id="matchs" class="section">
        <h2>Calendrier des Matchs</h2>
        <p>
            Match Samedi 05 avril 2025 contre le bayer les verres cul sec à 15h au stade Bouchié Giraudo.
        </p>
    </section>

    <section id="maillots" class="section">
        <h2>Nos Maillots</h2>
        <p>
            Présentation des différents maillots (domicile, extérieur, troisième maillot...).  
            Vous pouvez insérer des images pour chaque tenue.
        </p>
    </section>

    <section id="projets" class="section">
        <h2>Nos Projets</h2>
        <p>
            Nous souhaitons trouver des sponsors pour financer en partie notre futur projet : avoir nos propres maillots.
        </p>
    </section>

    <section id="historique" class="section">
        <h2>Notre Histoire</h2>
        <p>
            Le FC Chevachier est un club de Briançon créé en juin 2024 par une bande de copains. <br> 
            Nous avons jusqu'à présent remporté 1 match contre le fc Ice Spice aux prolongations, <br>
            mais nous avons accroché plusieurs grandes équipes comme le fc 100 petasses, monévier <br>
            ou encore le bayer les verres cul sec. Nous rappelons que nous sommes les plus jeunes <br>
            du championnat.
        </p>
    </section>

    <section id="sponsors" class="section">
        <h2>Nos Sponsors</h2>
        <p>
            A la recherche de sponsors
        </p>
    </section>

    <section id="contact" class="section">
        <h2>Contact</h2>
        <p>
            Email : <a href="lorenzo.rovagna@icloud.com" style="color: var(--bleu);">lorenzo.rovagna@icloud.com</a><br>
            Téléphone : 0767710193
        </p>
        <div class="social-links">
            <a href="#" target="_blank">Facebook</a>
            <a href="#" target="_blank">Instagram</a>
        </div>
    </section>

    <!-- ========= PIED DE PAGE ========= -->
    <footer>
        <p>© 2024 FC Chevachier - Briançon</p>
        <p>Site officiel - Tous droits réservés</p>
    </footer>

    <script>
        // Fonction pour afficher/masquer le menu
        function toggleMenu() {
            const menu = document.getElementById('menu');
            if (menu.style.display === 'block') {
                menu.style.display = 'none';
            } else {
                menu.style.display = 'block';
            }
        }

        // Fonction pour afficher une section et masquer les autres
        function showSection(sectionId) {
            // On masque toutes les sections
            document.querySelectorAll('.section').forEach(section => {
                section.style.display = 'none';
            });
            // On affiche la section demandée
            const targetSection = document.getElementById(sectionId);
            targetSection.style.display = 'block';

            // On referme le menu après le clic
            toggleMenu();
        }

        // Optionnel : fermer le menu si clic en dehors
        window.onclick = function(event) {
            const menu = document.getElementById('menu');
            // Si l'utilisateur clique hors du menu ET hors du logo d'accueil
            if (event.target !== menu && event.target !== document.getElementById('main-logo')) {
                // Vérifie aussi que le menu n'est pas déjà masqué
                if (menu.style.display === 'block' && !menu.contains(event.target)) {
                    menu.style.display = 'none';
                }
            }
        }
    </script>
</body>
</html>
