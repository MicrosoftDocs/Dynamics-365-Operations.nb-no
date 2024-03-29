---
title: Klargjør Human Resources
description: Denne artikkelen forklarer prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc44b52e2f7662fc6be609562cec903a8755d1b
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178511"
---
# <a name="provision-human-resources"></a>Klargjør Human Resources

_**Gjelder For:** Human Resources i den frittstående infrastrukturen_ 

> [!NOTE]
> Fra og med juni 2022 kan Human Resources-miljøer kun distribueres i infrastrukturen i økonomi- og driftsapper. Hvis du vil ha mer informasjon , kan du se [Klargjøring av Human Resources i infrastrukturen i Finance and Operations](hr-admin-setup-provision-fo.md).

Denne artikkelen forklarer prosessen med å klargjøre et nytt produksjonsmiljø for Microsoft Dynamics 365 Human Resources. 

## <a name="prerequisites"></a>Forutsetninger

Før du kan begynne med å klargjøre et nytt produksjonsmiljø, må følgende forutsetninger være på plass :

- Du har kjøpt Human Resources via en Cloud Solution Provider (CSP) eller en enterprise architecture (EA)-avtale. Hvis du har en eksisterende Microsoft Dynamics 365-lisens som allerede inneholder Human Resources-serviceplanen, og du kan ikke fullføre trinnene i denne artikkelen, kan du kontakte kundestøtte.

- Den globale administratoren har logget seg på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og opprettet et nytt Human Resources-prosjekt. 

## <a name="provision-a-human-resources-trial-environment"></a>Klargjøre et Human Resources-prøvemiljø

>[!NOTE]
> Fra og med april 2022 vil ikke Human Resources-prøvemiljøene være tilgjengelige i den frittstående appen. Potensielle kunder som er interessert i å evaluere Human Resources-funksjonene i økonomi- og driftsapper, kan gjøre dette ved hjelp av den gratis 30-dagers prøveversjonen sammen med demodataene. Dynamics 365 Finance inneholder Human Resources-funksjonene som er innlemmet i Finance-infrastrukturen gjennom sammenslåingen av den frittstående appen. Hvis du vil ha mer informasjon, kan du se [Sammenslåing av HR-tilbud sammenfatter funksjoner for kunder](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Hvis du vil ha mer informasjon om Dynamics 365 Finance-prøveversjoner, kan du se den trinnvise [veiledningen](../fin-ops-core/fin-ops/get-started/before-you-buy.md). 


Før du klargjør den første sandkasse- eller produksjonsmiljøet, kan det hende at du vil klargjøre et [Human Resources-prøvemiljø](https://go.microsoft.com/fwlink/p/?LinkId=2115962) for å validere Human Resources-funksjonaliteten. Prøvemiljøer inneholder fiktive data som kan brukes til å utforske programmet på en sikker måte. Selv om et prøvemiljø eies av brukeren som ba om det, kan andre brukere inviteres gjennom systemadministrasjonsopplevelsen for Human Resources. 

Prøvemiljøer bidrar til å evaluere personalfunksjonaliteten for personer som ikke allerede har tilgang til et Human Resources-miljø. Hvis du klargjør et prøvemiljø, og den godkjente brukeren allerede har tilgang til ett eller flere eksisterende Personale-miljøer, blir brukeren sendt videre til det eksisterende miljøet eller listen over miljøer.

Prøvemiljøene er ikke ment å brukes som produksjonsmiljøer. De er begrenset til en 30-dagers prøveperiode. Når prøveperioden utløper, blir miljøet og alle dataene slettet, og de kan ikke gjenopprettes. Miljøet kan ikke konverteres til et sandkasse- eller produksjonsmiljø. Du kan registrere deg for et nytt prøvemiljø etter det eksisterende miljøet er utløpt.

Når du oppretter et prøvemiljø for Human Resources, opprettes det også et Power Apps prøvemiljø i leieren og knyttes til Human Resources-miljøet. Miljøet Power Apps, kalt "TestDrive", har den samme prøveperioden som Human Resources-miljøet.

> [!NOTE]
> Klargjøring av et prøvemiljø for Human Resources vil mislykkes hvis den godkjente brukeren ikke har tillatelse til å opprette Power Apps prøvemiljøer. Brukeren må være inkludert i brukergruppen som kan opprette prøvemiljøer i Power Platform administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Kontrollere hvem som kan opprette og administrere miljøer i Power Platform administrasjonssenteret](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Planlegge Human Resources-miljøer

Før du oppretter ditt første Human Resources-miljø, bør du nøye planlegge miljøbehovene for prosjektet. Et basisabonnement på Human Resources omfatter to miljøer: et produksjonsmiljø og et sandkassemiljø. Det kan hende at du må kjøpe flere sandkassemiljøer for å støtte prosjektaktiviteter, avhengig av kompleksiteten i prosjektet. 

Hensyn for tilleggsmiljøer:

- **Dataoverføring**: Datamigreringsaktiviteter gjør at sandkassemiljøet kan brukes til testeformål gjennom hele prosjektet. Hvis du har et ekstra miljø, kan aktiviteter for migrering av data fortsette mens testing og konfigurasjon skjer samtidig i et annet miljø.
- **Integrering**: Konfigurer og test integreringer, som kan omfatte opprinnelige integreringer, for eksempel Ceridian Dayforce, eller egendefinerte integreringer.
- **Opplæring**: Du trenger kanskje et eget miljø som er konfigurert med et sett med opplæringsdata for å lære opp de ansatte i bruken av det nye systemet. 
- **Prosjekt med flere faser**: Støtt konfigurasjon, dataoverføring, testing eller andre aktiviteter i en prosjektfase som er planlagt etter den innledende aktiveringen av prosjektet.

 > [!IMPORTANT]
 > Når du vurderer miljøet, anbefaler vi følgende:
 > - Bruk produksjonsmiljøet i hele prosjektet som GULL-konfigurasjonsmiljø. Dette er viktig fordi du ikke kan kopiere et sandkassemiljø til et produksjonsmiljø. Når du kommer aktiverer, er derfor GULL-miljøet produksjonsmiljøet ditt, og du fullfører overgangsaktivitetene i dette miljøet.</br></br>
 > - Bruk sandkassemiljøet ditt eller et annet miljø til å utføre en testovergang før selve aktiveringen. Du kan gjøre dette ved å oppdatere produksjonsmiljøet med GULL-konfigurasjonen i sandkassemiljøet.</br></br>
 > - Lag en detaljert kontrolliste for overgang som inneholder alle datapakkene som kreves for å migrere de siste dataene til produksjonsmiljøet under overgangen til aktivering.</br></br>
 > - Bruk sandkassemiljøet i hele prosjektet som TEST-konfigurasjonsmiljø. Hvis du trenger flere miljøer, kan organisasjonen kjøpe dem for en ekstra kostnad.</br></br>

## <a name="create-an-lcs-project"></a>Opprette et LCS-prosjekt

Hvis du vil bruke LCS til å administrere Human Resources-miljøene dine, må du først opprette et LCS-prosjekt.

1. Logg på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjelp av kontoen du brukte til å abonnere på Human Resources.

   > [!NOTE]
   > For å sikre en vellykket klargjøring må kontoen du bruker til klargjøring av personalmiljøet, være tilordnet enten **Systemadministrator**- eller **Systemtilpasser**-rollen i Power Apps-miljøet som er knyttet til personalmiljøet. Hvis du vil ha mer informasjon om tilordning av sikkerhetsroller til brukere i Power Platform, kan du se [Konfigurere brukersikkerhet på ressurser](/power-platform/admin/database-security).

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
    
3. Velg alternativet **Omfatter demodata** hvis du vil at ditt miljø skal ta med samme demodatasett som er brukt i testmiljøet i Human Resources. Demodata er nyttig for langsiktige demo- eller opplæringsmiljøer, og bør aldri brukes for produksjonsmiljøer. Du må velge dette alternativet ved innledende distribusjon. Du kan ikke oppdatere en eksisterende distribusjon senere.

4. Human Resources klargjøres alltid i et Microsoft Power Apps-miljø for å aktivere Power Apps-integrering og -utvidelsesmuligheter. Les delen "Velge et Power Apps-miljø" i denne artikkelen før du fortsetter. Hvis du ikke allerede har et Power Apps-miljø, velger du Administrer miljøer i LCS eller navigerer til Power Apps-administrasjonssenteret. Følg deretter trinnene i [Opprette et Power Apps-miljø](/powerapps/administrator/create-environment).

5. Velg miljøet som Human Resources skal klargjøres i.

6. Velg **Ja** for å godta vilkårene og begynne distribusjonen.

   Det nye miljøet ditt vises i listen over miljøer i navigasjonsruten på venstre side. Men du kan ikke begynne å bruke miljøet før distribusjonsstatusen er **Distribuert**. Denne prosessen tar vanligvis noen få minutter. Hvis klargjøringsprosessen mislykkes, må du kontakte kundestøtte.

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

5. Følgende Power Apps-miljøer kan ikke brukes for Human Resources. De er filtrert fra utvalgslisten i LCS:
 
    - **Standard Power Apps-miljøer** – Selv om hver leier automatisk klargjøres med et standard Power Apps-miljø, anbefaler vi ikke at du bruker dem sammen med Human Resources. Alle leierbrukere har tilgang til Power Apps-miljøet og kan skade produksjonsdata utilsiktet når de tester og utforsker med Power Apps- eller Power Automate-integreringer.
   
    - **Prøvemiljøer** – disse miljøene er opprettet med en utløpsdato. Ved utløpet fjernes miljøet og eventuelle Human Resources-forekomster i det automatisk.
   
    - **Ikke-støttede geografier** – Miljøet må være i en geografi som støttes. Hvis du vil ha mer informasjon, kan du se [Støttede geografier](hr-admin-setup-provision.md#supported-geographies).

6. Skrivefunksjoner for dobbel skriving for integrering av Personale-data med Power Apps-miljøet kan bare brukes hvis alternativet **Aktiver Dynamics 365-apper** er valgt for miljøet. Hvis du vil ha mer informasjon, kan du se [Startside for dobbel skriving](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md).

    > [!NOTE]
    > Alternativet **Aktiver Dynamics 365-apper** må være valgt når Power Apps-miljøet opprettes. Hvis alternativet ikke er valgt samtidig som klargjøringen, kan du ikke bruke dobbel skriving for å integrere data mellom Dynamics 365 Human Resources og Power Apps-miljøet, eller installere Dynamics 365-apper som Dynamics 365 Sales og Field Service i miljøet. Dette alternativet kan ikke tilbakeføres. 
    > -  Human Resources støtter ikke endring av den koblede Dataverse-forekomsten når Human Resources er distribuert i den. </br></br>
    > Hvis du vil ha mer informasjon, kan du se [Noen viktige hensyn når du oppretter et nytt miljø](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) på Power Platform-dokumentasjonsområdet.  

7. Når du har valgt det riktige miljøet som skal brukes, kan du fortsette med klargjøringsprosessen. 

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

Som standard har den globale administratoren som opprettet miljøet, tilgang til den. Du må eksplisitt gi tilgang til flere programbrukere. Du må legge til brukere og tilordne de riktige rollene til dem i Human Resources-miljøet. Hvis du vil ha mer informasjon, se [Opprette nye brukere](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tilordne brukere til sikkerhetsroller](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

