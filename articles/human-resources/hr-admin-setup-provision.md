---
title: Klargjøre Human Resources
description: Denne artikkelen leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f2fd2b7bf9f09a61d07e1bc35ad48fe2c5d7383
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138365"
---
# <a name="provision-human-resources"></a>Klargjøre Human Resources

Denne artikkelen leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources. Denne artikkelen antar at du har kjøpt Human Resources gjennom en Cloud Solution Provider (CSP)- eller enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Human Resources-serviceplanen, og du kan ikke fullføre trinnene i denne artikkelen, kan du kontakte kundestøtte.

Det første som må gjøres, er at den globale administratoren må logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og opprette et nytt Human Resources-prosjekt. Med mindre et lisensieringsproblem hindrer deg i å klargjøre Human Resources, kreves det ikke hjelp fra kundestøtte eller Dynamics Service Engineering (DSE)-representanter.

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt

Hvis du vil bruke LCS til å administrere Human Resources-miljøene dine, må du først opprette et LCS-prosjekt.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjelp av kontoen du brukte til å abonnere på Human Resources.

2. Velg plusstegnet (**+**) for å opprette et prosjekt.

3. Velg **Microsoft Dynamics 365 Human Resources** som produktnavn og produktversjon.

4. Velg **Dynamics 365 Human Resources**-metoden.

5. Velg **Opprett**.

Hvis du vil ha informasjon om hvordan du kan komme i gang med Human Resources, se **Human Resources**-metoden som du opprettet i det nye prosjektet ditt. Når du er ferdig med å opprette prosjektet, kan du fullføre fremgangsmåten nedenfor for å klargjøre Human Resources-miljøet ditt.

## <a name="provision-a-human-resources-project"></a>Klargjøre et Human Resources-prosjekt

Når du har opprettet et LCS-prosjekt, kan du klargjøre Human Resources i et miljø.

1. I LCS prosjektet velger du flisen **Human Resources-appbehandling**.

2. Angi om dette er en Sandkasse- eller Produksjon-forekomst av Human Resources. Tidlig forhåndsvisning-funksjonene kan være tilgjengelige i Sandbox-forekomstene for å tillate tidlig tilbakemelding og testing.
   
    > [!NOTE]
    > Forekomsttypen Human Resources kan ikke endres når den er angitt. Kontroller at du har valgt riktig forekomsttype før du fortsetter.</br></br>
    > Forekomsttypen Human Resources er atskilt fra forekomsttypen i Microsoft Power Apps-miljøet, som du angir i Power Apps-administrasjonssenteret.
    
3. Velg alternativet **Omfatter demodata** hvis du vil at ditt miljø skal ta med samme demodatasett brukt i testversjonen av Human Resources. Dette er nyttig for langsiktig demo eller opplæring miljøer, og bør aldri brukes for produksjonsmiljøer.  Vær oppmerksom på at du må velge dette alternativet ved innledende distribusjon. Du kan ikke oppdatere en eksisterende distribusjon senere.

4. Human Resources klargjøres alltid i et Microsoft Power Apps-miljø for å aktivere Power Apps-integrering og -utvidelsesmuligheter. Les delen "Velge et Power Apps-miljø" i denne artikkelen før du fortsetter. Hvis du ikke allerede har et Power Apps-miljø, velger du Administrer miljøer i LCS eller navigerer til Power Apps-administrasjonssenteret. Følg deretter trinnene i [Opprette et Power Apps-miljø](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Velg miljøet som Human Resources skal klargjøres i.

6. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

   Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

7. Velg **Logg på Human Resources** for å bruke det nye miljøet ditt.

    > [!NOTE]
    > Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Human Resources i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

    > Du kan vurdere å utnytte et gratis 60-dagers [Human Resources-prøvemiljø](https://dynamics.microsoft.com/talent/overview/). Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for Human Resources. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. De er ikke ment å brukes som produksjonsmiljøer. Merk at når prøvemiljøet utløper etter 60 dager, slettes alle dataene i miljøet og de kan ikke gjenopprettes. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

## <a name="select-a-power-apps-environment"></a>Velg et Power Apps-miljø

Integreringen mellom Human Resources- og Power Apps-miljøer gjør at du kan integrere og utvide bruken av Human Resources-data ved hjelp av Power Apps-verktøy. Å forstå formålet med Power Apps-miljøer vil ikke bare hjelpe deg med å lage apper for å utvide Human Resources, men kan også hjelpe deg med å velge det riktige miljøet ved klargjøring av Human Resources. Hvis du vil ha informasjon om Power Apps-miljøer, blant annet miljøomfang, miljøtilgang og opprettelse og valg av miljø, kan du se [Kunngjøre Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Bruk følgende retningslinjer når du skal avgjøre hvilket Power Apps-miljø Human Resources skal distribueres i: 

1. Velg **Behandle miljøer** i LCS, eller gå direkte til Power Apps-administrasjonssenteret, der du kan vise eksisterende miljøer og opprette nye miljøer.

2. Ett enkelt Human Resources-miljø er tilordnet til ett enkelt Power Apps-miljø.

3. Et Power Apps-miljø inneholder Human Resources-programmet, sammen med de tilsvarende Power Apps-, Power Automate- og Common Data Service -programmene. Hvis Power Apps-miljøet slettes, slettes også appene i det. Når du klargjør et Human Resources-miljø, kan du klargjøre et miljø av typen **Prøveversjon** eller **Produksjon**. Velg miljø basert på hvordan miljøet vil bli brukt. 

4. Dataintegrering og teststrategier skal vurderes, for eksempel sandkasse, UAT eller produksjon. Vi anbefaler at du vurderer forskjellige konsekvenser for distribusjonen, fordi det ikke er enkelt å endre hvilket Human Resources-miljø som skal tilordnes til Power Apps-miljøet, senere.

5. Følgende Power Apps-miljøer kan ikke brukes for Human Resources og filtreres fra valglisten i LCS:
 
    - **Standard Power Apps-miljøer** – Selv om hver leier er klargjort automatisk med et standard Power Apps-miljø, anbefales det ikke å bruke dem med Human Resources, siden alle leierbrukere har tilgang til Power Apps-miljøet og ved en feiltakelse kan skade produksjonsdata ved testing og utforsking med Power Apps- eller Power Automate-integreringer.
   
    - **Testmiljøer** – Disse miljøene opprettes med en utløpsdato og utløper etter dette tidspunktet, noe som fører til at miljøet og eventuelle Human Resources-forekomster i miljøet fjernes automatisk.
   
    - **Områder som ikke støttes** – Human Resources støttes for øyeblikket bare i følgende områder: USA, Europa, Storbritannia, Australia, Canada og Asia.

    > [!NOTE]
    > Human Resources-miljøet klargjøres i samme område som Power Apps-miljøet klargjøres i. Overføring av et Human Resources-miljø til en annen region støttes ikke.

6. Når du har valgt det riktige miljøet som skal brukes, kan du fortsette med klargjøringsprosessen. 
 
## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet

Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Flere brukere må imidlertid eksplisitt gis tilgang. For å gi tilgang må du legge til brukere og tilordne de riktige rollene til dem i Human Resources-miljøet. Den globale administratoren som distribuerte Human Resources, må også starte både Attract og Onboard for å fullføre initialiseringen og aktivere tilgang for andre leierbrukere.  Før dette skjer, andre brukere vil ikke kunne få tilgang til Attract og Onboard og få tilgangsbruddfeil. Hvis du vil ha mer informasjon, se [Opprette nye brukere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tilordne brukere til sikkerhetsroller](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
