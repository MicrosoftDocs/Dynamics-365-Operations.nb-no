---
title: "Klargjøre Microsoft Dynamics 365 for Talent"
description: "Dette emnet leder deg gjennom prosessen med å klargjøre et nytt miljø for Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: nb-no
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Klargjøre Microsoft Dynamics 365 for Talent
Dette emnet leder deg gjennom prosessen med å klargjøre et nytt miljø for Microsoft Dynamics 365 for Talent. Dette emnet antar at du har kjøpt Talent gjennom en Cloud Solution Provider (CSP)- or enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Talent-serviceplanen, og du kan ikke fullføre trinnene i dette emnet, kan du kontakte kundestøtte.

Det første som må gjøres, er at den globale administratoren må logge på [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) og opprette et nytt Talent-prosjekt. Med mindre et lisensieringsproblem hindrer deg i å klargjøre Talent, kreves det ikke hjelp fra kundestøtte eller Dynamics Service Engineering (DSE)-representanter.

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt
Hvis du vil bruke LCS til å administrere Talent-miljøene dine, må du først opprette et LCS-prosjekt.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjelp av kontoen du brukte til å abonnere på Talent.
2. Velg plusstegnet (**+**) for å opprette et prosjekt.
3. Velg **Microsoft Dynamics 365 for Talent** som produktnavn og produktversjon.
4. Velg **Dynamics 365 for Talent**-metoden.
5. Velg **Opprett**.

Hvis du vil ha informasjon om hvordan du kan komme i gang med Talent, se **Talent**-metoden som du opprettet i det nye prosjektet ditt. Når du er ferdig med å opprette prosjektet, kan du fullføre fremgangsmåten nedenfor for å klargjøre Talent-miljøet ditt.

## <a name="provision-a-talent-project"></a>Klargjøre et Talent-prosjekt
Når du har opprettet et LCS-prosjekt, kan du klargjøre Talent i et miljø.

1. I LCS prosjektet velger du flisen **Talent-appbehandling**.
2. Talent klargjøres alltid i et Microsoft PowerApps-miljø for å aktivere PowerApps-integrering og -utvidelsesmuligheter. Hvis du ikke allerede har et PowerApps-miljø, følger du trinnene i delen "Opprette en nytt PowerApps-miljø (hvis nødvendig)" i dette emnet før du fortsetter.

    > [!NOTE]
    > Hvis du vil vise eksisterende miljøer eller opprette nye miljøer, må leieradministratoren som klargjør Talent, være tilordnet til PowerApps P2-lisensen. Hvis organisasjonen ikke har en PowerApps P2-lisens, kan du få en fra CSP-en eller fra [PowerApps-prisingssiden](https://powerapps.microsoft.com/en-us/pricing/).

3. Velg **Legg til**, og velg deretter miljøet som Talent skal klargjøres for.
4. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

    Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis bare noen få minutter. Hvis du klargjøringen mislykkes, må du kontakte kundestøtte.

6. Velg **Logg på Talent** for å bruke det nye miljøet ditt.

> [!NOTE]
> Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Talent i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

## <a name="create-a-new-powerapps-environment-if-required"></a>Opprette et ny PowerApps-miljø (hvis nødvendig)
1. Velg **Administrer miljøer** i LCS. Du tas til [PowerApps-administrasjonssenteret](https://preview.admin.powerapps.com/environments), der du kan vise eksisterende miljøer og opprette nye miljøer.
2. Velg (**+**) **Nytt miljø**-knappen.
3. Angi et unikt navn for miljøet, og velg plasseringen du vil distribuere til.

    > [!NOTE]
    > Talent er ikke tilgjengelig i alle områder. Derfor må du kontrollere tilgjengelighet før du velger plassering for ditt miljø.

4. Når du blir spurt om du vil opprette en database, velger du **Opprett database** for å opprette Common Data Service (CDS)-databasen som må være vert for en del av Talent-dataene dine. Når du oppretter en database, kan du også integrere PowerApps-programmer med Talent.
5. Du blir spurt om tilgangsnivået du vil bruke for databasen. Vi anbefaler at du velger **Begrens tilgang** fordi dette alternativet hindrer at Talent-brukere får direkte tilgang til sensitive data ved hjelp av et PowerApps-program.
6. CDS-databasen som opprettes, inneholder demonstrasjonsdata. Disse demodataene er nyttige fordi du kan bruke demodatafirmaet for testing, eller til å opprette oppgaveopptak eller oppgaveveiledninger. Demodataene legger imidlertid til inaktive ansatte og fiktive adresser blant annen informasjon i produksjonsmiljøet. Hvis du vil fjerne demodataene, kan du bruke følgende fremgangsmåte når du er ferdig med å opprette CDS-databasen:

    > [!IMPORTANT]
    > Hvis du tidligere opprettet en CDS-database og angav noen av firmaets produksjonsdata i den, må du være oppmerksom på at disse trinnene fjerner **alle** dataene i den valgte databasen, til og med firmaets produksjonsdata.

    1. Logg på [PowerApps](https://preview.web.powerapps.com/home), og gå til miljøet som du opprettet i trinn 2.
    2. Velg **Enheter**. På høyre side av siden velger du ellipsen (**...**), og velger deretter **Fjern alle data**.
    3. Velg **Slett data** for å bekrefte at du vil fjerne dataene. Denne handlingen fjerner alle demodataene som er inkludert i CDS-en som standard. Den fjerner også alle andre data som er angitt i den valgte databasen.

Nå kan du bruke det nye miljøet ditt.

