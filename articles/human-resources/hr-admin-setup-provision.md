---
title: Klargjøre Human Resources
description: Dette emnet leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58ffce072c8b73f4907b18c6c60b022f9a3b55f26cb785238367254021afdc28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756154"
---
# <a name="provision-human-resources"></a>Klargjøre Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet leder deg gjennom prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources. Dette emnet antar at du har kjøpt Human Resources via en Cloud Solution Provider (CSP) eller en enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Human Resources-serviceplanen, og du kan ikke fullføre trinnene i denne artikkelen, kan du kontakte kundestøtte.

Det første som må gjøres, er at den globale administratoren må logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og opprette et nytt Human Resources-prosjekt. Med mindre et lisensieringsproblem hindrer deg i å klargjøre Human Resources, kreves det ikke hjelp fra kundestøtte eller Dynamics Service Engineering (DSE)-representanter.

## <a name="provision-a-human-resources-trial-environment"></a>Klargjøre et Human Resources-prøvemiljø

Før du klargjør den første sandkasse- eller produksjonsmiljøet, kan det hende at du vil klargjøre et [Human Resources-prøvemiljø](https://go.microsoft.com/fwlink/p/?LinkId=2115962) for å validere Human Resources-funksjonaliteten. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for Human Resources. 

Prøvemiljøene er ikke ment å brukes som produksjonsmiljøer. De er begrenset til en 60-dagers prøveperiode. Når prøveperioden utløper, kan ikke miljøet alle dataene slettes eller gjenopprettes. Miljøet kan ikke konverteres til et sandkasse- eller produksjonsmiljø. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

## <a name="plan-human-resources-environments"></a>Planlegge Human Resources-miljøer

Før du oppretter ditt første Human Resources-miljø, bør du nøye planlegge miljøbehovene for prosjektet. Et basisabonnement på Human Resources omfatter to miljøer: et produksjonsmiljø og et sandkassemiljø. Det kan hende at du må kjøpe flere sandkassemiljøre for å støtte prosjektaktiviteter, avhengig av kompleksiteten i prosjektet. 

Hensyn til tilleggsmiljøer omfatter, men er ikke begrenset til, følgende:

- **Dataoverføring**: Det kan hende at du må vurdere et tilleggsmiljø for dataoverføringsaktiviteter for å tillate at sandkassemiljøet brukes til testeformål gjennom hele prosjektet. Hvis du har et ekstra miljø, kan aktiviteter for migrering av data fortsette mens testing og konfigurasjon skjer samtidig i et annet miljø.
- **Integrering**: Det kan hende at du må vurdere et tilleggsmiljø for å konfigurere og teste integreringer. Dette kan for eksempel inkludere opprinnelige integrasjoner som Ceridian Dayforce LinkedIn Talent Hub-integrasjoner, eller egendefinerte integrasjoner, for eksempel integreringer av lønn, søkersporingssystemer eller fordelssystemer og -leverandører.
- **Opplæring**: Du trenger kanskje et eget miljø som er konfigurert med et sett med opplæringsdata for å lære opp de ansatte i bruk av det nye systemet. 
- **Prosjekt med flere faser**: Du trenger kanskje et tilleggsmiljø for å støtte konfigurasjon, dataoverføring, testing eller andre aktiviteter i en prosjektfase som er planlagt etter den innledende aktiveringen av prosjektet.

 > [!IMPORTANT]
 > Det anbefales at du bruker produksjonsmiljøet i hele prosjektet som GULL-konfigurasjonsmiljø. Dette er viktig fordi du ikke kan kopiere et sandkassemiljø til et produksjonsmiljø. Når du kommer aktiverer, er derfor GULL-miljøet produksjonsmiljøet ditt, og du fullfører overgangsaktivitetene i dette miljøet.</br></br>
 > Det anbefales at du bruker sandkassemiljøet ditt eller et annet miljø til å utføre en testovergang før selve aktiveringen. Du kan gjøre dette ved å oppdatere produksjonsmiljøet med GULL-konfigurasjonen i sandkassemiljøet.</br></br>
 > Det anbefales at du har en detaljert kontrolliste for overgang som inneholder alle datapakkene som kreves for å migrere de siste dataene til produksjonsmiljøet under overgangen til aktivering.</br></br>
 > Det anbefales også at du bruker sandkassemiljøet i hele prosjektet som TEST-miljø. Hvis du trenger flere miljøer, kan organisasjonen kjøpe dem for en ekstra kostnad.</br></br>

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt

Hvis du vil bruke LCS til å administrere Human Resources-miljøene dine, må du først opprette et LCS-prosjekt.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjelp av kontoen du brukte til å abonnere på Human Resources.

   > [!NOTE]
   > For å sikre en vellykket klargjøring må kontoen du bruker til klargjøring av personalmiljøet, være tilordnet enten **Systemadministrator**- eller **Systemtilpasser**-rollen i Power Apps-miljøet som er knyttet til personalmiljøet. Se [Konfigurere brukersikkerhet på ressurser](/power-platform/admin/database-security) hvis du vil ha mer informasjon om tilordning av sikkerhetsroller til brukere i Power Platform.

2. Velg plusstegnet (**+**) for å opprette et prosjekt.

3. Velg **Microsoft Dynamics 365 Human Resources** som produktnavn og produktversjon.

4. Velg **Dynamics 365 Human Resources**-metoden.

5. Velg **Opprett**.

Hvis du vil ha informasjon om hvordan du kan komme i gang med Human Resources, se **Human Resources**-metoden som du opprettet i det nye prosjektet ditt. Når du er ferdig med å opprette prosjektet, kan du fullføre fremgangsmåten nedenfor for å klargjøre Human Resources-miljøet ditt.

## <a name="provision-a-human-resources-project"></a>Klargjøre et Human Resources-prosjekt

Når du har opprettet et LCS-prosjekt, kan du klargjøre Human Resources i et miljø.

1. I LCS prosjektet velger du flisen **Human Resources-appbehandling**.

2. Angi om dette miljøet er en Sandkasse- eller Produksjon-forekomst av Human Resources. Tidlig forhåndsvisning-funksjonene kan være tilgjengelige i Sandbox-forekomstene for å tillate tidlig tilbakemelding og testing.
   
    > [!NOTE]
    > Forekomsttypen Human Resources kan ikke endres når den er angitt. Kontroller at du har valgt riktig forekomsttype før du fortsetter.</br></br>
    > Forekomsttypen Human Resources er atskilt fra forekomsttypen i Microsoft Power Apps-miljøet, som du angir i Power Apps-administrasjonssenteret.
    
3. Velg alternativet **Omfatter demodata** hvis du vil at ditt miljø skal ta med samme demodatasett brukt i testversjonen av Human Resources. Demodata er nyttig for langsiktige demo- eller opplæringsmiljøer, og bør aldri brukes for produksjonsmiljøer. Du må velge dette alternativet ved innledende distribusjon. Du kan ikke oppdatere en eksisterende distribusjon senere.

4. Human Resources klargjøres alltid i et Microsoft Power Apps-miljø for å aktivere Power Apps-integrering og -utvidelsesmuligheter. Les delen "Velge et Power Apps-miljø" i denne artikkelen før du fortsetter. Hvis du ikke allerede har et Power Apps-miljø, velger du Administrer miljøer i LCS eller navigerer til Power Apps-administrasjonssenteret. Følg deretter trinnene i [Opprette et Power Apps-miljø](/powerapps/administrator/create-environment).

5. Velg miljøet som Human Resources skal klargjøres i.

6. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

   Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen oppdateres til **Distribuert**. Denne prosessen tar vanligvis noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

7. Velg **Logg på Human Resources** for å bruke det nye miljøet ditt.

    > [!NOTE]
    > Hvis du ennå ikke har godkjent for de endelige kravene, kan du distribuere en testforekomst av Human Resources i prosjektet. Du kan deretter bruke denne forekomsten til å teste løsningen til du godkjenner. Hvis du bruker det nye miljøet for testing, må du gjenta denne fremgangsmåten for å opprette et produksjonsmiljø.

## <a name="select-a-power-apps-environment"></a>Velg et Power Apps-miljø

Du kan integrere og utvide bruken av Human Resources-data ved hjelp av Power Apps-verktøy. Hvis du vil ha informasjon om Power Apps-miljøer, blant annet miljøomfang, miljøtilgang og opprettelse og valg av miljø, kan du se [Kunngjøre Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Bruk følgende retningslinjer når du skal avgjøre hvilket Power Apps-miljø Human Resources skal distribueres i: 

1. Velg **Administrer miljøer** i LCS. Du kan også gå direkte til Power Apps-administrasjonssenteret, der du kan vise eksisterende miljøer og opprette nye miljøer.

2. Ett enkelt Human Resources-miljø er tilordnet til ett enkelt Power Apps-miljø.

3. Et Power Apps-miljø inneholder Human Resources-programmet, sammen med de tilsvarende Power Apps-, Power Automate- og Dataverse -programmene. Hvis Power Apps-miljøet slettes, slettes også appene i det. Når du klargjør et Human Resources-miljø, kan du klargjøre et miljø av typen **Prøveversjon** eller **Produksjon**. Velg miljø basert på hvordan miljøet vil bli brukt. 

4. Dataintegrering og teststrategier skal vurderes, for eksempel sandkasse, UAT eller produksjon. Vurder forskjellige konsekvenser for distribusjonen, for det er ikke enkelt å endre hvilket Human Resources-miljø som skal tilordnes til Power Apps-miljøet, senere.

5. Du kan ikke bruke følgende Power Apps-miljøer for Human Resources. De er filtrert fra utvalgslisten i LCS:
 
    - **Standard Power Apps-miljøer** – Selv om hver leier automatisk klargjøres med et standard Power Apps-miljø, anbefaler vi ikke at du bruker dem sammen med Human Resources. Alle leierbrukere har tilgang til Power Apps-miljøet og kan skade produksjonsdata utilsiktet når de tester og utforsker med Power Apps- eller Power Automate-integreringer.
   
    - **Prøvemiljøer** – disse miljøene er opprettet med en utløpsdato. Ved utløpet fjernes miljøet og eventuelle Human Resources-forekomster i det automatisk.
   
    - **Ikke-støttede geografier** – Miljøet må være i en geografi som støttes. Hvis du vil ha mer informasjon, kan du se [Støttede geografier](hr-admin-setup-provision.md#supported-geographies).

6. Når du har valgt det riktige miljøet som skal brukes, kan du fortsette med klargjøringsprosessen. 

### <a name="supported-geographies"></a>Geografier som støttes

Personale støtter følgende geografier:

- USA
- Europa
- Storbritannia
- Australia
- Canada
- Asia 

Når du oppretter et Personale-miljø, velger du et Power Apps-miljø som skal knyttes til Personale-miljøet. Personale-miljøet klargjøres deretter i samme Azure-geografi som det valgte Power Apps-miljøet. Du kan velge hvor Human Resources-miljøet og -databasen skal ligge fysisk ved å velge geografien når du oppretter Power Apps-miljøet som skal knyttes til Human Resources-miljøet.

Du kan velge Azure-*geografien* der miljøet er klargjort, men du kan ikke velge det bestemte Azure-*området*. Automation bestemmer det bestemte området i geografien der miljøet opprettes for å optimalisere belastningsfordeling og ytelse. Du finner informasjon om Azure-geografier og -områder i dokumentasjonen på [Azure-geografier](https://azure.microsoft.com/global-infrastructure/geographies).

Dataene for Personale-miljøet ligger alltid i Azure-geografien der de er opprettet. Området vil imidlertid ikke alltid være innenfor det samme Azure-området. Av hensyn til nødgjenoppretting blir dataene replikert både i det primære Azure-området og et sekundært failover-område i geografien.

 > [!NOTE]
 > Overføring av et Human Resources-miljø fra ett Azure-området til et annet støttes ikke.

## <a name="grant-access-to-the-environment"></a>Gi tilgang til miljøet

Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Du må eksplisitt gi tilgang til flere programbrukere. Du må legge til brukere og tilordne de riktige rollene til dem i Human Resources-miljøet. Den globale administratoren som distribuerte Human Resources, må også starte både Attract og Onboard for å fullføre initialiseringen og aktivere tilgang for andre leierbrukere. Før dette skjer, andre brukere vil ikke kunne få tilgang til Attract og Onboard og få tilgangsbruddfeil. Hvis du vil ha mer informasjon, se [Opprette nye brukere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tilordne brukere til sikkerhetsroller](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
