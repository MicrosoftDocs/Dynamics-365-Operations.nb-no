---
title: Klargjøre Talent
description: Dette emnet leder deg gjennom prosessen med å klargjøre et nytt miljø for Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 2bb5dd5e29559807e40b66ad7f9c061bf510ed67
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026147"
---
# <a name="provision-talent"></a>Klargjøre Talent

[!include [banner](includes/banner.md)]

Dette emnet leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Talent. Dette emnet antar at du har kjøpt Talent gjennom en Cloud Solution Provider (CSP)- or enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Talent-serviceplanen, og du kan ikke fullføre trinnene i dette emnet, kan du kontakte kundestøtte.

Det første som må gjøres, er at den globale administratoren må logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og opprette et nytt Talent-prosjekt. Med mindre et lisensieringsproblem hindrer deg i å klargjøre Talent, kreves det ikke hjelp fra kundestøtte eller Dynamics Service Engineering (DSE)-representanter.

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt
Hvis du vil bruke LCS til å administrere Talent-miljøene dine, må du først opprette et LCS-prosjekt.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjelp av kontoen du brukte til å abonnere på Talent.
2. Velg plusstegnet (**+**) for å opprette et prosjekt.
3. Velg **Microsoft Dynamics 365 Talent** som produktnavn og produktversjon.
4. Velg **Dynamics 365 Talent**-metoden.
5. Velg **Opprett**.

Hvis du vil ha informasjon om hvordan du kan komme i gang med Talent, se **Talent**-metoden som du opprettet i det nye prosjektet ditt. Når du er ferdig med å opprette prosjektet, kan du fullføre fremgangsmåten nedenfor for å klargjøre Talent-miljøet ditt.

## <a name="provision-a-talent-project"></a>Klargjøre et Talent-prosjekt
Når du har opprettet et LCS-prosjekt, kan du klargjøre Talent i et miljø.

1. I LCS prosjektet velger du flisen **Talent-appbehandling**.
2. Angi om dette er en Sandkasse- eller Produksjon-forekomst av Talent. Tidlig forhåndsvisning-funksjonene kan være tilgjengelige i Sandbox-forekomstene for å tillate tidlig tilbakemelding og testing. 
    > [!NOTE]
    > Forekomsttypen Talent er atskilt fra forekomsttypen i PowerApps-miljøet, som du angir i PowerApps-administrasjonssenteret.
3. Velg alternativet **Omfatter demodata** hvis du vil at ditt miljø skal ta med samme demodatasett brukt i testversjonen av Talent. Dette er nyttig for langsiktig demo eller opplæring miljøer, og bør aldri brukes for produksjonsmiljøer.  Vær oppmerksom på at du må velge dette alternativet ved innledende distribusjon. Du kan ikke oppdatere en eksisterende distribusjon senere.
4. Talent klargjøres alltid i et Microsoft PowerApps-miljø for å aktivere PowerApps-integrering og -utvidelsesmuligheter. Les delen "Velge et PowerApps-miljø" i dette emnet før du fortsetter. Hvis du ikke allerede har et PowerApps-miljø, velger du Administrer miljøer i LCS eller navigerer til PowerApps-administrasjonssenteret. Følg deretter trinnene i [Opprette et PowerApps-miljø](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > Hvis du vil vise eksisterende miljøer eller opprette nye miljøer, må leieradministratoren som klargjør Talent, være tilordnet til PowerApps P2-lisensen. Hvis organisasjonen ikke har en PowerApps P2-lisens, kan du få en fra CSP-en eller fra [PowerApps-prissiden](https://powerapps.microsoft.com/pricing/).

5. Velg miljøet som Talent skal klargjøres i.
6. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

    Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

7. Velg **Logg på Talent** for å bruke det nye miljøet ditt.

    > [!NOTE]
    > Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Talent i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

    > Siden bare to LCS-miljøer er tillatt som en del av Talent-abonnementet, kan du vurdere et gratis 60-dagers [Talent-prøvemiljø](https://dynamics.microsoft.com/talent/overview/). Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for kjerne-HR. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. De er ikke ment å brukes som produksjonsmiljøer. Merk at når prøvemiljøet utløper etter 60 dager, slettes alle dataene i miljøet og de kan ikke gjenopprettes. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

## <a name="select-a-powerapps-environment"></a>Velg et PowerApps-miljø

Integreringen mellom Talent- og PowerApps-miljøer gjør at du kan integrere og utvide bruken av Talent-data ved hjelp av PowerApps-verktøy. Å forstå formålet med PowerApps-miljøer vil ikke bare hjelpe deg med å lage apper for å utvide Talent, men kan også hjelpe deg med å velge det riktige miljøet ved klargjøring av Talent. Hvis du vil ha informasjon om PowerApps-miljøer, blant annet miljøomfang, miljøtilgang og opprettelse og valg av miljø, kan du se [Kunngjøre PowerApps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Bruk følgende retningslinjer når du skal avgjøre hvilket PowerApps-miljø Talent skal distribueres i: 

1. Velg **Behandle miljøer** i LCS, eller gå direkte til PowerApps-administrasjonssenteret, der du kan vise eksisterende miljøer og opprette nye miljøer.
2. Ett enkelt Talent-miljø er tilordnet til ett enkelt PowerApps-miljø.
3. Et PowerApps-miljø inneholder Talent-programmet, sammen med de tilsvarende PowerApps-, Flow- og Common Data Service-programmene. Hvis PowerApps-miljøet slettes, slettes også appene i det. Når du klargjør et Talent-miljø, kan du klargjøre et miljø av typen **Prøveversjon** eller **Produksjon**. Velg miljø basert på hvordan miljøet vil bli brukt. 
4. Dataintegrering og teststrategier skal vurderes, for eksempel sandkasse, UAT eller produksjon. Vi anbefaler at du vurderer forskjellige konsekvenser for distribusjonen, fordi det ikke er enkelt å endre hvilket Talent-miljø som skal tilordnes til PowerApps-miljøet, senere.
5. Følgende PowerApps-miljøer kan ikke brukes for Talent og filtreres fra valglisten i LCS:
 
    - **Standard PowerApps-miljøer** – Selv om hver leier er klargjort automatisk med et standard PowerApps-miljø, anbefales det ikke å bruke dem med Talent, siden alle leierbrukere har tilgang til PowerApps-miljøet og ved en feiltakelse kan skade produksjonsdata ved testing og utforsking med PowerApps eller Flow-integreringer.
   
    - **Testmiljøer** – Disse miljøene opprettes med en utløpsdato og utløper etter dette tidspunktet, noe som fører til at miljøet og eventuelle Talent-forekomster i miljøet fjernes automatisk.
   
    - **Områder som ikke støttes** – Talent støttes for øyeblikket bare i følgende områder: USA, Europa, Storbritannia, Australia, Canada og Asia.
  
6. Når du har valgt det riktige miljøet som skal brukes, kan du fortsette med klargjøringsprosessen. 
 
## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet
Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Flere brukere må imidlertid eksplisitt gis tilgang. For å gi tilgang må du legge til brukere og tilordne de riktige rollene til dem i Core HR-miljøet. Globale administratoren som distribuerte Talent, må også starte både Attract og Onboard for å fullføre initialiseringen og aktivere tilgang for andre leierbrukere.  Før dette skjer, andre brukere vil ikke kunne få tilgang til Attract og Onboard og få tilgangsbruddfeil. Hvis du vil ha mer informasjon, se [Opprette nye brukere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tilordne brukere til sikkerhetsroller](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
