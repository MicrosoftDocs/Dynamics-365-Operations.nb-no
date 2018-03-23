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
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: e4459e8be4bfab8e0789744eacd533286b6c05e0
ms.contentlocale: nb-no
ms.lasthandoff: 03/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Klargjøre Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

Dette emnet leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 for Talent. Dette emnet antar at du har kjøpt Talent gjennom en Cloud Solution Provider (CSP)- or enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Talent-serviceplanen, og du kan ikke fullføre trinnene i dette emnet, kan du kontakte kundestøtte.

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

    Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis bare noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

6. Velg **Logg på Talent** for å bruke det nye miljøet ditt.

> [!NOTE]
> Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Talent i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

> [!NOTE]
> Talentmiljøer som klargjøres gjennom LCS, inneholder ikke demodata som er konfigurert for personaloppgaver, eller som er spesifikke for Talent. Hvis du trenger et miljø som inneholder demodata, anbefaler vi at du registrerer deg for et gratis 60-dagers [Talent-prøvemiljø](https://dynamics.microsoft.com/en-us/talent/overview/). Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for kjerne-HR. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. De er ikke ment å brukes som produksjonsmiljøer. Merk at når prøvemiljøet utløper etter 60 dager, slettes alle dataene i miljøet og de kan ikke gjenopprettes. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

## <a name="create-a-new-powerapps-environment-if-required"></a>Opprette et ny PowerApps-miljø (hvis nødvendig)
Integreringen mellom Talent- og PowerApps-miljøer gjør at du kan integrere og utvide bruken av Talent-data ved hjelp av PowerApps-verktøy. En forståelse av formålet med PowerApps-miljøer hjelper deg med å lage programmer som oppfyller behovene du har for å utvide Talent. For informasjon om PowerApps-miljøer, blant annet miljøomfang, miljøtilgang og opprettelse og valg av miljø, kan du se [Kunngjøre PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Ettersom hver leier får klargjort automatisk et standard PowerApps-miljø, er det kanskje ikke det beste miljøet som kan brukes for Talent-distribusjonen. Dataintegrering og testing av strategier bør vurderes i dette trinnet, så vi anbefaler at du vurderer konsekvensene som kan påvirke virkningen på distribusjonen fordi noen beslutningen ikke er enkle å endre senere. 

Selv om hver leier er klargjort automatisk i et standard PowerApps-miljø, er kanskje ikke dette miljøet det beste for Talent-distribusjonen. Dataintegrering og testestrategier må vurderes i dette trinnet. Vi anbefaler derfor at du vurderer forskjellige konsekvenser for distribusjonen, fordi det ikke er enkelt å endre PowerApps-miljøet senere.

1. Velg **Administrer miljøer** i LCS. Du tas til [PowerApps-administrasjonssenteret](https://preview.admin.powerapps.com/environments), der du kan vise eksisterende miljøer og opprette nye miljøer.
2. Velg **Nytt miljø**.
3. Angi et unikt navn for miljøet, og velg plasseringen du vil distribuere til.

    > [!NOTE]
    > Talent er ikke tilgjengelig i alle områder. Derfor må du kontrollere tilgjengelighet før du velger plassering for ditt miljø.

4. Når du blir spurt om du vil opprette en database, velger du **Opprett database** for å opprette Common Data Service (CDS)-databasen som må være vert for en del av Talent-dataene dine. Når du oppretter en database, kan du også integrere PowerApps-programmer med Talent.
5. Du blir spurt om tilgangsnivået som skal brukes for databasen. Vi anbefaler at du velger **Begrens tilgang** fordi dette alternativet hindrer at Talent-brukere får direkte tilgang til sensitive data ved hjelp av et PowerApps-program.
6. CDS-databasen som opprettes, inneholder demodata som legger til inaktive ansatte og fiktive adresser blant annen informasjon i produksjonsmiljøet. Hvis du vil fjerne demodataene, kan du bruke følgende fremgangsmåte når du er ferdig med å opprette CDS-databasen:

    > [!IMPORTANT]
    > Hvis du tidligere opprettet en CDS-database og angav noen av firmaets produksjonsdata i den, vil disse trinnene fjerne **alle** dataene i den valgte databasen, til og med firmaets produksjonsdata.

    1. Logge på [PowerApps](https://preview.web.powerapps.com/home)
    2. Velg miljøet som du opprettet i trinn 2, i rullegardinlisten øverst til høyre.
    3. Utvid **Common Data Service** i navigasjonsruten til venstre, og velg deretter **Enheter**.
    4. På høyre side av siden velger du ellipsen (**...**), og velger deretter **Fjern alle data**.
    5. Velg **Slett data** for å bekrefte at du vil fjerne dataene. Denne handlingen fjerner alle demodataene som er inkludert i CDS-en som standard. Den fjerner også alle andre data som er angitt i den valgte databasen.

Nå kan du bruke det nye miljøet ditt.

## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet
Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Flere brukere må imidlertid eksplisitt gis tilgang. For å gi tilgang må du [legge til brukere](../dev-itpro/sysadmin/tasks/create-new-users.md) og [tilordne de riktige rollene til dem](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) i kjerne-HR-miljøet. Du må også legge til disse brukerne i PowerApps-miljøet, slik at de får tilgang til Attract and Onboard-programmene. Fremgangsmåten er beskrevet her. Hvis du trenger hjelp til å fullføre trinnene, kan du se blogginnlegget [Introdusere PowerApps-administrasjonssenteret](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/) .

Denne prosedyren fullføres av den globale administratoren som distribuerte Talent-miljøet.

1. Åpne [PowerApps-administrasjonssenteret](https://preview.admin.powerapps.com/environments).
2. Merk av for de aktuelle miljøene.
3. Legg til nødvendige brukere til rollen **Miljøskaper** under kategorien **Sikkerhet**.

Merk at dette siste trinnet der du manuelt legger til brukere i PowerApps-miljøet, er midlertidig. Til slutt vil det bli fullført automatisk når brukere legges til i kjerne-HR.

