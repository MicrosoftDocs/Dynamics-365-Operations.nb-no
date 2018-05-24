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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 343e372ad9e29372649e975a5bee16e8913b66c8
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Klargjøre Microsoft Dynamics 365 for Talent

[!include [banner](includes/banner.md)]

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
2. Talent klargjøres alltid i et Microsoft PowerApps-miljø for å aktivere PowerApps-integrering og -utvidelsesmuligheter. Les delen "Velge et PowerApps-miljø" i dette emnet før du fortsetter. 
3. Hvis du ikke allerede har et PowerApps-miljø, følger du trinnene i delen "Opprette en nytt PowerApps-miljø (hvis nødvendig)" i dette emnet før du fortsetter.

    > [!NOTE]
    > Hvis du vil vise eksisterende miljøer eller opprette nye miljøer, må leieradministratoren som klargjør Talent, være tilordnet til PowerApps P2-lisensen. Hvis organisasjonen ikke har en PowerApps P2-lisens, kan du få en fra CSP-en eller fra [PowerApps-prisingssiden](https://powerapps.microsoft.com/en-us/pricing/).

4. Velg **Legg til**, og velg deretter miljøet som Talent skal klargjøres for.
5. Velg alternativet "Omfatter demodata" hvis du vil at ditt miljø skal ta med samme demodatasett brukt i testversjonen av Talent.  Dette er nyttig for langsiktig demo eller opplæring miljøer, og bør aldri brukes for produksjonsmiljøer.  Vær oppmerksom på at du må velge dette alternativet ved distribusjon, og kan ikke oppdatere en eksisterende distribusjon senere.
6. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

    Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis bare noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

7. Velg **Logg på Talent** for å bruke det nye miljøet ditt.

> [!NOTE]
> Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Talent i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

> [!NOTE]
> Siden bare to LCS miljøer er tillatt som en del av Talent-abonnementet, kan du også vurdere en gratis 60-dagers [Talent-prøvemiljø](https://dynamics.microsoft.com/en-us/talent/overview/). Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for kjerne-HR. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. De er ikke ment å brukes som produksjonsmiljøer. Merk at når prøvemiljøet utløper etter 60 dager, slettes alle dataene i miljøet og de kan ikke gjenopprettes. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

## <a name="select-a-powerapps-environment"></a>Velge et PowerApps-miljø

Integreringen mellom Talent- og PowerApps-miljøer gjør at du kan integrere og utvide bruken av Talent-data ved hjelp av PowerApps-verktøy. Å forstå formålet med PowerApps-miljøer vil ikke bare hjelpe deg med å lage apper for å utvide Talent, men kan også hjelpe deg med å velge det riktige miljøet ved klargjøring av Talent. For informasjon om PowerApps-miljøer, blant annet miljøomfang, miljøtilgang og opprettelse og valg av miljø, kan du se [Kunngjøre PowerApps-miljøer](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Bruk følgende retningslinjer når du skal avgjøre hvilket PowerApps-miljø Talent skal distribueres i: 
1. Velg Behandle miljøer i LCS, eller gå direkte til PowerApps-administrasjonssenteret, der du kan vise eksisterende miljøer og opprette nye miljøer.
2. Ett enkelt Talent-miljø er tilordnet til ett enkelt PowerApps-miljø.
3. Et PowerApps-miljø inneholder Talent-programmet, sammen med de tilsvarende PowerApps-, Flyt- og CDS-programmene. Hvis PowerApps-miljøet slettes, slettes også appene i det.
4. Dataintegrering og teststrategier skal vurderes, for eksempel: Sandkasse, UAT, Produksjon. Vi anbefaler derfor at du vurderer forskjellige konsekvenser for distribusjonen, fordi det ikke er enkelt å endre hvilket Talent-miljø som skal tilordnes til PowerApps-miljøet senere.
5. Følgende PowerApps-miljøer kan ikke brukes for Talent og filtreres fra valglisten i LCS:
 
    **CDS 2.0-miljøer** CDS 2.0 er offentlig tilgjengelig fra 21. mars 2018, men Talent støtter ennå ikke CDS 2.0. Selv om du kan vise og opprette CDS 2.0-databaser i PowerApps-administrasjonssenteret, vil de ikke kunne brukes i Talent. Alternativet for å bruke CDS 2.0-miljøer i Talent-distribusjoner vil være tilgjengelig på et senere tidspunkt.
   
   > [!Note]
   > For å skille mellom CDS 1.0- og 2.0-miljøer i administrasjonsportalen velger du et miljø og ser **Detaljer**. CDS 2.0-miljøer refererer alle til det faktum at "Du kan administrere disse innstillingene i Dynamics 365 Administration Center," velge en instansversjon og ikke ha en Database-kategori. 
 
   **Standard PowerApps-miljøer** Selv om hver leier er klargjort automatisk med et standard PowerApps-miljø, anbefales det ikke å bruke dem med Talent siden alle leierbrukere har tilgang til PowerApps-miljøet og ved en feiltakelse kan skade produksjonsdata ved testing og utforsking med PowerApps eller Flyt-integreringer.
   
   <strong>Testversjonsmiljøer</strong> Miljøer med et navn som "TestDrive – alias@domain" opprettes med en utløpsdato på 60 dager og utløper etter dette tidspunktet, noe som fører til at miljøet fjernes automatisk.
   
   **Områder som ikke støttes** Talent støttes for øyeblikket bare i følgende områder: USA, Europa og Australia.
  
6. Det finnes ingen bestemt handling som skal utføres når du har valgt det riktige miljøet du vil bruke. Fortsett med klargjøringen. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Opprette et ny PowerApps-miljø (hvis nødvendig)

Kjør et PowerShell-skript for å opprette et nytt PowerApps-miljø for Talent i forbindelse med leieradministratoren som har PowerApps Plan 2-lisensen. Skriptet automatiserer trinnene nedenfor:


 + Oppretting av et PowerApps-miljø
 + Oppretting av en CDS 1.0-database
 + Fjern alle eksempeldata i CDS 1.0-databasen


Fullfør fremgangsmåten nedenfor for å kjøre skriptet:

1. Last ned filen ProvisionCDSEnvironment.zip fra følgende plassering: [ProvisionCDSEnvironment-skript](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Fra nedlastingsmappen, høyreklikk filen ProvisionCDSEnvironment.zip nettopp lastet ned og velg **Egenskaper**.  Hvis det er en sikkerhetsmelding nederst i dialogboksen som sier "Denne filen kommer fra en annen datamaskin, og kan være blokkert for å beskytte datamaskinen", merker du av for **Fjern blokkering**, deretter klikk **Bruk** og **OK**.

3. Pakk ut hele innholdet i filen ProvisionCDSEnviroinment.zip til en mappe, som ikke kan være rotmappen.

4. Kjør Windows PowerShell- eller Windows PowerShell ISE-programmet som administrator.

   Se emnet [Angi policyen for kjøring](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) hvis du vil ha mer informasjon om hvordan du angir policyen for kjøring slik at skript kan kjøres. Vi foreslår at du bruker følgende "Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process", men pass på å følge dine retningslinjer for sikkerhet i firmaet, og lukk PowerShell-vinduet når du er ferdig. 
  
5. I PowerShell går du til mappen der du pakket ut filen, og kjører følgende kommando, der du erstatter verdier som anvist nedenfor:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** skal erstattes med navnet på ditt miljø. Dette navnet vises i LCS og vil være synlig når brukere velger hvilket Talent-miljø som skal brukes. 

   **YourLocation** skal erstattes med en av de støttede områdene for Talent: USA, Europa, Australia. 

   **-Dealjert** er valgfritt og gir detaljert informasjon som skal sendes til kundestøtte hvis det oppstår problemer.

6. Fortsett med klargjøringen.
 

## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet
Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Flere brukere må imidlertid eksplisitt gis tilgang. For å gi tilgang må du [legge til brukere](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [tilordne de riktige rollene til dem](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) i kjerne-HR-miljøet. Globale administratoren som distribuerte Talent, må også starte både Attract- og Onboard-programmene for å fullføre initialiseringen og aktivere tilgang for andre leierbrukere.  Før dette skjer, andre brukere vil ikke kunne få tilgang til Attract og Onboard og få tilgangsbruddfeil.


