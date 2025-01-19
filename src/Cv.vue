<script setup>
import { inject } from 'vue'

import Page from './components/Page.vue'
import Header from './components/Header.vue'
import Skills from './components/Skills.vue'
import Section from './components/Section.vue'
import Job from './components/Job.vue'
import Formation from './components/Formation.vue'

const showLink = inject('showLink');
</script>

<template>
    <Page>
        <Header/>
        <div class="content">
            <div class="side-column">
                <Skills title="Techniques" :skills="['C#', 'Rx', 'Swift', 'Vue.js', '.Net MAUI', 'MongoDB']"></Skills>
                <Skills title="Logiciels" :skills="['Git', 'Visual&nbsp;Studio', 'Xcode', 'Unity', 'Rider']"></Skills>
                <Skills title="Loisirs" :skills="['Impression&nbsp;3D', 'Photographie', 'Réparation', 'Cinéma', 'Escape Games', 'Domotique']"></Skills>
                <Skills title="Sports" :skills="['Badminton', 'Trail', 'Vélo']"></Skills>
                <Skills title="Langues" :skills="['Français', 'Anglais']"></Skills>
            </div>
            <div class="main-column">
                <p class="description">Passionné et créatif, je suis constamment à la recherche de nouvelles technologies. Doté d'un tempérament calme et patient, ma proactivité me permet d'être efficace aussi bien en autonomie qu'au sein d'une équipe. Mon engagement envers l'innovation et mon approche méthodique feront de moi un atout précieux pour vos projets.</p>
                
                <Section title="EXPÉRIENCES PROFESSIONNELLES">
                <Job title="OPUSCOPE"
                startMonth="Mai"
                startYear="2021"
                endMonth="Janv."
                endYear="2024"
                :places="['Full télétravail', 'France']"
                jobType="CDI"
                subtitle="Développeur natif iOS AR & Meta Quest VR"
                teamSize="20+"
                :tags="['Swift', 'Rx', 'MongoDB', 'C#', 'Mobile', 'Git', 'XR', 'Unity']">
                    <p class="description text-indent"><a href="https://www.youtube.com/watch?v=u54OMrF5XqI" target="_blank" class="link" :class="{'link-icon': showLink}">Développement frontend via Swift & UIKit de l'application 'Mappn'.</a></p>
                    <p class="description text-indent">Requêtes à la base de données via MongoDB Realm FlexibleSync.</p>
                    <p class="description text-indent">Communication avec Unity (Unity as a Service) pour les phases 3D en réalité augmentée.</p>
                    <p class="description text-indent">Développent d'interface VR pour l'application 'Minsar studio'.</p>
                </Job>
                <Job title="FULL CYCLE GAMES"
                startMonth="Fév."
                startYear="2017"
                endMonth="Avril"
                endYear="2020"
                :places="['Vaulx-en-Velin', 'France']"
                jobType="CDI"
                subtitle="Développeur jeu mobile en ligne en temps réel"
                teamSize="8"
                :tags="['C#', 'Mobile', 'Git', 'Multijoueur', 'Unity']">
                    <p class="description text-indent"><a href="https://www.youtube.com/watch?v=vSwRtdF4hM0" target="_blank" class="link" :class="{'link-icon': showLink}">Conception du client Unity du jeu mobile multijoueur 'Gleem Lands'.</a></p>
                    <p class="description text-indent">Création d'outils et de shaders.</p>
                    <p class="description text-indent">Communication avec le backend via différents protocoles réseaux (API / WebSocket / UDP).</p>
                </Job>
                <Job title="GERCOP DIGITAL"
                startMonth="Fév."
                startYear="2016"
                endMonth="Fév."
                endYear="2017"
                :places="['Lyon', 'France']"
                jobType="CDI"
                subtitle="Développeur d'application d'aide à la vente immobilière"
                teamSize="2"
                :tags="['C#', 'Mobile', 'Git', 'VR', 'Unity']">
                    <p class="description text-indent">Développement d'applications mobiles 3D sur Unity pour la présentation de biens immobiliers.</p>
                    <p class="description text-indent"><a href="https://www.youtube.com/watch?v=_QBolkK5HW8" target="_blank" class="link" :class="{'link-icon': showLink}">Création de visite virtuelle immersive (HTC Vive), permettant à l'utilisateur de personnaliser son intérieur.</a></p>
                </Job>
                <Job title="BREAKFIRST"
                startMonth="Sept."
                startYear="2014"
                endMonth="Sept."
                endYear="2015"
                :places="['Lyon', 'France']"
                jobType="Alternance"
                subtitle="Développeur jeu mobile AR"
                teamSize="6"
                :tags="['C#','Mobile', 'Git', 'AR', 'Unity']">
                    <p class="description text-indent">Développement de gameplay en réalité augmenté via la caméra frontale des mobiles.</p>
                    <p class="description text-indent">Intégration d'assets graphiques (UI/modèles 3D) et audio (FX/musique).</p>
                    <p class="description text-indent">Implémentation de features sur le moteur interne du studio.</p>
                </Job>
                <Job title="CRSNG ESSILOR"
                startMonth="Avril"
                startYear="2014"
                endMonth="Juin"
                endYear="2014"
                :places="['Montréal', 'Canada']"
                jobType="Stage"
                subtitle="Développeur projet de recherche"
                teamSize="4"
                :tags="['C#', 'Git', 'VR', 'Unity']">
                    <p class="description text-indent">Développement d'un simulateur de foule sur une salle immersive (CAVE) pour la Chaire industrielle CRSNG-Essilor.</p>
                    <p class="description text-indent">Synchronisation de la simulation à travers les différents clusters du CAVE.</p>
                </Job>
                </Section>

                <Section title="FORMATIONS">
                <div class="section-row">
                    <Formation :titles="['Licence Pro en alternance', '3D Temps Réel et Réalité Virtuelle']"
                    date="2014 - 2015"
                    place="IUT Le Puy-en-Velay (43)"/>
                    <Formation :titles="['DUT', 'Imagerie Numérique']"
                    date="2012 - 2014"
                    place="IUT Le Puy-en-Velay (43)"/>
                    <Formation :titles="['BAC Scientifique', '(option Sciences de l\'ingénieur)']"
                    date="2012"
                    place="Lycée Jacob-Holtzer, Firminy (42)"/>
                </div>
                </Section>

                <Section title="PROJETS PERSONNELS">
                <Job title="BOARD GAME TOOLBOX"
                endYear="2024"
                subtitle="Développeur .Net MAUI"
                :tags="['C#', '.Net MAUI', 'Rx', 'LiteDB', 'Mobile', 'Git']">
                    <p class="description text-indent"><a href="https://github.com/JanisseDev/ScoreTracker" target="_blank" class="link" :class="{'link-icon': showLink}">Développement d'une application compagnon open source pour des jeux de societé.</a></p>
                </Job>
                <Job title="MONTURE ÉQUATORIALE MOTORISÉE"
                endYear="2023"
                subtitle="Designer Impression 3D & Développeur C++"
                :tags="['C++', 'HTML', 'Fusion 360', 'Impression 3D', 'Raspberry Pico W', 'Git']">
                    <p class="description text-indent"><a href="https://github.com/JanisseDev/motorized-equatorial-mount" target="_blank" class="link" :class="{'link-icon': showLink}">Design & Développement d'une monture équatoriale motorisée pilotable via un smartphone en Wifi.</a></p>
                </Job>
                </Section>
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
</style>