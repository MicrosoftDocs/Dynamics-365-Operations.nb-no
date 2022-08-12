---
title: Bestillingspostering
description: Denne artikkelen beskriver Bestilling-fanen på siden Lagerposteringsprofiler.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151040"
---
# <a name="purchase-order-posting"></a>Bestillingspostering

**Bestilling**-fanen på siden **Lagerposteringsprofiler** brukes til å styre hvordan bestillinger skal posteres i økonomimodulen. To hovedaktiviteter posteres til økonomimodulen for en bestilling: 

- Produktkvittering
- Faktura

For at en fysisk transaksjon (mottaksseddel) skal kunne posteres i økonomimodulen på en bestilling, må følgende bokser avmerkes:

- **Poster mottaksseddel i finans** på siden **Parametere for beholdnings- og lagerstyring**.
- **Poster aktuell beholdning** og **Gjeldsavsetning på mottaksseddel** på siden **Varemodellgrupper**.

Hovedkontoene må være angitt på siden **Lagerposteringsprofil** for følgende posteringstyper:

- Kostnad for innkjøpte materialer mottatt
- Innkjøpsutgift, ikke-fakturert
- Innkjøp, avsetning

For at en finanstransaksjon (faktura) skal kunne posteres i økonomimodulen for en bestilling, må følgende betingelser oppfylles:

- Det må være merket av for **Poster økonomisk lager på siden** på siden **Varemodellgrupper** for varen som er valgt på bestillingslinjen.
- Hovedkontoene må være angitt på siden **Lagerposteringsprofil** for følgende posteringstyper:
  - Kostnad for innkjøpte materialer fakturert
  - Innkjøpsutgift for produktet
  - Innkjøpsutgift for utgiften
  - Rabatt (valgfritt)

## <a name="fixed-receipt-price-posting"></a>Postering for fast mottakspris

Du kan bruke fast mottakspris som standardkostnad for et produkt som et alternativ til å velge alternativet **Standardkost** i feltet **Lagermodell** på siden **Varemodellgrupper** for en vare. Den viktigste forskjellen er at når **Fast mottakspris** brukes, brukes gjeldende kostpris for varen når mottak til lager posteres. Det finnes ingen kostnadsrevalueringsprosess for **Fast mottakspris**, og når en økonomisk oppdatering posteres, brukes gjeldende kostpris ved postering. Hvis det er en forskjell mellom kostprisen som brukes ved mottak og faktura, vil avviket posteres til de faste resultatkontoene for mottakspris.

Hvis du vil bruke en fast mottakspris for et produkt, må du konfigurere følgende:

- På siden **Varemodellgrupper** merker du av for **Poster aktuell beholdning** og **Fast mottakspris**. 
- Det må være merket av for **Poster følgeseddel i finans** på siden **Parametere for beholdnings- og lagerstyring**.
- Angi hovedkontoene for følgende posteringstyper på siden **Lagerposteringsprofil**:
  - Fortjeneste på fast mottakspris
  - Tap på fast mottakspris
  - Motkonto for fast mottakspris

Hvis du vil ha mer informasjon, se [Fast mottakspris](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="purchase-charges-and-stock-variation-posting"></a>Postering av innkjøpsgebyrer og lagervariasjon

Hvis du planlegger å gjøre rede for innkjøpstillegg og lageravvik, må du gjøre følgende:

- På siden **Leverandørparametere** i fanen **Faktura** merker du av for **Postere i belastningskonto i finans**.
- På siden **Varemodellgrupper** for varen som er valgt i bestillingslinjen, merker du av for **Poster fysisk lager**, **Poster økonomisk lager** og **Gjeldsavsetning på mottaksseddel**.
- Merk av for **Generer tillegg for produktkvittering** på siden **Parametere for innkjøp og leverandører**.
- Det må være merket av for **Poster følgeseddel i finans** på siden **Parametere for beholdnings- og lagerstyring**.

På siden **Lagerposteringsprofil** må du angi hovedkontoene for følgende posteringstyper:

- Innkjøpsutgift, ikke-fakturert
- Innkjøpsutgift for produktet
- Lageravvik

> [!NOTE]
> Posteringstypen **Tillgg** brukes ikke når parameteren **Postere i belastningskonto i finans** er valgt.

Hvis du vil ha mer informasjon, se [Regnskapsprinsippet Postere i belastningskonto](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md).

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfigurasjon av posteringsprofil

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og beskrivelser:

- **Avregningskonto**-kolonnen angir at posteringstypen er en avregningskonto. Beløpet som er postert på denne kontoen, tilbakeføres automatisk når en senere transaksjon posteres. 
- **F/Ø**-kolonnen inneholder **F** for fysisk postering og **Ø** for økonomisk postering. 
- **Følg**-kolonnen angir om hovedkontoen for en bestemt posteringstype vanligvis er den samme som en annen posteringstype. Verdien i kolonnen angir posteringstypen som vanligvis brukes.

> [!NOTE]
> Hovedkontoene og hovedkontonavnene er bare forslag. Vi anbefaler<!--note from editor: Via Writing Style Guide.--> at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.


| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Kostnad for innkjøpte materialer mottatt | 140100</br>140101 | Materiallager</br>Materialer sendt, ikke fakturert | Objekt | Debet | Ja | Ø | Kostnad for innkjøpte materialer fakturert | Brukes når et produktmottak for en bestilling posteres, og motposteringen til kontoen er Innkjøpsutgift, ikke-fakturert. Beløpet på denne kontoen tilbakeføres når en bestillingsfaktura posteres. |
| Innkjøpsutgift, ikke-fakturert | 600180 | Materialmottak | Utgift | Debet | Ja | Ø | |Brukes når en bestillingsmottaksseddel posteres. To bilag opprettes for mottak for å spore avvik i innkjøpspris når standard kostpris brukes. Motkontoen på det første bilaget er Innkjøpsavsetning. Motregningen på det andre bilaget er summen av kontoene Kostnad for innkjøpte materialer mottatt og Avvik i kjøpspris. Beløpene som er postert på denne kontoen, tilbakeføres når en bestillingsfaktura posteres. |
| Kostnad for innkjøpte materialer fakturert | 140100 | Materiallager | Objekt | Debet | Nei | F  |Kostnad for innkjøpte materialer mottatt | Brukes når en bestillingsfaktura posteres. Motkontoen for denne kontoen er Innkjøpsutgift, ikke-fakturert for produktet. Denne kontoen representerer lageret i balansen. Kontoen som brukes, er vanligvis den samme kontoen som brukes for Kostnad for enheter, levert og Kostnad for enheter, fakturert for bestilling. |
| Innkjøpsutgift for produktet | 600180 | Materialmottak | Utgift | Kreditt | Ja | F  | |Brukes når en bestillingsfaktura posteres. To bilag opprettes for fakturaen for å spore avvik i innkjøpspris når standard kostpris brukes. Motposteringen til denne kontoen er kontoen Innkjøpsutgift, ikke-fakturert, som brukes på mottaksposteringen og tilbakeføres under fakturaposteringen. Representerer kostnader for beholdningen som er kjøpt ved fakturering, som ikke gjenspeiles i beholdningskontoen i balansen. Dette er en resultatpostering for kjøpsprisavvik som vanligvis vises i vareinnkjøp med standard kostpris.|
| Fast mottaksprisfortjeneste (Innkjøp, fortjeneste på fast mottakspris*) | 510310 | Avvik i kjøpspris | Utgift | Kreditt | Nei | F | Tap på fast mottakspris | Brukes når en bestillingsfaktura posteres, og det er en forskjell mellom den fakturerte prisen og standardkostnaden for varen. Denne kontoen brukes når differansen er høyere. Motkontoen for denne kontoen er Motkonto for fast mottakspris. |
| Fast mottakspristap (Innkjøp, tap på fast mottakspris*) | 510310 | Avvik i kjøpspris | Utgift | Debet | Nei | F | Fortjeneste på fast mottakspris | Brukes når en bestillingsfaktura posteres, og det er en forskjell mellom den fakturerte prisen og standardkostnaden for varen. Denne kontoen brukes når differansen er lavere. Motkontoen for denne kontoen er Motkonto for fast mottakspris. |
| Motkonto for fast mottakspris (Innkjøp, motkonto for fast mottakspris*) | 140900 | Lageravvik | Objekt | Begge | Nei | F  | |Brukes når en bestillingsfaktura posteres, og det er en forskjell mellom den fakturerte prisen og standardkostnaden for varen. Denne kontoen er motkontoen for resultatkontoene for Fast mottakspris. |
| Tillegg | I/T | I/T | I/T | I/T | I/T | I/T | I/T | Denne kontoen brukes ikke lenger. Bruk lagervariasjonen i stedet. |
| Lageravvik | 600170 | Lageravvik | Utgift | Kreditt | Nei | Begge | | Denne kontoen brukes når: <ul><li>Det er forskjell i enhetsprisen mellom produktmottak og faktura.</li><li>Tilleggene posteres til varen.</li><li>Indirekte kostnader er<!--note from editor: Edit okay?--> lagt til de innkjøpte varene. </li><li>Motkontoen til denne kontoen er kontoen Innkjøpsutgift, ikke-fakturert.</li></ul> |
| Innkjøp, avsetning | 200140 | Påløpte innkjøp | Gjeld | Kreditt | Y | Ø | |Brukes når et produktmottak for en bestilling posteres, og alternativet for å avsette innkjøpsbeløp er aktivert. |
| Påløpt merverdiavgift ved mottak | 250500 | Påløpt merverdiavgift | Gjeld | Kreditt | Y | Begge  | |Denne kontoen brukes når du velger alternativet **Poster fysisk merverdiavgift** på **Parametere for beholdnings- og lagerstyring**, og du har en bestilling med mva. Beløpet posteres når du oppdaterer bestillingen fysisk (produktmottak), og tilbakeføres når du posterer bestillingen finansielt (faktura). |
| Anleggsmiddelmottak (Anleggsmiddeldebet*) | 180100 | Materielle anleggsmidler | Objekt | Debet | N | Begge | Begge | Denne kontoen brukes når du velger alternativet på bestillingslinjen for anleggsmidler. Integrering av bestillingen er konfigurert til å anskaffe anleggsmidlet ved produktmottak eller faktura. Hvis du vil ha mer informasjon om integrering av anleggsmiddelbestilling, kan du gå til [Skaffe aktiva ved hjelp av innkjøp](/fixed-assets/acquire-assets-procurement). |
| Innkjøpsutgift for utgiften | 618900 | Diverse utgifter | Utgift | Debet | N | Begge | |Brukes når du posterer et produktmottak eller en faktura for en bestilling der varene ikke er på lager, eller en innkjøpskategori brukes. |
| Forskuddsbetaling | 132190 | Forskuddsbetalt utgift | Objekt | Debet | N | Begge | | Brukes ved behandling av en forskuddsbetalingsfaktura på en bestilling. |


\*Verdiene som vises i parentes, representerer verdien som brukes i feltet **Posteringstype** på siden **Bilagstransaksjoner**. Du kan vise **Posteringstype** på **Generelt**-fanen på siden **Bilagstransaksjoner**.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Anleggsmiddelpostering med bestillinger

Hvis du bruker modulen **Anleggsmidler** og planlegger å kjøpe anleggsmidler via bestillinger, må du konfigurere posteringstypen for **Anleggsmiddelmottak** i kategorien **Bestilling** på **Lagerposteringsprofil**-siden. Hvis du vil ha mer informasjon, kan du gå til [Integrering av fast objekt](/fixed-assets/fixed-asset-integration.md) og [Opprette og anskaffe anleggsmidler som opprettes fra kunder](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md).

## <a name="prepayment-purchase-order-invoice-posting"></a>Postering av faktura til forskuddsbetaling i bestilling

Hvis du planlegger å bruke funksjonen for **Forskuddsbetalt faktura** for bestillinger må posteringstypen **Forskuddsbetaling** velges i fanen **Bestilling** på siden **Lagerposteringsprofil**. Hvis du vil ha mer informasjon, kan du gå til [Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger](/accounts-payable/prepayments-invoices-vs-prepayments.md).

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Postering av innkjøpsrekvisisjon og bestillingsbekreftelse

Innkjøpsrekvisisjoner og bestillingsbekreftelser kan også konfigureres til å postere forhåndsdisposisjoner og disposisjoner til økonomimodulen. Disse posteringene styres av en posteringsdefinisjon. Hvis du vil ha mer informasjon, kan du gå til [Bestillingsdisposisjoner](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances).

## <a name="procurement-category-posting"></a>Postering for innkjøpskategori

Som et alternativ til å konfigurere lagerpostering for alle varer, en varegruppe eller en enkeltvare, kan du konfigurere kategorier og styre finanspostering etter innkjøpkategorier. Hvis du vil ha mer informasjon om hvordan du definerer kategorier og tilordner dem til produkter, kan du gå til [Eksempel på konfigurasjon av posteringsprofil](#sample-posting-profile-configuration) tidligere i denne artikkelen.

Når du bruker kategorier med bestillinger eller leverandørfakturaer, må kategorihierarkiet tilordnes til typen **Innkjøpskategorihierarki** på siden **Kategorihierarkirolletilordninger**.

### <a name="vendor-invoices-with-procurement-categories"></a>Leverandørfakturaer med innkjøpskategorier

Hvis organisasjonen bruker bestillinger for noen innkjøp, og ikke for andre, kan du behandle ikke-bestillingsrelaterte fakturaer på en rekke måter. Dette omfatter bruk av journaler i **Leverandør** eller av siden **Ventende leverandørfakturaer** som brukes til å generere fakturaer for bestillinger. Når du oppretter fakturaer for fakturaer som ikke er knyttet til bestillinger, må du opprette innkjøpskategorier for hver utgiftstype. Du må tilordne kategorien til den riktige utgiftskontoen på siden **Lagerposteringsprofiler**.

Det nøyaktige antallet kategorier vil variere basert på antall utgiftskontoer som du bruker til å postere fakturaene. Du trenger minst én innkjøpskategori for hver hovedkonto som du utgiftsfører ikke-bestillingsfakturaer til. Mange kategorier kan brukes for en enkelt hovedkonto. Dette kan være nyttig for brukervennlighet, søkbarhet og rapportering av utgiftstypene du bruker.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Fordeler ved bruk av innkjøpskategorier for leverandørfakturaer

Noen fordeler ved bruk av innkjøpskategorier for leverandørfakturaer omfatter:

- Konsekvent brukererfaring : Når du konfigurerer innkjøpskategorier for alle utgifter som ikke er knyttet til bestillinger, kan brukere behandle én prosess for fakturering ved å bruke siden **Ventende leverandørfakturaer**.
- Forbedret rapporteringserfaring: Når du konfigurerer innkjøpskategorier for alle varer og alle utgifter som ikke er knyttet til bestillinger, vil rapporten om innkjøpskostnad analysere forbruket etter leverandør, kategori og mer.
- Konsekvent arbeidsflyt: Når du bruker **Ventende leverandørfakturaer** til å behandle alle fakturaer, kan du opprette en konsekvent arbeidsflyt og godkjenningsprosess ved å bruke én enkelt arbeidsflyt.

## <a name="consignment-inventory-posting"></a>Forsendelseslager-postering

Forsendelseslager bruker samme finanspostering som andre innkjøpte varer. Hovedforskjellen er at når lageret mottas, blir det ikke registrert noen finanstransaksjoner. Hvis du vil overføre eierskap til organisasjonen når en **Endring av lagereierskap**-journal posteres, genereres et bilag for å registrere varekostnaden. Hvis du vil ha mer informasjon, kan du gå til [Definere forsendelse](/supply-chain/inventory/consignment.md).
