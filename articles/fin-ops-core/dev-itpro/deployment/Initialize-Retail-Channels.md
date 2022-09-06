---
title: Initialiser Commerce Scale Unit (sky)
description: Denne artikkelen beskriver hvordan du initialiserer Commerce Scale Unit (sky) i Microsoft Dynamics 365 Commerce.
author: jashanno
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 25ca054df6422370b1e61dff7965189ad90d7fcc
ms.sourcegitcommit: 7bcaf00a3ae7e7794d55356085e46f65a6109176
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/26/2022
ms.locfileid: "9357665"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Initialiser Commerce Scale Unit (sky)

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du initialiserer Commerce Scale Unit (sky) i Microsoft Dynamics 365 Commerce.

Hvis du bruker et sandkasse eller produksjonsmiljø på nivå 2 som har appversjonen 8.1.2.x eller senere, må du initialisere Commerce Scale Unit (sky) før du kan bruke detaljhandelskanalfunksjonaliteten enten for salgsstedsoperasjoner (POS) eller for e-handelsoperasjoner som bruker Retail Server i skyen. Initialiseringen vil implementere en Commerce Scale Unit (sky).

> [!IMPORTANT]
> For eksisterende kunder som bruker detaljhandelskanalfunksjonalitet i skyen, krever vi at du oppdaterer detaljhandelskanalene til å bruke Commerce Scale Unit for å sikre fortsatt og uavbrutt støtte for forretningen. Nye miljøer som implementeres uten Commerce Scale Unit, vil ikke lenger motta kvalitets- og tjenesteoppdateringer for skyvertsbaserte detaljhandelskanalkomponenter. Det kreves ingen handling for kunder som utelukkende bruker Commerce Scale Unit (egenvertsbasert). Kontakt Microsoft FastTrack Solution Architect hvis du trenger en utvidelse.

## <a name="prerequisites"></a>Forutsetninger

1. Distribuer et sandkasse- eller produksjonsmiljø på nivå 2 som har versjon 8.1.2.x eller senere.
2. Du kan implementere opptil 2 Commerce Scale Units per miljø selv. Hvis du krever mer enn 2 Commerce Scale Unit per miljø, oppretter du en støtteforespørsel i Microsoft Dynamics Lifecycle Services (LCS), og angir **Be om ytterligere Commerce Scale Unit** og angir miljø-ID, antall for Commerce Scale Unit og ønskede datasenterområder. Forespørselen fullføres innen fem virkedager. Hvis du ikke trenger mer enn 2 Commerce Scale Unit per miljø, trenger du ikke å opprette en støtteforespørsel. 
3. Du må ha prosjekteiertillatelser i Lifecycle Services før du kan initialisere Commerce Scale Unit.
4. Kontroller at konfigurasjonsnøkler for detaljhandelslisens er aktivert i miljøet ditt. For mer informasjon, se [Rapport for lisenskoder og konfigurasjonsnøkler](../sysadmin/license-codes-configuration-keys-report.md). Du må ha aktivert følgende nøkler for å bruke Commerce Scale Unit.

    - RetailBasic
    - RetaileCommerce - Hvis du planlegger å bruke e-handel for Dynamics 365 Commerce.
    - RetailGiftCard - Hvis du har tenkt å bruke gavekort.
    - RetailInvent - Hvis du planlegger å bruke lager.
    - RetailModernPos – Hvis du planlegger å bruke salgssted (POS).
    - RetailReplenishment - Hvis du planlegger å bruke etterfyllinger.
    - RetailScheduler
    - RetailStores - Hvis du har tenkt å bruke POS.


## <a name="region-availability"></a>Områdetilgjengelighet
Commerce Scale Unit er tilgjengelig for distribusjon i følgende områder.

| Global plassering | Område              | Tilgjengelighet        | Kommentarer                  |
|-----------------|---------------------|---------------------|---------------------------|
| NORD- OG SØR-AMERIKA        | USA øst             | Generelt tilgjengelig |  Ingen kommentarer.                         |
| NORD- OG SØR-AMERIKA        | USA øst 2           | Generelt tilgjengelig |  Ingen kommentarer.                          |
| NORD- OG SØR-AMERIKA        | USA sentralt i nord    | Begrenset kapasitet    |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | USA sentralt i sør    | Begrenset kapasitet    |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | USA sentralt          | Generelt tilgjengelig |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | USA vest             | Generelt tilgjengelig |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | USA vest 2           | Generelt tilgjengelig |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | Canada, sentralt      | Begrenset kapasitet    |  Ingen kommentarer.                            |
| NORD- OG SØR-AMERIKA        | Canada, øst         | Begrenset kapasitet    |   Ingen kommentarer.                           |
| NORD- OG SØR-AMERIKA        | USA, vest-sentralt     | Begrenset kapasitet    |   Ingen kommentarer.                           |
| APAC            | Australia øst      | Generelt tilgjengelig |   Ingen kommentarer.                           |
| APAC            | Asia sørøst      | Kapasitetsbegrenset | Ingen distribusjoner tillatt.    |
| APAC            | Japan øst          | Generelt tilgjengelig |  Ingen kommentarer.                            |
| APAC            | Japan vest          | Generelt tilgjengelig |   Ingen kommentarer.                           |
| APAC            | Australia sørøst | Generelt tilgjengelig |   Ingen kommentarer.                           |
| APAC            | Asia øst           | Begrenset kapasitet    |   Ingen kommentarer.                           |
| APAC            | India, Sør         | Kapasitetsbegrenset | Ingen distribusjoner tillatt.    |
| APAC            | Det sentrale India       | Begrenset kapasitet    | Krever godkjenningsprosess. |
| EMEA            | Europa vest         | Generelt tilgjengelig    |  Ingen kommentarer. |
| EMEA            | Europa nord        | Generelt tilgjengelig    |  Ingen kommentarer. |
| EMEA            | Storbritannia, sør            | Generelt tilgjengelig |    Ingen kommentarer.                          |
| EMEA            | Storbritannia, vest             | Generelt tilgjengelig |    Ingen kommentarer.                          |
| Sveits     | Sveits, nord   | Begrenset kapasitet    | Krever godkjenningsprosess. |
| De forente arabiske emirater             | De forente arabiske emirater, nord           | Begrenset kapasitet    | Krever godkjenningsprosess. |

Distribusjonskapasitet i områder med begrenset kapasitet er ekstremt begrenset. Forespørsler om distribusjon evalueres hver for seg. Hvis du har et tvingende forretningsbehov for distribusjon i områder med begrenset kapasitet, kan du sende en støtteforespørsel som skal legges til i ventelisten. Kapasitetsbegrensede områder tillater i øyeblikket ikke Commerce Scale Unit-distribusjon. 

![Kart som viser områdetilgjengelighet.](media/Commerce-Scale-Unit-Region-Availability.png "Kart som viser områdetilgjengelighet")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Initialiser Commerce Scale Unit som en del av en ny miljødistribusjon

Kontroller at hovedkontoret er tilgjengelig. Dette er nødvendig for å registrere storskalaenheten i hovedkontoret i løpet av initialiseringsprosessen. Det anbefales ikke å initialisere en storskalaenhet når hovedkontoret er under service, fordi det kan bli utilgjengelig under prosessen.

1. Kontroller at hovedkontormiljøet er tilgjengelig, og ikke i [vedlikeholdsmodus](../sysadmin/maintenance-mode.md).
2. I LCS, på siden med miljødetaljer, velger du **Miljøfunksjoner \> Commerce**.
3. På siden for oppsett av Commerce-distribusjon velger du **Initialiser**.
4. Velg versjonen av Commerce Scale Unit som skal initialiseres.
5. Velg et område som Commerce Scale Unit skal initialiseres i.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Konfigurere kanaler for å bruke Commerce Scale Unit

Når Commerce Scale Unit er distribuert, må du kontrollere at kanalene er konfigurert til å bruke databasen for det. 

Følg denne fremgangsmåten for å konfigurere kanalene for å bruke Commerce Scale Unit-databasen.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Handelsplanlegger \> Kanaldatabase** i Commerce Headquarters.
1. I den venstre ruten velger du en kanaldatabase.
1. På hurtigfanen **Detaljhandelskanal** velger du **Legg til**, og deretter velger du detaljhandelskanalen fra rullegardinlisten.
1. Velg **Legg til**, og velg deretter nettkanalen i rullegardinlisten. 

Når du er ferdig, går du til **Retail og Commerce \> IT for Retail og Commerce \> Distribusjonsplan** og kjører jobb 9999.

> [!NOTE] 
> Jobb 9999 synkroniserer alle nye produkter og kunder til Commerce Scale Unit. Denne prosessen kan ta lang tid. Hvis kanalen må være tilgjengelig kun for konfigurasjon av områdebygger for e-handel, kan du kjøre jobb 1070 i stedet for jobb 9999.

### <a name="database-refresh-and-commerce-scale-units"></a>Databaseoppdatering og Commerce Scale Units

Før du begynner, må du være kjent med [trinnene som må fullføres etter en databaseoppdatering for miljøer som bruker Commerce-funksjonalitet](../database/database-refresh.md).

Kanaldatabasepostene for storskalaenheten (i skjemaet Kanaldatabase) kan ikke flyttes på tvers av miljøer som en del av databaseoppdateringen. Dette skyldes at postene representerer miljøspesifikk konfigurasjon.

Etter databaseoppdateringen kan du generere storskalaenhetens kanaldatabasepost på nytt ved å utstede en ny distribusjon av storskalaenheten i LCS. Alle distribusjoner eller vedlikeholdsoperasjoner i storskalaenheten vil forsøke å registrere storskalaenheten i hovedkontoret hvis registreringen oppdages som manglende.

Du kan utstede en omdistribuering av storskalaenheten uten å endre noen komponenter ved å velge å distribuere den samme versjonen av storskalaenheten som den allerede har. Dette kan gjøres i LCS via følgende trinn:

1. I LCS, på siden med miljødetaljer, velger du **Miljøfunksjoner \> Retail**.
2. På siden for oppsett av distribusjonen velger du storskalaenheten du vil distribuere på nytt.
3. Velg **Oppdater** på storskalaenhetens operasjonsmeny .
4. På glidebryteren i rullegardinlisten for **Velg versjon** velger du alternativet **Angi en versjon**.
5. I tekstboksen under **Angi en versjon** skriver du inn versjonen som vises for storskalaenheten, som vises ved siden av etiketten **Gjeldende versjon**.
6. Klikk på **Oppdater**-knappen.

Du trenger ikke å velge **Oppdater tillegg**, selv om du har brukt utvidelser tidligere, siden siste utvidelsespakke som brukes på storskalaenheten, plukkes automatisk ved oppdatering av en storskalaenhet.

Hvis du har flere storskalaenheter, må du utføre operasjonen over for hver storskalaenhet. Du kan utføre disse operasjonene parallelt hvis du vil det.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Distribuere flere Commerce Scale Units (valgfritt)

Når du har initialisert Commerce Scale Unit, kan du selv distribuere en ny storskalaenhet hvis lisensen gir deg rett til å gjøre det. Hvis du vil distribuere mer enn to storskalaenheter, må du opprette en støtteforespørsel. I støtteforespørselen oppgir du antallet Commerce Scale Units du trenger, miljønavnet og de ønskede områdene. Hvis du vil ha mer informasjon om lisensiering, kan du se [lisensieringsveiledningen for Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

For hver nye Commerce Scale Unit du distribuerer, anbefaler vi at du oppretter en egen kanaldatabasegruppe ved å følge disse trinnene.

1. I Commerce-hovedkontoret går du til **Detaljhandel og handel > Retail Headquarters > Oppsett av Detaljhandel Planlegger > Kanaldatabasegruppe**.
2. Opprett ny gruppe for kanaldatabase.
3. Gå til **Detaljhandel og handel > Retail Headquarters > Oppsettet av Detaljhandel Planlegger > Kanaldatabase**, og velg kanaldatabasen som tilsvarer den nyopprettede Commerce Scale Unit.
4. Velg **Rediger**, og velg den nye kanaldatabasegruppen.
5. Velg **Lagre**.
6. Velg **Kjør fullstendig datasynkronisering** for den valgte kanaldatabasen.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Flere hensyn hvis du initialiserer skyvertsbaserte handelskanalkomponenter i et eksisterende miljø

Hvis du allerede bruker skybaserte handelskanalkomponenter i et miljø, vil initialisering av Commerce Scale Unit bidra til å redusere nedetiden når disse komponentene oppdateres. Tilleggsplanlegging er nødvendig før initialiseringen av Commerce Scale Unit.

Når du initialiserer din første Commerce Scale Unit i et miljø som bruker skybaserte handelskanalkomponenter, migrerer initialiseringsprosessen kanalene som er knyttet de skyvertsbaserte kanalkomponentene til den første storskalaenheten. Kanaler som er tilknyttet storskalaenheter for butikk, er upåvirkede.

Migreringsprosessen er synlig for kanalene. Når initialiseringen av storskalaenheten har startet, utføres følgende operasjoner automatisk:

1. En ny Commerce Scale Unit opprettes og knyttes til miljøet.
2. Commerce Scale Unit blir registrert som en tilgjengelig kanaldatabase i hovedkontoret.
3. Alle kanaler som er tilordnet **standard** kanaldatabase i hovedkontoret, blir oppdatert for å tilordne til den nye Commerce Scale Unit.
4. En fullstendig datasynkronisering i Commerce Data Exchange (CDX) blir utført for å bringe kanaldataene til den nye storskalaenheten.

**Planlegge og teste for initialisering av Commerce Scale Unit** Når du initialiserer Commerce Scale Unit, må du som en genrell regel planlegge for et vindu med fem timers nedetid for butikkoperasjoner, i tillegg til eventuelle operasjoner i e-handelskanalen som bruker Retail Server eller Cloud Point of Sale.

1. Utfør en databaseoppdatering fra produksjonsmiljøet til et UAT-sandkassemiljø. 
2. Initialiser Commerce Scale Unit i UAT-sandkassemiljøet. 
3. Legg merke til initialiseringstiden for Commerce Scale Unit. Dette vil være sammenlignbart med tiden denne operasjonen tar i produksjonsmiljøet, der butikkoperasjoner og e-handelsoperasjoner ikke er tilgjengelige.

Du må utføre følgende tilleggstrinn før du initialiserer Commerce Scale Unit.

- **Lukk alle POS-skift** – Etter migrering vil POS-brukere ikke kunne lukke skift som var aktive under migreringsprosessen.
- **Valider at alle P-jobber er fullført** – Det anbefales at P-jobber for å synkronisere ventende transaksjoner er fullført før CSU initialiseres.
- **Logg av alle POS-enheter** – POS-operasjoner støttes ikke under migrering.
- **Tilbakekall og annuller alle suspenderte transaksjoner i POS** – Suspenderte transaksjoner beholdes ikke som en del av initialiseringen.

> [!IMPORTANT]
> Som en del av initialiseringen av Commerce Scale Unit vil tidligere suspenderte transaksjoner gå tapt, og de kan ikke tilbakekalles. 

Følgende skjer i løpet av initialiseringsperioden:

- Handelskanaler driftet i skyen vil ikke fungere, med mindre du slår på offline-funksjonalitet for POS.
- POS-enheter med offline-funksjonalitet aktivert vil ha redusert funksjonalitet.
- Alle e-handelsklienter som avhenger av Retail Server, blir avbrutt.
- Kanaler som driftes på Commerce Scale Units (egendriftet), berøres ikke.
- Hovedkontorfunksjonaliteten påvirkes ikke.

Følgende skjer når initialiseringen er fullført:

- Aktiveringsstatusen for alle aktiverte POS-enheter beholdes, noe som betyr at enhetene ikke må aktiveres på nytt.
- Frittstående forekomster av maskinvarestasjoner vil fortsette å fungere.
- Rapporter på POS-kanalsiden blir tilbakestilt og vil ikke vise data fra før initialiseringen.
- Vis journal-operasjonen blir også tilbakestilt og vil ikke vise data fra før initialiseringen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
