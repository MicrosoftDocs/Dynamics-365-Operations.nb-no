---
title: Salgsordrepostering
description: Denne artikkelen inneholder informasjon om Salgsordre-fanen på siden for lagerposteringsprofil.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 5ea1c3c90b32d18243615e3ff283e1e818ac23b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886320"
---
# <a name="sales-order-posting"></a>Salgsordrepostering

**Salgsordre**-fanen på siden **Lagerposteringsprofiler** brukes til å styre hvordan salgsordrer skal posteres i økonomimodulen. To hovedaktiviteter posteres i økonomimodulen for en salgsordre: 

- Følgeseddel
- Faktura

For at en fysisk transaksjon (følgeseddel) skal kunne posteres i økonomimodulen for en salgsordre, må følgende betingelser oppfylles:

- Det må være merket av for **Poster følgeseddel i finans** på siden **Parametere for beholdnings- og lagerstyring**.
- Det må være merket av for **Poster aktuell beholdning i finans** på siden **Varemodellgruppe** for varen som er valgt på salgsordrelinjen.
- På siden **Lagerposteringsprofil** må hovedkontoene angis for følgende posteringstyper:
  - Kostnad for enheter, levert
  - Solgte varers kostnad, levert

For at en finanstransaksjon (faktura) skal kunne posteres i økonomimodulen for en salgsordre, må følgende betingelser oppfylles:

- Det må være merket av for **Poster økonomisk lager i finans** på siden **Varemodellgruppe** for varen som er valgt på salgsordrelinjen.
- Hovedkontoene må være angitt på siden **Lagerposteringsprofil** for følgende posteringstyper:
  - Kostnad for enheter, fakturert
  - Solgte varers kostnad, fakturert
  - Inntekt
  - Rabatt\*

> [!NOTE]
> Rabatt-kontoen er valgfri. Mange regnskapsregler, for eksempel GAAP og IFRS, krever at rabatter reduserer salgsinntektene, og derfor brukes ikke disse kontoene i mange scenarioer. Hvis lokale bestemmelser tillater det, bruker du en separat hovedkonto til å postere delen av salgsprisen som er rabattert.

Hvis du vil postere den utsatte (estimerte) inntektsverdien i økonomimodulen når du genererer en følgeseddel for en salgsordre, må følgende betingelser være oppfylt:

- Det må være merket av for **Poster aktuell beholdning i finans** på siden **Varemodellgruppe** for varen som er valgt på salgsordrelinjen.
- Det må være merket av for **Poster til utsatt inntektskonto ved salgslevering** på siden **Varemodellgruppe**.
- Det må være merket av for **Poster følgeseddel i finans** på siden **Parametere for beholdnings- og lagerstyring**.
- Det må være merket av for **Poster fysisk merverdiavgift** på siden **Parametere for beholdnings- og lagerstyring**.
- Det må være merket av for **Poster følgeseddel i finans** på siden **Parametere for kundereskontro**.
- På siden **Lagerposteringsprofil** må hovedkontoene angis for følgende posteringstyper:
  - Utsatt inntekt ved levering
  - Utsatt motregning ved levering
  - Utsatt merverdiavgift for levering

> [!NOTE]
> Vi anbefaler generelt at du aktiverer alternativene **Poster aktuell beholdning** og **Poster følgeseddel i finans**. Når du aktiverer disse alternativene, bidrar det til å fremskynde månedsavslutningsprosedyrene siden ingen periodisering må beregnes og posteres manuelt. Regnskapsoppgjør gjenspeiler i tillegg de utsatte beløpene automatisk uten at noe må gjøres manuelt.

> [!IMPORTANT]
> Alternativet **Poster til utsatt inntektskonto ved salgslevering** brukes ikke med inntektsføring. Hvis du vil ha mer informasjon om inntektsføring, kan du gå til [Oversikt over inntektsføring](/accounts-receivable/revenue-recognition-overview.md)

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfigurasjon av posteringsprofil 

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og beskrivelser:
 
- **Avregningskonto**-kolonnen angir at posteringstypen er en avregningskonto. Beløpet som er postert på denne kontoen, tilbakeføres automatisk når en senere transaksjon posteres. 
- **F/Ø**-kolonnen inneholder **F** for fysisk postering og **Ø** for økonomisk postering. 
- **Følg**-kolonnen angir om hovedkontoen for en bestemt posteringstype vanligvis er den samme som en annen posteringstype. Verdien i kolonnen angir posteringstypen som vanligvis brukes.

> [!NOTE]
> Disse hovedkontoene og hovedkontonavnene er bare forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.


| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|------------|------------------------|-------------------------|--------------|---------|-------------------|------------|------|-------------------------|
| Kostnad for enheter, levert | 140100</br>140101 | Materiallager</br>Materialer sendt, ikke fakturert | Objekt | Kreditt | Ja | Ø | Kostnad for enheter, fakturert | Brukes når en følgeseddel for salgsordre posteres. Motkontoen for kontoen er Solgte varers kostnad, levert. Beløpet på denne kontoen tilbakeføres når en salgsordrefaktura posteres. Du vil kanskje bruke kontoen Materialer sendt, ikke fakturer til å representere den aktuelle beholdningen, og reservere kontoen Materiallager til den økonomiske oppdateringen. |
| Solgte varers kostnad, levert | 500150 | Utsatt vareforbruk | Utgift | Debet | Ja | Ø  | Brukes når en følgeseddel for salgsordre posteres. Motkontoen for kontoen er Kostnad for enheter, levert. Beløpet på denne kontoen tilbakeføres når en salgsordrefaktura posteres. |
| Kostnad for enheter, fakturert | 140100 | Materiallager | Objekt | Kreditt | Nei | Ø | Kostnad for enheter, levert | Brukes når en salgsordrefaktura posteres. Motkontoen for denne kontoen er Solgte varers kostnad, fakturert. Denne kontoen representerer lageret i balansen. |
| Solgte varers kostnad, fakturert | 500100 | Vareforbruksmaterialer | Utgift | Debet | Nei | Ø  | Brukes når en salgsordrefaktura posteres. Motkontoen for denne kontoen er Kostnad for enheter, fakturert. Denne kontoen representerer vareforbruket i resultatregnskapet. |
| Inntekt (salgsordreinntekt*) | 400100 | Inntektsmaterialer | Inntekt | Kreditt | Nei | Ø   | Brukes når en salgsordrefaktura posteres. Motkontoen for denne kontoen er samlekontoen (kundesaldo*) i **Posteringsprofil for kunder**. |
| Provisjon (salg, provisjon*) | 602150 | Provisjonsutgifter | Utgift | Debet | Nei | Ø  | Brukes når provisjon aktiveres og beregnes for et salg og posteres i løpet av fakturaprosessen for salgsordre. Motkontoen for denne kontoen er Skyldig provisjon. |
| Provisjonsmotkonto (salg, provisjonsmotkonto*) | 201110 | Skyldige provisjoner | Gjeld | Kreditt | Ja | Ø | Brukes når provisjon aktiveres og beregnes for et salg og posteres i løpet av fakturaprosessen for salgsordre. Motkontoen for denne kontoen er Provisjonsutgifter. |
| Utsatt inntekt for levering (Salg – følgeseddelomsetning*) | 401400 | Påløpt salg | Inntekt | Kreditt | Ja | Ø  | Brukes når Utsatt inntekt for levering aktiveres og posteres når du behandler en følgeseddel for salgsordre. Motkontoen for denne kontoen er Motregning for utsatt inntekt. Beløpene på denne kontoen tilbakeføres automatisk når du posterer salgsordrefakturaen. |
| Utsatt motregning ved levering (Salg – motregning for følgeseddelomsetning)* | 130400 | Kunder – ikke fakturert | Objekt | Debet | Ja | Ø  | Brukes når Utsatt inntekt for levering aktiveres og posteres når du behandler en følgeseddel for salgsordre. Motkontoen for denne kontoen er Utsatt inntekt ved levering. Beløpene på denne kontoen tilbakeføres automatisk når du posterer salgsordrefakturaen. |
| Utsatt merverdiavgift for levering (Salg, følgeseddelsavgift*) | 250500 | Utsatt merverdiavgift | Gjeld | Kreditt | Ja | Ø  | Brukes når Utsatt inntekt for levering er aktivert og Poster fysisk merverdiavgift er aktivert. Avgiftsbeløpet posteres når du behandler en følgeseddel for salgsordre. |

\*Verdiene som vises i parentes i denne tabellen, representerer verdien som brukes i feltet **Posteringstype** på siden **Bilagstransaksjoner**. Du kan vise **Posteringstype** i **Generelt**-fanen på siden **Bilagstransaksjoner**.

## <a name="sales-category-posting"></a>Salgskategoripostering

Som et alternativ til å konfigurere lagerpostering for alle varer, en varegruppe eller en enkeltvare, kan du konfigurere kategorier og styre finanspostering etter salgskategorier. Hvis du vil ha mer informasjon om hvordan du konfigurerer et kategorihierarki og tilordner kategorier til produkter, kan du gå til [Opprette et hierarki for produktklassifisering](/supply-chain/pim/tasks/create-hierarchy-product-classification.md) og [Klassifisere et produkt ved hjelp av kategorihierarkier](/supply-chain/pim/tasks/classify-product-category-hierarchies.md).

Etter at du har opprettet et kategorihierarki, må du tilordne hierarkiet til én eller flere typer. Hvis du vil bruke et kategorihierarki på salgsordrer, må du tilordne kategorien til typen Salgskategorihierarki. Hvis du vil ha mer informasjon, kan du gå til [Om kategorihierarkier](/dynamicsax-2012/appuser-itpro/about-category-hierarchies.md).

## <a name="create-revenue-posting-by-sales-category"></a>Opprette inntektspostering etter salgskategori

Følg denne fremgangsmåten for å tilordne finansposteringer for en salgsordre basert på en salgskategori:

1. Gå til **Lagerstyring** > **Oppsett** > **Postering** > **Postering**.
2. Velg **Salg**-fanen.
3. Velg alternativknappen for posteringstypen du vil konfigurere (for eksempel **Inntekt**).
4. Velg **Ny**.
5. Velg **Kategori** i **Varekode**-feltet.
6. Bruk feltet **Kategorirelasjon** til å velge kategorien for posteringsprofilen.
7. Velg et alternativ for **Tabell**, **Gruppe** eller **Alle** i **Kontokode**-feltet. Hvis du for eksempel vil bruke posteringsprofilen på alle kunder, velger du **Alle**.
   - Hvis du valgte **Tabell** i trinn 6, velger du det spesifikke **Leverandørnummer** for posteringsprofilen i feltet **Kontorelasjon**.
   - Hvis du valgte **Gruppe** i trinn 6, velger du den spesifikke **Leverandørgruppe** for posteringsprofilen i feltet **Kontorelasjon**.
   - Hvis du valgte **Alle** i trinn 6, blir feltet **Kontorelasjon** stående tomt.

8. Hvis du vil tilknytte en bestemt avgiftsgruppe som har den valgte posteringstypen, velger du en **Merverdiavgiftsgruppe**. Hvis du lar dette feltet stå tomt, gjelder posteringstypen alle eksisterende avgiftsgrupper. Posteringer som er angitt for avgiftsgrupper, gjelder bare transaksjoner for salg og kjøp.

9. I **Hovedkonto**-feltet angir du kontonummeret du vil postere kontotypen til. Velg ett av de eksisterende kontonumrene i kontoplanen.
