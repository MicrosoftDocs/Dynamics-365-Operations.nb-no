---
title: Utvide Talent med Power Apps og Power Automate
description: Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent – Attract som bruker Microsoft Power Apps og Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529640"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Utvide Talent med Power Apps og Power Automate

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Denne artikkelen beskriver noen eksempler på scenarier for utvidelsesmuligheter for Microsoft Dynamics 365 Talent: Attract som bruker Microsoft Power Apps og Microsoft Power Automate. Du kan importere løsningspakken som er tilknyttet hvert eksempel, i ditt Power Apps-miljø. Du kan deretter bruke pakkene som retningslinjer eller som utgangspunkt til å implementere scenarioene som gjelder for organisasjonen din.

> [!IMPORTANT]
> Hvis du vil bruke malene og appen som er beskrevet i denne artikkelen, "som de er", må du teste dem å være sikker på at de dekker alle scenarioene som er spesifikke for implementeringen.


## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil importere pakker, må brukerne ha **Miljøskaper**-tillatelsen.
- Hvis du vil eksportere eller importere apper, må brukerne ha en Power Apps Plan 2-lisens eller en Power Apps Plan 2-prøvelisens.

## <a name="power-automate--form-connect"></a>Power Automate – skjematilkobling

Malen for **Power Automate – skjematilkobling** kan brukes til å lese data fra Microsoft Forms og lagre den i en Common Data Service-enhet.

Denne malen kan utvides slik at den kan brukes til andre scenarioer. Her er noen eksempler:

- Registrer kandidatvurderinger.
- Lagre resultater fra kursspørreskjema.
- Kompiler et bibliotek med intervjuspørsmål for HR-administratorer.
- Registrere en kandidats evaluering av intervjuprosessen

I Microsoft Dynamics 365: Attract kan du bruke skjemaer i kandidatportalen, der kandidater fyller ut detaljer. Du kan også legge inn skjemaer som aktiviteter i en jobbmal.

Når en kandidat sender et skjema, fanger Microsoft Power Automate opp skjemainnsendingen, leser dataene og lagrer den i Common Data Service-enheten.

For å laste ned malen for **Power Automate – skjematilkobling** og den egendefinerte enhetsstrukturen, kan du gå til [Power Automate – skjematilkobling](https://go.microsoft.com/fwlink/?linkid=2081988) på Microsoft Download Center.

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePoint-integrering

Malen **Power Automate – SharePoint-integrering** kan brukes til å lese data fra en Microsoft SharePoint-liste, sammenligne listen med feltverdier for alle Common Data Service-enheter og sende resultatene av sammenligningen som en e-postvarsling. 

En organisasjon kan ha et sett med ferdigheter som den har raskt behov for. Disse ferdighetene kan lagres i SharePoint som en SharePoint-liste. Når en kandidat søker på jobber som er oppført med et sett med nødvendige kvalifikasjoner, og hvis det er betydelig samsvar mellom kandidatens ferdigheter og ferdighetene som er lagret i SharePoint, sendes en e-postvarsling. Dette forenkler fylling av påkrevde hastestillinger raskere, fordi varslingene hjelper rekrutterere å ansette kandidater på tvers av hele organisasjonen.

Denne malen kan utvides, slik at den kan brukes på alle scenarioer som involverer SharePoint-integrering.

For å laste ned malen **Power Automate – SharePoint-integrering** går du til [Power Automate – SharePoint-integrering](https://go.microsoft.com/fwlink/?linkid=2082109) på Microsoft Download Center.

## <a name="referral-app"></a>Henvisning-appen

Du kan bruke henvisningsappen for å legge til kandidater i en delt talentsamling. Henviseren kan angi **Fornavn**, **Etternavn** **E-post** og **URL-adresse for LinkedIn** når en kandidat sendes inn. Metadataene for kandidatkilden fylles deretter ut med henviserens informasjon.

Du kan bygge inn denne appen i Employee Self-Service (ESS) for innsending av henvisninger, eller du kan bruke den som en hyperkobling i bedriftsportalen og kjøre den som en frittstående app.

Hvis du vil laste ned **henvisningsappen**, går du til [Dynamics 365 Talent-utvidelsesløsning: Henvisningsapp](https://www.microsoft.com/download/details.aspx?id=58497) på Microsoft Download Center. Du kan importere denne appen og tilpasse den for å legge til flere funksjoner.

## <a name="additional-resources"></a>Tilleggsressurser

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Overføre app mellom leiere og miljøer](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
