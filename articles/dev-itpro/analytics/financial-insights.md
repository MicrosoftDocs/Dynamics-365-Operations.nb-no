---
title: "Økonomisk innsikt"
description: "Økonomisk innsikt bruker Microsoft Power BI til å sette sammen økonomiske nøkkelindikatorer (KPI-er), diagrammer og regnskapsoppgjør."
author: kweekley
manager: AnnBe
ms.date: 02/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6679215a664ddf938a204196b00f3bc28bf65f8f
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="financial-insights"></a>Økonomisk innsikt

[!include [banner](../includes/banner.md)]

**Økonomisk innsikt** bruker Microsoft Power BI til å sette sammen økonomiske nøkkelindikatorer (KPI-er), diagrammer og regnskapsoppgjør. Power BI is er innebygd i Microsoft Dynamics 365 for Finance and Operations.
Fokuset til **Økonomiske innsikt** er analytisk rapportering. Personer i en organisasjon kan vise, undersøke, forstå og utføre en handling. 

**Økonomisk innsikt** kombinerer data fra økonomimodulen og underfinans for å gi en mer fullstendig oversikt over den økonomiske situasjonen i en organisasjon.

> [!NOTE] 
> Dette dokumentet bruker følgende Power BI-terminologi:                                                                           
**Rapport** – En enkelt .pbix-fil som alle visuelle effekter i alle kategoriene lagres i.                                                          
**Side** – En kategori i en enkelt .pbix-fil. Hver side kan inneholde én eller flere visuelle effekter.                                                     
**Visuelt** – Én enkelt kilde med data, for eksempel kort, KPI, diagram, graf, matrise og regnskapsoppgjør. En side som har et regnskapsoppgjør som en visuell effekt, kan ikke ha flere andre visuelle effekter på grunn av størrelsen på dataene som rapporteres.


For øyeblikket brukes **økonomisk innsikt** til å vise data for den aktive juridiske enheten eller alle juridiske enheter. I fremtidige versjoner utvikles arbeidsområdet til et sted der du kan bruke Power BI til å redigere og opprette visuelle effekter.

**CFO-oversikt**-arbeidsområdet viser samme visuelle effekter som **økonomisk innsikt**, men fokuserer på at du kan vise og filtrere dataene i eksisterende rapporter. I fremtidige versjoner vil du kunne legge til nye visuelle effekter i **Økonomisk innsikt**-arbeidsområdet. De nye visuelle effektene kan også være tilgjengelige i arbeidsområder som fokuserer på andre roller, for eksempel prosjektledere eller regnskapssjefer for leverandørreskontro. **CFO-oversikt**-arbeidsområdet fortsetter å vise data for alle juridiske enheter, uavhengig av de juridiske enhetene som rollen har tilgang til.

## <a name="finance-and-operations-setup"></a>Oppsett av Finance and Operations
**Økonomimodul**

Hovedkontotypen og hovedkontokategoriene brukes til å fylle ut riktige standardhovedkontoer i **Balanse**-regnskapsoppgjøret og de ulike **Resultatregnskap**-regnskapsoppgjørene i **Økonomisk innsikt**.

På **Hovedkontoer**-siden må du definere hovedkontoen din slik at én av følgende typer tilordnes til den:

•   Omsetning

•   Utgift

•   Aktiva

•   Gjeld

•   Egenkapital

Ikke tilordne noen annen hovedkontotype, for eksempel **Balanse** eller **Resultat**, til hovedkontoene. Rapportering kan ikke bestemme typen hovedkonto når andre hovedkontotyper er tilordnet fordi de ikke er detaljert nok. Type hovedkonto må bestemmes for å vise gjeld og omsetning som positive beløp i finansrapporter.

For å vises i regnskapsoppgjørene og inkluderes i forskjellige andre visuelle effekter, for eksempel KPI-er, må hver hovedkonto tilordnes en hovedkontokategori. Hovedkontokategoriene er forbedret slik at de inkluderer en visningsrekkefølge. Visningsrekkefølgen brukes spesielt i regnskapsoppgjør i **Økonomisk innsikt**. Når du har redigert eller lagt til en ny hovedkontokategori, kan du endre **Visningsrekkefølge**-verdien for å definere rekkefølgen som hovedkontokategoriene skal vises i, i et regnskapsoppgjør. Hvis du må endre visningsrekkefølgen for mange hovedkontokategorier, kan du bruke Åpne i Excel-funksjonen til å raskt redigere og publisere endringene tilbake til Finance and Operations.


## <a name="entity-store"></a>Enhetslager
Dataene for **Økonomisk innsikt** hentes fra enhetslageret (**Systemadministrasjon** > **Oppsett** > **Enhetslager**). Hvis du åpner **CFO-oversikt**- eller **Økonomisk innsikt**-arbeidsområdet, og følgende advarsel vises i de visuelle effektene, må du oppdatere enhetene.
 
![Advarsel!](./media/Cantdisplay.png)

Du må oppdatere følgende enheter for å vise data i **Økonomisk innsikt**- og **CFO-oversikt**-arbeidsområder:

•   CustCollectionsBIMeasurements

•   FinancialReportingOtherData

•   FinancialReportingReferenceData

•   FinancialReportingTransactionData

•   LedgerCovLiquidityMeasurement

•   Innkjøpskube

•   Salgskube

I den forrige versjonen ble enhetene LedgerActivityMeasure og VendPaymentBIMeasure brukt for data i **CFO-oversikt**-arbeidsområdet. De brukes imidlertid ikke lenger i denne versjonen.

Du kan definere en gjentakende satsvis jobb for å oppdatere dataene i enhetene regelmessig. Fordi hver enhet fullstendig gjenoppbygges under en oppdatering, må du velge nøye tid og frekvens for enhetsoppdateringene. Hovedenheten som skal brukes for regnskapsoppgjør, er FinancialReportingTransactionData-enheten. Derfor kan det hende at du vil oppdatere denne enheten oftere.

## <a name="security"></a>Sikkerhet
For øyeblikket kan ikke dataene i innebygde Power BI-rapporter være begrenset til de juridiske enhetene som brukeren har tilgang til. Derfor kontrolleres innebygde Power BI-rapporter via plikter i sikkerhetsoppsettet. Pliktene som defineres, gir tilgang til data for alle juridiske enheter eller bare det aktive selskapet. Følgende tabell viser pliktene som finnes og rollene de er tilordnet til. Pliktene kan fjernes eller tilordnes til forskjellige roller, basert på organisasjonens behov.

| **Avgift**                     | **Roller**                                       | Beskrivelse                     |
|------------------------------|-------------------------------------------------|-----------------|
| Vis arbeidsområde for CFO-oversikt  | Økonomidirektør                         | •    Denne plikten gir tilgang til arbeidsområdet for CFO-oversikt. •  Som standard brukes det aktive selskapet som et filter. Du kan imidlertid legge til alle juridiske enheter, uansett om brukeren har tilgang til andre juridiske enheter.               |
| Vis økonomisk innsikt for gjeldende firma | •   Regnskapsfører •    Regnskapssjef •    Regnskapsansvarlig • Revisor •   Budsjettbehandling •    Administrerende direktør •   Økonomidirektør •   Økonomikontrollør  |   • Denne plikten gir tilgang til Økonomisk innsikt. •  Som standard brukes det aktive selskapet som et filter. Du kan ikke legge til andre juridiske enheter.            |
| Vis økonomisk innsikt på tvers av firma   | •   I Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, er ikke denne plikten tilordnet en rolle. • I neste versjon vil denne plikten tilordnes til Økonomidirektør-rollen. | •    Denne plikten gir tilgang til menyelementet for arbeidsområdet CFO-oversikt. •    Som standard brukes det aktive selskapet som et filter. Du kan imidlertid legge til alle juridiske enheter, uansett om brukeren har tilgang til andre juridiske enheter.             |


## <a name="financial-reporting-vs-finanical-insights"></a>Finansrapportering kontra økonomisk innsikt
Selv om **Økonomisk innsikt** inneholder regnskapsoppgjør, er det ikke en erstatning for Finansrapportering i Finance and Operations. Standard regnskapsoppgjør i **Økonomisk innsikt** er begrenset i omfang og omfatter ikke alle typer regnskapsoppgjør. Finansrapportering er fremdeles primærverktøyet som brukes til å utforme, opprette og generere lovbestemte regnskapsoppgjør.

Sammenligningsdiagrammet nedenfor vil hjelpe deg med å skille mellom de to alternativene:


|                                                                       |               <strong>Finansrapportering</strong>                |                                      <strong>Økonomisk innsikt</strong>                                      |
|-----------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
|                 <strong>Rediger standardrapporter</strong>                 |                                Ja                                |                                                      Antall                                                       |
|                  <strong>Opprett nye rapporter</strong>                  |                                Ja                                |                                                      Antall                                                       |
|                    <strong>Skriv ut rapporter</strong>                     |                                Ja                                |                                                      Antall                                                       |
|                   <strong>Eksporter til Excel</strong>                    |                                Ja                                |                           Begrenset Eksporterer rådata til Excel, ikke en formatert rapport                           |
|  <strong>Støtt rapporteringshierarki/organisasjonshierarki</strong>  |                                Ja                                |                                                      Antall                                                       |
|               <strong>Rapporter om underfinansdata</strong>               |               Ja Begrenset til bare leverandør, kunde                |                 Ja Leverandør, kunde, leverandør-/kundegrupper, leverandør-/kundeadresser og så videre.                 |
|                  <strong>Rapporteringsvaluta</strong>                  |    Ja Regnskapsvaluta og omveksle til rapporteringsvaluta    |                                          Nei Bare regnskapsvaluta                                          |
|                       <strong>Sikkerhet</strong>                       | Ja Samsvarer med Finance and Operations- og rapporteringstresikkerhet | Begrenset Vis rapporter for alle firmaer (uansett Finance and Operations-sikkerhet) eller bare aktivt selskap |
| <strong>Støtt ulike kontoplaner og regnskapsår</strong> |                                Ja                                |                                                      Antall                                                       |
|               <strong>rapporter om eksterne data</strong>                |                                Antall                                 |                                                      Antall                                                       |
|                <strong>Støtt konsolideringer</strong>                |                                Ja                                |                   Begrenset Kan rapportere om flere firmaer, men bare bruke regnskapsvaluta                   |

I tillegg til brukergrensesnittet i det opprinnelige **CFO-oversikt**-arbeidsområdet, finnes det nå nye KPI-er, diagrammer og regnskapsoppgjør. Følgende regnskapsoppgjør er tilgjengelige:

•   Råbalanse

•   Balanse

•   Resultatregnskap etter område

•   Resultatregnskap – faktisk i forhold til budsjett

•   Resultatregnskap med avvik

•   12-måneders trend resultatregnskap

•   Utgifter treårs trend

•   Utgifter etter leverandør

•   Salg etter kunde

## <a name="edit-visuals"></a>Rediger visuelle effekter
I den første versjonen av **Økonomisk innsikt** kan ingen av de visuelle effektene redigeres. I fremtidige versjoner kan brukere som har riktig sikkerhet, opprette nye visuelle effekter, kopiere eksisterende effekter og redigere dem. Selv om .pbix-filene som inneholder rapportene, er tilgjengelige som ressurser, anbefaler vi ikke at du redigerer standardrapportene. Flere endringer vil bli gjort i visuelle effekter for datamodellen, standardrapporter og tilpasset regnskapsoppgjør som brukes til å opprette regnskapsoppgjørene. Derfor, hvis du vil dra nytte av nye funksjoner og endringer i datamodellen i neste versjon, må du gjøre om eventuelle endringer du foretok i standardrapportene via Microsoft Power BI Desktop.


## <a name="filtering"></a>Filtrering
Brukere kan filtrere rapporten ved hjelp av **Filter**-ruten til venstre. Dette er den samme ruten som er tilgjengelig via Power BI-skrivebordet.
Det finnes forskjellige nivåer med filtrering, noen er kanskje ikke tilgjengelige, avhengig av hva du har valgt på en side (kategori), eller om du bruker funksjonene for gjennomgang:

•   **Rapportnivåfiltrere** – Disse filtrene brukes på alle visuelle effekter på alle sider (kategorier).

•   **Sidenivåfiltre** – Disse filtrene brukes på alle visuelle effekter i den aktive kategorien. Disse filtrene brukes over rapportnivåfiltrene.

•   **Visuellnivåfiltre** – Disse filtrene brukes bare på den valgte visuelle effekten. Disse filtrene brukes på toppen av sidenivåfiltrene.

•   **Gjennomgangsfilter** – Dette filteret filtrerer fra en visuell kildeeffekt som brukes på den gjeldende visuelle effekten når du gjennomgår fra den visuelle kildeeffekten til den gjeldende visuelle effekten.

![Filter](./media/filter.png)


Hvis du vil fjerne en bestem filterverdi, velger du slettesymbolet ved siden av den. Ikke fjern et filter ved å velge X. Hvis du velger X, fjernes feltet du filtrerer på, som filteralternativ. Hvis du ved et uhell fjerner et felt fra filteret, lukk arbeidsområdet og åpne det deretter på nytt. Standardfilterinnstillingene blir brukt på nytt.

Når du først åpner arbeidsområder, brukes den aktive juridiske enheten som standard som rapportnivåfilter. Avhengig av sikkerheten, kan det hende at brukere kan legge til andre juridiske enheter eller endre standard juridisk enhet som er valgt i filteret.

**Regnskapskalender**-filteret er nødvendig, slik at riktig kalender brukes for visuelle effekter. Som standard settes rapportnivåfilteret til regnskapskalenderen for den aktive juridiske enheten. Hvis du endrer filteret til en økonomisk kalender som har en annen startdato eller sluttdato, blir ikke startsaldoene inkludert. Derfor viser ikke **Balanse**-regnskapsoppgjøret riktig saldo. Hvis du velger en ekstra økonomisk kalender i filteret, får du et ekstra sett med kolonner. Hvert ekstra sett med kolonner viser beløpene for en annen regnskapskalender.

**Posteringslag**-filteret er også nødvendig. Som standard settes filteret til Gjeldende. Du kan velge flere posteringslag i filteret for å vise de akkumulerte beløpene.

Filtre er også tilgjengelige for **Dato**- og **Regnskapsår**-feltene. Disse filtrene brukes vanligvis på sidenivå. Som standard bruker **Dato**-filteret en tilhørende dato som du kan endre. Du kan også fjerne det tilhørende datofilteret og bruke **Regnskapsår**-filteret i stedet.

## <a name="currency"></a>Valuta

Alle visuelle effekter som rapportere finansdata, viser beløp i regnskapsvalutaen. Når du filtrerer på den juridiske enheten, må du derfor være forsiktig å ta med bare juridiske enheter som har samme regnskapsvaluta. Hvis ikke, vil du aggregere data i ulike valutaer.

Alle visuelle effekter som rapporterer underfinansdata, som de visuelle effekten **Kontantstrømprognose** og **Topp 10**, viser beløpene i systemvalutaen. Systemvaluta og systemvalutakurstype defineres på **Systemparametere**-siden.

Den visuelle effekten **Saldo etter bankkonto** bruker beløp i valutaen til bankkontoene.

## <a name="dimensions"></a>Dimensjoner

Standard regnskapsoppgjør ta ikke med alle finansdimensjoner, men fokuserer bare på hovedkontoen. Støtte for finansdimensjoner vil være tilgjengelig i fremtidige versjoner, når rapportene blir redigerbare. Organisasjoner kan da filtrere på finansdimensjonsverdiene.

Noen regnskapsoppgjør inneholder dimensjonene som er basert på underfinanstransaksjoner. Målet med de nye regnskapsoppgjørene er å aktivere filtrering på dimensjoner som ikke er angitt som finansdimensjoner. For eksempel standardrapporten Utgifter per leverandør lar deg utvide ned utover hovedkontoen, slik at du kan se saldoene inndelt etter leverandør. Leverandøren er ikke konfigurert som en finansdimensjon. I stedet returnerer systemet til den opprinnelige underfinanstransaksjonen for å finne leverandøren.

Følgende dimensjoner brukes på standardrapportene. Ingen av disse dimensjonene er finansdimensjoner.

•   Leverandør

•   Leverandørgruppe

•   Kunde

•   Kundegruppe

•   Land/område

•   Delstat/område

•   Poststed

> [!IMPORTANT] 
> Hvis du vil summere transaksjoner for flere leverandører eller kunder i et enkelt bilag ved å bruke finansjournaler, vil dataene bli feil. Rapportering kan ikke bestemme hvilken leverandør eller kunde som er knyttet til en bestemt finanskonto i en journaloppføring fordi denne informasjonen ikke vedlikeholdes hvor som helst. Derfor anbefaler vi ikke at du angir flere leverandører, kunder, aktiva eller prosjekter i et enkelt bilag.

## <a name="drill-on-data"></a>Vise detaljer for dataene

Ulike nivåer av drilling er tilgjengelig via Power BI. Hvert nivå har ulikt navn og ulik funksjonalitet. Du kan også drille i rader og kolonner. Denne delen beskriver de ulike alternativene ved å bruke **Råbalanse**-regnskapsoppgjøret som et eksempel og viser hvordan du kan se detaljer i radene. Det finnes samme funksjonalitet for kolonnene. Du trenger bare å endre **Drill på**-innstillingen.

I illustrasjonen nedenfor er **Råbalanse**-utdraget trukket sammen til det høyeste nivået i radhierarkiet, hovedkontotypen.

![Råbalanse](./media/trial-balance.png)

 
Hvis du vil vise det neste nivået i hierarkiet, hovedkontokategoriene, kan du sette **Drill på**-feltet til **Rader** og velge **Vis** (den tredje knappen etter Drill på-feltet). Du kan nå se alle hovedkontokategoriene. For øyeblikket lar ikke Power BI deg vise bare én rad eller kolonne, men samtidig kunne se alle de andre radene eller kolonnene.
 
![Råbalanse](./media/trial-balance2.png)
 
  
Hvis du vil utvide hovedkontoene for alle radene, kan du igjen bruke **Vis**-knappen. Men for å drille ned til hovedkontoene for bare én rad, må du første velge **Drill ned**-knappen (den enkle pilen som peker nedover, til høyre i vinduet), og deretter velge raden for neddrilling. Illustrasjonen nedenfor viser resultatet når **Salg**-raden velges etter **Drill ned**-knappen er valgt.

![Råbalanse](./media/trial-balance3.png)

Når du har drillet ned på en enkelt rad, kreves det flere klikk for å gå tilbake til den fullstendige råbalansen. **Drill opp**-knappen (den første knappen etter **Drill på**-feltet) driller bare opp i forbindelse med **Salg**-kategorien, som vist i illustrasjonen nedenfor.
 
![Råbalanse](./media/trial-balance4.png)
 
 
Du kan fortsette å bruke **Drill opp**-knappen for å gå tilbake til det høyeste nivået i summeringen for radene.

Power BI har også en knapp som gjør det mulig å gå til neste nivå i hierarkiet (den andre knappen etter **Drill på**-feltet). Effekten av denne knappen er forskjellig fra effekten av **Vis**-knappen (den tredje knappen etter **Drill på**-feltet), som brukes til å utvide hierarkiet. Når du utvider hierarkiet, beholdes hierarkiet i rapporten. Hvis du for eksempel som vist tidligere utvider på hovedkontotypen, ser du fortsatt hovedkontotypen i rapporten. Men når du går til neste nivå i hierarkiet, viser ikke lenger rapporten overordnet i hierarkiet, som vist i illustrasjonen nedenfor.

![Råbalanse](./media/trial-balance5.png)

 
Hvis du vil vise transaksjonsinformasjonen bak de summerte saldoene, kan du velge noen beløp for å drille tilbake til Financial and Operations.

Tilbakedrillingen fra regnskapsoppgjørene fører deg til regnskapskildeutforskeren, ikke bilagstransaksjonene. Regnskapskildeutforskeren viser ikke bare regnskapsoppføringer i økonomimodulen. I stedet viser den detaljene for underfinanstransaksjonen. Du får derfor mye mer detaljert informasjon om den opprinnelige transaksjonen og kan bruke den for analyse. Du kan for eksempel se hvem kunden eller leverandøren var, hva kunden kjøpte eller leverandøren solgte, og også hvilket prosjekt som ble brukt i transaksjonen.

Følgende filtre fra regnskapsoppgjøret sendes til regnskapskildeutforskeren, slik at den viser transaksjonene som er aggregert:

Obligatoriske felt for filtrering:

  - Juridisk enhet
 
  - Økonomisk kalender
 
  - År
 
  - ID for hovedkonto

Valgfrie felt for filtrering:

  - Kvartal

  - Måned

  - Periode

Hvis du ikke utvider langt nok nedover på en rad, vil ikke neddrillingen fungere. For eksempel hvis du utvider ned bare til hovedkontokategorien, kan du ikke drille ned til regnskapskildeutforskeren i balansen fordi hovedkontoen er et obligatorisk felt for filtrering i utforskeren.

Hvis du utvider ned for langt på en rad, sendes ikke de ekstra filtrene på regnskapsoppgjøret til regnskapskildeutforskeren. Derfor kan du se en forskjell i tallene. For eksempel, hvis du utvider ned til landet eller området på radene i resultatregnskapet etter områderegnskapsoppgjør, er ikke landet eller området inkludert som et filter i regnskapskildeutforskeren.

> [!NOTE]
> Du kan drille videre ned i regnskapsoppgjørsradene eller -kolonnene enn regnskapskildeutforskeren for øyeblikket støtter for filtrering. Derfor vil i noen tilfeller summen av detaljerte transaksjoner i regnskapskildeutforskeren ikke samsvare med saldoen som du driller tilbake på. Denne funksjonen vil forbedres videre i fremtiden.

## <a name="hierarchies"></a>Hierarkier

Standardregnskapsoppgjørene bruker to hierarkier til å drille og utvide på dataene. Ett hierarki er for radene, og det andre hierarkiet er for kolonnene. Begge hierarkier er forhåndsdefinert i utformingen av regnskapsoppgjøret. For de fleste regnskapsoppgjør er radhierarkiet **Hovedkontotype** > **Hovedkontokategorier** > **Hovedkonto**. Noen av rapportene har imidlertid flere felt, for eksempel land og område. De ekstra nodene i hierarkiet er basert på underfinansdata for hver transaksjon.

For kolonnene fokuserer hierarkiet på de juridiske enhetene og regnskapsperiodene. For de fleste regnskapsoppgjør er klonnehierarkiet **Juridisk enhet** > **Regnskapskalender** > **Regnskapsår** > **Kvartal** > **Periode**.

For øyeblikket støtter ikke regnskapsoppgjør organisasjonshierarkiene, som lar deg aggregere data.

## <a name="data-limitations"></a>Databegrensninger
Visuelle effekter for regnskapsoppgjøret har en grense for hvor mange rader som kan vises. Grensen er for øyeblikket satt til 30 000. Hvis du overskrider denne grensen, har den visuelle effekten et varselsymbol som varsler deg om dette.
 
![Databegrensninger](./media/data-limit.png)


Hvis maksimalt overskrides, blir totalsummene som vises i regnskapsoppgjøret feil fordi ikke alle radene ble lastet inn i den visuelle effekten.

### <a name="empty-rows"></a>Tomme rader
Power BI har ikke et alternativ for å vise og skjule tomme rader. Hvis en rad ikke inneholder data, vises ikke raden i bildet.

## <a name="what-is-coming-in-future-releases"></a>Hva kommer i fremtidige versjoner?
De nye arbeidsområdene og regnskapsoppgjørene som bruker Power BI, vil fortsatt bli forbedret. Her er noen av de nye funksjonene som vurderes for fremtidige versjoner:

 - Muligheten til å kopiere, redigere, slette og opprette visuelle effekter, selv regnskapsoppgjørene                                                  
 - Flere standardrapporter                                                                                                            
    - Støtte for flere underfinansdata                                                                                            
 - Støtte for en rapporteringsvaluta                                                                                                      
 - Legge til egendefinerte beregninger for rader og kolonner                                                                                          
 - Muligheten til å eksportere regnskapsoppgjør til Microsoft Excel                                                                     
   - Bevare formatet til regnskapsoppgjøret under eksport.                                                                          
   - Analysere data i Excel ved å opprette en pivottabell som bruker informasjonen i den visuelle effekten.                                              
 - Lokal støtte                                                                                                                        
 - Muligheten til å definere rapporteringshierarkier, slik at du kan definere hovedkontohierarkier eller et organisasjonshierarki som kan brukes i regnskapsoppgjør for utforming, filtrering og sikkerhet.                                                                    
 - Støtte for utskrift

De nye funksjonene vil kommuniseres via veikartwebområdet når arbeidet startes: https://roadmap.dynamics.com/.

## <a name="additional-resources-for-power-bi"></a>Tilleggsressurser for Power BI

Informasjonen i følgende ressurser er ikke nødvendig for å aktivere de innebygde rapportene for **CFO-oversikt**- eller **Økonomisk innsikt**-arbeidsområdet i et produksjonsmiljø. I stedet er de nyttige for utviklerbokser og hvis du vil bygge inn dine egne Power BI-rapporter i Finance and Operations.

https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/

https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces

