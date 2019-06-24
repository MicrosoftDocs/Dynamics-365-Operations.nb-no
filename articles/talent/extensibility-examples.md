---
title: Utvide Talent ved hjelp av PowerApps og Microsoft Flow – eksempelscenarier
description: Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 for Talent som bruker Microsoft PowerApps og Microsoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a9ebfd1f2621b8ad65d7623c37b6851cc0b5cb54
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577801"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Utvide Talent ved hjelp av PowerApps og Microsoft Flow – eksempelscenarier

Dette emnet beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 for Talent som bruker Microsoft PowerApps og Microsoft Flow. Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt miljø for PowerApps. Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.

> [!IMPORTANT]
> Hvis du vil bruke malene og appen som er beskrevet i dette emnet, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.


## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.
- Hvis du vil eksportere eller importere apper, må brukerne ha en PowerApps Plan 2-lisens eller en PowerApps Plan 2-prøvelisens.

## <a name="flow--form-connect"></a>Flyt – skjematilkobling

Malen for **Flyt – skjematilkobling** kan brukes til å lese data fra Microsoft Forms og lagre den i en Common Data Service-enhet.

Denne malen kan utvides slik at den kan brukes til andre scenarioer. Her er noen eksempler:

- Registrer kandidatvurderinger.
- Lagre resultater fra kursspørreskjema.
- Kompiler et bibliotek med intervjuspørsmål for HR-administratorer.
- Registrere en kandidats evaluering av intervjuprosessen

I Microsoft Dynamics 365: Attract kan skjemaer vises i kandidatportalen, og kandidater kan fylle ut detaljer. Skjemaer kan også innebygges som aktiviteter i en jobbmal.

Når en kandidat sender et skjema, fanger Microsoft Flow opp skjemainnsendingen, leser dataene og lagrer den i Common Data Service-enheten.

For å laste ned malen for **Flyt – skjematilkobling** og den egendefinerte enhetsstrukturen, kan du gå til [Flyt – skjematilkobling](https://go.microsoft.com/fwlink/?linkid=2081988) på Microsoft Download Center.

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Starte og hente parametere som er sendt til Powerapps

Malen for **Starte og hente parametere som er sendt til Powerapps** kan brukes som utgangspunkt for et hvilket som helst PowerApps-scenario som er spesifikt for Attract. Den inneholder alle standardparameterne som sendes av Attract, for eksempel **Stillingssøknad**, **Kandidat-ID** og **Jobb-ID**.

Denne malen kan brukes til å hente et kandidatvurderingsskjema, slik at en ansettelsesansvarlig kan vise vurderingen som en kandidat fylte ut.

Apper som er opprettet ved hjelp av PowerApps, kan bygges inn jobbmalen i Attract.

For å laste ned malen for **Starte og hente parametere som er sendt til Powerapps** og den egendefinerte enhetsstruktur, kan du gå til [Starte og hente parametere som er sendt til Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) på Microsoft Download Center.

## <a name="integration-with-office-365"></a>Integrering med Office 365

**Integrering med Office 365**-appen kan brukes til å hente teaminformasjon for påloggede brukere fra Microsoft Office 365. Den refererer til arbeidere i Talent for å hente innstemplings- og utstemplingsdetaljer og unntaksregistreringer. Innstemplings- og utstemplingsinformasjon lagres i egendefinerte Common Data Service-enheter. Det antas at disse opplysningene fylles ut fra tredjepartssystemer via integrasjon.

Denne appen kan utvides, slik at den kan brukes til andre scenarioer. Den kan for eksempel brukes til å vise ferieinformasjon for team, kalenderhendelser og teamspesifikke hendelser.

For å laste ned **Integrering med Office 365**-appen og egendefinert enhetsstruktur, kan du gå til [Integrering med Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) på Microsoft Download Center.

## <a name="flow--email-notification"></a>Flyt – e-postvarsling

Malen **Flyt – e-postvarsling** kan brukes i e-postvarslingsscenarioer. Den kan brukes til å utløse varsel-e-postmeldinger til kandidater som ansettelsesteamet avviser i løpet av et hvilket som helst trinn i rekrutteringsprosessen.

Denne malen kan utvides til å spore endringer i kandidatstadiet i rekrutteringsprosessen og til å sende meldinger til ansettelsesteamet og kandidaten.

Generelt for enhetene som er lagret i Common Data Service, kan flyter defineres til å sende varslinger for hendelser som forekommer i Core HR, Attract eller Dynamics 365 Talent: Onboard.

For å laste ned **Flyt – e-postvarsling**-malen, gå til [Flyt – e-postvarsling](https://go.microsoft.com/fwlink/?linkid=2082103) på Microsoft Download Center.

## <a name="flow--sql-connect-and-execute"></a>Flyt – SQL-tilkobling og kjøring

**Flyt – SQL-tilkobling og kjøring**-malen kobler til Microsoft SQL Server og aktiverer SQL-spørringer som skal kjøres.

Selv om denne malen er utformet for å lese og oppdatere SQL-tabeller, kan den utvides, slik at den kan brukes til andre scenarioer. Den kan for eksempel brukes til å fylle ut en oppsamlingstabell i Common Data Service med poster fra SQL Server og synkronisere oppsamlingstabellen jevnlig ved hjelp av en trinnvis push fra SQL Server.

For å laste ned malen for **Flyt – SQL-tilkobling og kjøring**, kan du gå til [Flyt – SQL-tilkobling og kjøring](https://go.microsoft.com/fwlink/?linkid=2081789) på Microsoft Download Center.

## <a name="flow--sharepoint-integration"></a>Flyt – SharePoint-integrering

Malen **Flyt – SharePoint-ingetrering** kan brukes til å lese data fra en Microsoft SharePoint-liste, sammenligne listen med feltverdier for alle Common Data Service-enheter og sende resultatene av sammenligningen som en e-postvarsling. 

En organisasjon kan ha et sett med ferdigheter som den har raskt behov for. Disse ferdighetene kan lagres i SharePoint som en SharePoint-liste. Når en kandidat søker på jobber som er oppført med et sett med nødvendige kvalifikasjoner, og hvis det er betydelig samsvar mellom kandidatens ferdigheter og ferdighetene som er lagret i SharePoint, sendes en e-postvarsling. Dermed blir hastestillinger raskere fylt, fordi varslingene hjelper rekrutteringspersoner med å kontakte og ansette kandidater på tvers av organisasjonen.

Denne malen kan utvides, slik at den kan brukes på alle scenarioer som involverer SharePoint-integrering.

For å laste ned **Flyt – SharePoint-integrering**-malen, gå til [Flyt – SharePoint-integrering](https://go.microsoft.com/fwlink/?linkid=2082109) på Microsoft Download Center.

## <a name="admin-console-to-manage-talent-pools"></a>Administrasjonskonsoll for å administrere talentsamlinger

Når du aktiverer integrering med LinkedIn, oppretter Attract automatisk en LinkedIn-talentsamling. Når en rekrutterer utveksler InMail med en rekrutt via LinkedIn, oppretter Attract en profil for rekrutten, og rekrutten blir medlem av LinkedIn-talentsamlingen. Denne PowerApps-appen er nyttig for omorganisering av kandidater i talentsamlinger på basis av kompetanse.

Kjør denne PowerApps-appen som administrasjonskonsoll for å utføre følgende oppgaver:

- Angi kandidater i en talentsamling
- Legge til og fjerne kandidater fra en talentsamling
- Flytte kandidater fra én talentsamling til en annen
- Finne ut om kandidater allerede er del av en talentsamling før du flytter dem
- Kontrollere kompetansen til kandidater før du flytter dem til andre talentsamlinger

Denne PowerApps-appen bruker mange-til-mange-relasjoner, slik at du kan bruke den som en mal for andre scenarier der du må trekke ut poster som har mange-til-mange-relasjoner.

Hvis du vil laste ned malen **Administrasjonskonsoll for å administrere talentsamlinger**, går du til [Administrasjonskonsoll for å administrere talentsamlinger](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) på Microsoft Download Center.

## <a name="additional-resources"></a>Tilleggsressurser

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Overføre app mellom leiere og miljøer](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
