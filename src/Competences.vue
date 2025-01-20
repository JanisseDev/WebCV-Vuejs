<script setup>
import { inject } from 'vue'

import Page from './components/Page.vue'
import Header from './components/Header.vue'
import Skills from './components/Skills.vue'
import Section from './components/Section.vue'
import Job from './components/Job.vue'
import Project from './components/Project.vue'
import Formation from './components/Formation.vue'

const showLink = inject('showLink');
</script>

<template>
    <Page>
        <Header/>
        <div class="content">
            <div class="main-column">
                <Section style="margin-top:40px" title="DOSSIER DE COMPÉTENCES"></Section>
                <Job class="job"
                 title="OPUSCOPE"
                startMonth="Mai"
                startYear="2021"
                endMonth="Janv."
                endYear="2024"
                :places="['Full télétravail', 'France']"
                jobType="CDI"
                subtitle="Développeur natif iOS AR & Meta Quest VR">
                    <div class="job-content">
                        <Project teamSize="20+"
                        :tags="['Swift', 'Rx', 'MongoDB', 'C#', 'Mobile', 'Git', 'XR', 'Unity']">
                            <p class="description text-indent"><a href="https://www.youtube.com/watch?v=u54OMrF5XqI" target="_blank" class="link" :class="{'link-icon': showLink}">Développement frontend via Swift & UIKit de l'application 'Mappn'.</a></p>
                            <ul class="padding-left-30">
                                <li><p class="description text-indent">Intégration UI des fonctionnalités développées par l'équipe</p></li>
                                <li><p class="description text-indent">Requêtes à la base de données via MongoDB Realm FlexibleSync</p></li>
                                <li><p class="description text-indent">Formation autodidacte à Swift & UIKit</p></li>
                                <li><p class="description text-indent">Communication avec la partie embarquée Unity (Unity as a Service) pour les phases 3D et de réalité augmentée</p></li>
                                <li><p class="description text-indent">Intégration des pins/clusters sur la carte</p></li>
                                <li><p class="description text-indent">Création des interfaces à partir des designs Figma fournis par les UI designers</p></li>
                                <li><p class="description text-indent">Amélioration de l'expérience utilisateur en collaboration avec l'UX designer</p></li>
                                <li><p class="description text-indent">Intégration d'assets graphiques UI</p></li>
                                <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                                <li><p class="description text-indent">Méthode Agile: Scrum</p></li>
                                <li><p class="description text-indent">Environnement de travail: Natif iOS (Swift) & Unity 3D (C#), Git, XCode, Visual Studio, Build CI quotidienne, Notion</p></li>
                            </ul>
                        </Project>
                        <Project teamSize="20+"
                        :tags="['Swift', 'Rx', 'MongoDB', 'C#', 'Mobile', 'Git', 'XR', 'Unity']">
                            <p class="description text-indent"><a href="https://www.opuscope.com/minsar/overview" target="_blank" class="link" :class="{'link-icon': showLink}">Contribution à l'interface utilisateur VR de l'application 'Minsar Studio'</a></p>
                            <ul class="padding-left-30">
                                <li><p class="description text-indent">Adaptation de l'interface VR vers une interface 2D mobile & PC</p></li>
                                <li><p class="description text-indent">Intégration UI des fonctionnalités développées par l'équipe</p></li>
                                <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                                <li><p class="description text-indent">Méthode Agile: Scrum</p></li>
                                <li><p class="description text-indent">Environnement de travail: Unity 3D (C#), Git, Visual Studio, Build CI quotidienne, Notion</p></li>
                            </ul>
                        </Project>
                    </div>
                </Job>
                <Job title="FULL CYCLE GAMES"
                startMonth="Fév."
                startYear="2017"
                endMonth="Avril"
                endYear="2020"
                :places="['Vaulx-en-Velin', 'France']"
                jobType="CDI"
                subtitle="Développeur jeu mobile en ligne en temps réel">
                    <Project teamSize="8"
                    :tags="['C#', 'Mobile', 'Git', 'Multijoueur', 'Unity']">
                        <p class="description text-indent"><a href="https://www.youtube.com/watch?v=vSwRtdF4hM0" target="_blank" class="link" :class="{'link-icon': showLink}">Conception du client Unity du jeu mobile multijoueur 'Gleem Lands'.</a></p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Conception du cahier des charges avec l'équipe</p></li>
                            <li><p class="description text-indent">Développement de l'architecture du client mobile</p></li>
                            <li><p class="description text-indent">Communication avec le backend via des requêtes API et des notifications via WebSocket</p></li>
                            <li><p class="description text-indent">Envoi et réception de paquets UDP avec les serveurs de jeu via la librairie Enet</p></li>
                            <li><p class="description text-indent">Optimisation des performances via la création d'un outil permettant de convertir une animation en un ensemble de vertex précalculés (évitant au processeur de devoir gérer un grand nombre d'animators lors de l'exécution)</p></li>
                            <li><p class="description text-indent">Création de shaders pour améliorer les performances (optimisation du nombre de Drawcalls)</p></li>
                            <li><p class="description text-indent">Développement d'un outil de débogage interne permettant d'interpréter des logs serveur afin de retracer visuellement le déroulement d'une phase de gameplay</p></li>
                            <li><p class="description text-indent">Déploiement de l'application sur les stores Google Play et Apple App Store</p></li>
                            <li><p class="description text-indent">Intégration d'assets graphiques (UI/modèles 3D) et audio (FX/musique)</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Méthode Agile: Scrum avec Poker planning</p></li>
                            <li><p class="description text-indent">Environnement de travail: Unity 3D (C#), Git, Monodevelop, Jira</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job class="break-before"
                 title="GERCOP DIGITAL"
                startMonth="Fév."
                startYear="2016"
                endMonth="Fév."
                endYear="2017"
                :places="['Lyon', 'France']"
                jobType="CDI"
                subtitle="Développeur d'application d'aide à la vente immobilière">
                    <Project teamSize="2"
                    :tags="['C#', 'Mobile', 'Git', 'VR', 'Unity']">
                        <p class="description text-indent">Développement d'applications mobiles 3D sur Unity pour la présentation de biens immobiliers.</p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Conception du cahier des charges avec les clients</p></li>
                            <li><p class="description text-indent">Intégration d'assets graphiques UI et modèles 3D</p></li>
                            <li><p class="description text-indent">Création de shaders pour un rendu plus réaliste de la végétation et de l'eau</p></li>
                            <li><p class="description text-indent">Déploiement des applications sur un réseau interne AdHoc</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Méthode Agile: Kanban</p></li>
                            <li><p class="description text-indent">Environnement de travail: Unity 3D (C#), Git, Monodevelop, Trello</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job title="BREAKFIRST"
                startMonth="Sept."
                startYear="2014"
                endMonth="Sept."
                endYear="2015"
                :places="['Lyon', 'France']"
                jobType="Alternance"
                subtitle="Développeur jeu mobile AR">
                    <Project teamSize="6"
                    :tags="['C#', 'Mobile', 'Git', 'AR', 'Unity']">
                        <p class="description text-indent">Développement de gameplay en réalité augmenté via la caméra frontale des mobiles.</p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Utilisation de la technologie de motion gaming développée en interne, permettant d'utiliser la caméra frontale d'un téléphone ou d'une tablette à la manière de l'Eye Toy et Kinect</p></li>
                            <li><p class="description text-indent">Prototypage de jeux mobiles Android/iOS</p></li>
                            <li><p class="description text-indent">Développement de phases de gameplay</p></li>
                            <li><p class="description text-indent">Intégration d'assets graphiques (UI/modèles 3D) et audio (FX/musique)</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Environnement de travail: Unity 3D (C#), Git, Trello, Xcode, Monodevelop</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job title="CRSNG ESSILOR"
                startMonth="Avril"
                startYear="2014"
                endMonth="Juin"
                endYear="2014"
                :places="['Montréal', 'Canada']"
                jobType="Stage"
                subtitle="Développeur projet de recherche">
                    <Project teamSize="4"
                    :tags="['C#', 'Git', 'VR', 'Unity']">
                        <p class="description text-indent">Développement d'un simulateur de foule sur une salle immersive (CAVE) pour la Chaire industrielle CRSNG-Essilor.</p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Conception du cahier des charges avec les équipes de recherche</p></li>
                            <li><p class="description text-indent">Intégration d'assets graphiques UI et modèles 3D</p></li>
                            <li><p class="description text-indent">Implémentation d'un système de pathfinding A*</p></li>
                            <li><p class="description text-indent">Synchronisation des simulations tournant sur chaque machine (un PC dédié à chaque mur du CAVE)</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Environnement de travail: Unity 3D (C#), Git, Monodevelop</p></li>
                        </ul>
                    </Project>
                </Job>
                
                <Section title="FORMATIONS"></Section>
                <Job title="IUT LE PUY-EN-VELAY"
                startMonth="Sept."
                startYear="2014"
                endMonth="Juill."
                endYear="2015"
                :places="['Le Puy-en-Velay', 'France']"
                jobType="Licence Pro en alternance"
                subtitle='"3D Temps Réel et Réalité Virtuelle"'>
                    <Project :tags="['C#', 'C++', 'VR', 'Unity', 'OpenGL']">
                        <p class="description text-indent">Approfondissement de la formation DUT orientée vers les nouvelles technologies 3D.</p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Développement de projets sur l'Oculus DK1</p></li>
                            <li><p class="description text-indent">Création d'un plugin Unity permettant de récupérer la position et l'orientation de deux aimants dans l'espace</p></li>
                            <li><p class="description text-indent">Environnement de travail: Visual Studio, Unity 3D (C#)</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job title="IUT LE PUY-EN-VELAY"
                startMonth="Sept."
                startYear="2014"
                endMonth="Juill."
                endYear="2015"
                :places="['Le Puy-en-Velay', 'France']"
                jobType="DUT"
                subtitle='"Imagerie Numérique"'>
                    <Project :tags="['C#', 'C++', 'VR', 'Unity', 'OpenGL', 'SQL']">
                        <p class="description text-indent">Formation à la programmation orientée vers le domaine de l'imagerie (rendu 3D, vision industrielle, analyse d'image).</p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Développement d'un projet de visite virtuelle sur Google Cardboard</p></li>
                            <li><p class="description text-indent">Adaptation d'un jeu de société sur table interactive (Microsoft SUR40)</p></li>
                            <li><p class="description text-indent">Projet de site internet type forum avec base de données SQL</p></li>
                            <li><p class="description text-indent">Environnement de travail: Visual Studio, Unity 3D (C#)</p></li>
                        </ul>
                    </Project>
                </Job>

                <Section class="break-before" title="PROJETS PERSONNELS"></Section>
                <Job title="TRIGGER MOVIE"
                endYear="2025"
                subtitle="Développeur fullstack Vue.js & PHP">
                    <Project teamSize="1"
                    :tags="['Vue.js', 'PHP', 'MariaDB', 'Git']">
                        <p class="description text-indent"><a href="https://maroon-dog-827220.hostingersite.com/" target="_blank" class="link" :class="{'link-icon': showLink}">Design et Développement d'une plateforme collaborative où les utilisateurs ajoutent des avertissements aux films pour des expériences cinématographiques plus sûres et éclairées.</a></p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Réalisation de la partie front avec Vue.js</p></li>
                            <li><p class="description text-indent">Gestion de l'authentification et des requêtes via une API réalisé en PHP</p></li>
                            <li><p class="description text-indent">Stockage des données dans une base de donnée MariaDB</p></li>
                            <li><p class="description text-indent">Connexion à l'API publique de 'The Movie Database'</p></li>
                            <li><p class="description text-indent">Mise en ligne du site</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Environnement de travail: Git, Visual Studio Code, Postman, Sequel Pro</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job title="BOARD GAME TOOLBOX"
                endYear="2024"
                subtitle="Développeur .Net MAUI">
                    <Project teamSize="1"
                    :tags="['C#', '.Net MAUI', 'Rx', 'LiteDB', 'Mobile', 'Git']">
                        <p class="description text-indent"><a href="https://github.com/JanisseDev/ScoreTracker" target="_blank" class="link" :class="{'link-icon': showLink}">Développement d'une application compagnon open source pour des jeux de societé.</a></p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Utilisation de Rx pour un rafraichissement de l'affichage réactif</p></li>
                            <li><p class="description text-indent">Stockage des données localement via une base de données LiteDB</p></li>
                            <li><p class="description text-indent">Déploiement de l'application sur le store Google Play</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Environnement de travail: Git, Visual Studio</p></li>
                        </ul>
                    </Project>
                </Job>
                <Job title="MONTURE ÉQUATORIALE MOTORISÉE"
                endYear="2023"
                subtitle="Designer Impression 3D & Développeur C++">
                    <Project teamSize="1"
                    :tags="['C++', 'HTML', 'Fusion 360', 'Impression 3D', 'Raspberry Pico W', 'Git']">
                        <p class="description text-indent"><a href="https://github.com/JanisseDev/motorized-equatorial-mount" target="_blank" class="link" :class="{'link-icon': showLink}">Design et Développement d'une monture équatoriale motorisée pilotable via un smartphone en Wifi.</a></p>
                        <ul class="padding-left-30">
                            <li><p class="description text-indent">Modélisation des pièces mécaniques en 3D</p></li>
                            <li><p class="description text-indent">Impression et assemblage des pièces mécaniques</p></li>
                            <li><p class="description text-indent">Création des schéma électronique</p></li>
                            <li><p class="description text-indent">Utilisation du module Wifi du Raspberry Pico pour auto-héberger un site pour contrôler l'appareil à distance</p></li>
                            <li><p class="description text-indent">Mise à disposition publique de la Documentation sur GitHub</p></li>
                            <li><p class="description text-indent">Tests et corrections de bugs</p></li>
                            <li><p class="description text-indent">Environnement de travail: Git, Visual Studio Code</p></li>
                        </ul>
                    </Project>
                </Job>
            </div>
        </div>
    </Page>
</template>

<style scoped>
.content {
    display: flex;
    flex-direction: row;
    align-items: stretch;
    justify-content: space-evenly;
    flex: 1;
    padding-top: calc(var(--additional-gap));
}

.side-column {
    display: flex;
    background-color: white;
    border-right: solid #dcdcdc 2px;
    flex-direction: column;
    align-items: stretch;
    justify-content: space-around;
    padding: 0px 20px;
    margin: 50px 0px;
    gap: 30px;
    flex: 0;
}

.main-column {
    display: flex;
    background-color: white;
    flex-direction: column;
    align-items: stretch;
    justify-content: space-evenly;
    padding: 0px 25px 25px 25px;
    gap: 25px;
    flex: 1;
}

.section-row {
    display: flex;
    align-items: flex-start;
    justify-content: space-around;
    gap: var(--primary-secondary-gap);
    break-inside: avoid;
}
</style>

<style>
.description {
    font-weight: 300;
    font-size: 0.8rem;
    letter-spacing: 0rem;
    text-align: justify;
}

a {
    color: black;
    text-decoration: none;
}

.link-icon::after {
    content:'';
    background-image:url('@/assets/link.png');
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center center;
    margin-left: 2px;
    padding-right: 20px;    /* Size */
}

.text-indent {
    text-indent: -12px;
    padding-left: 18px !important;
}

.job-content {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.padding-left-30 {
    padding-left: 30px;
}

.break-before {
    padding-top: 20px;
    page-break-before: always;
}
</style>