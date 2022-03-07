---
title: Farlige materialer i produkter, ordrer, forsendelser og laster
description: Dette emnet forklarer hvordan du angir egenskaper for farlige materialer for frigitte produkter, hvordan du kan plassere lagergrenser på farlige varer, og hvordan du inkluderer farlige materialer i en salgsordre, forsendelse eller last.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: d3573aa5f8f986fa4fbf1c9ea8b322a1256aee36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434605"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Farlige materialer i produkter, ordrer, forsendelser og laster

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet forklarer hvordan du angir egenskaper for farlige materialer for frigitte produkter, hvordan du kan plassere lagergrenser på farlige varer, og hvordan du inkluderer farlige materialer i en salgsordre, forsendelse eller last.

## <a name="set-hazardous-material-specifications-for-products"></a>Angi spesifikasjoner for farlige materialer for produkter

Når du har definert en forskrift for farlig materiale og satt opp de tilknyttede referansekodene som beskrevet i [Definere farlige materialer](hazmat-setup.md), kan du knytte denne informasjonen til frigitte varer. Forsendelsesteksten for forsendelsesdokumenter hentes fra informasjonen om farlig materiale for de frigitte varene.

Som en del av prosessen med å knytte en frigitt vare til et farlig materiale, må du angi reguleringskoden og materialet. Forskjellige reguleringskoder kan være knyttet til en vare, avhengig av transportmodus, og du kan knytte flere forskrifter og materialkoder til hver vare.

Følg denne fremgangsmåten for å konfigurere et frigitt produkt som et farlig materiale.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg eller opprett et produkt for å åpne siden **Detaljer om frigitt produkt**.
1. På **Administrer lager**-hurtigfanen angir du **Farlig materiale**-alternativet til **Ja**. Denne innstillingen identifiserer varen som farlig og brukes når forsendelsesdokumentasjonen skrives ut.
1. I handlingsruten, i kategorien **Administrer lager**, i gruppen **Samsvar** velger du valget for **varer med farlig materiale**.
1. Fyll ut siden for **vare, farlig materiale** for den valgte varen ved hjelp av feltene som er beskrevet i følgende underdeler.

### <a name="item-hazardous-materials-header"></a>Overskrift for vare med farlig materiale

Følgende tabell beskriver feltene som er tilgjengelige øverst på siden for **vare, farlig materiale**.

| Felt | beskrivelse |
|---|---|
| Varenummer | Det frigitte produktet du arbeider med. |
| Reguleringskode | Velg farlig materiale-forskriften som gjelder for produktet. Forskriften definerer hvordan den utskrevne forsendelsesteksten blir opprettet for en vare, og de tilknyttede leveringsmåtene. Når koden er tilordnet, kan den ikke redigeres på denne siden. Du kan imidlertid tilordne en ny forskriftskode ved å velge **Ny**. |
| Materialkode | (Valgfritt) Velg farlig materiale-koden som gjelder for produktet. Materialkoden inneholder en mal som inkluderer standardverdier for mange andre felt på denne siden. Når du velger en kode, blir alle spesifikasjonene for farlig materiale kopiert til det gjeldende produktet. Først blir du imidlertid bedt om å bekrefte at materialdata for varen skal fylles ut fra materialkoden. |
| Gruppekode | (Valgfritt) Velg farlig materiale-klassifiseringsgruppekoden som gjelder for produktet. Som for feltet **Materialkode**, når du velger en kode, blir alle spesifikasjonene for farlig materiale kopiert til det gjeldende produktet. Først blir du imidlertid bedt om å bekrefte at klassegruppedata for varen skal fylles ut fra gruppekoden. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Hurtigfanen Beskrivelser

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Beskrivelser**.

| Felt | beskrivelse |
|---|---|
| Riktig forsendelsesnavn | Angi standardbeskrivelsen for materialet, som angitt av gjeldende regulering. Du kan angi oversettelser for denne verdien i hurtigfanen for **Oversettelse av tekst for vareforsendelse**, som beskrevet i neste del. |
| Teknisk navn | Velg det vanlige eller generiske navnet på materialet. Dette navnet kan være et navn som firmaet ditt bruker internt for materialet. |
| N.O.S. | Merk av i denne avmerkingsboksen for å angi at verdien for **Korrekt forsendelsesnavn** er et ikke ellers spesifikt navn (N.O.S.) for varen. N.O.S.-forsendelsesnavn brukes for grupper med lignende kjemikalier og materialer som har spesifikk sluttbruk, men som kanskje ikke er oppført med navn i tabellen for farlig materiale i en bestemt forskrift. |

### <a name="item-ship-text-translation-fasttab"></a>Hurtigfanen Oversettelse av tekst for vareforsendelse

Hurtigfanen **Oversettelse av tekst for vareforsendelse** inneholder et rutenett som viser oversettelser av verdiene for **riktige leveringsnavn** som er definert for det primære språket i hurtigfanen **Beskrivelser**. Disse oversettelsene kan brukes i forsendelsesteksten for ett eller flere tilleggsspråk.

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Oversettelse av tekst for vareforsendelse**.


| Felt | beskrivelse |
|---|---|
| Språk | Språkkoden som raden bruker. For eksempel indikerer **pt-br** brasiliansk portugisisk. |
| Forsendelse - skriv ut tekst | Den oversatte verdien for **Korrekt forsendelsesnavn** på språket som raden bruker. |

Hvis du vil legge til eller redigere en oversettelse, velger du **Oversettelser** over rutenettet for å åpne siden **Tekstoversettelser**. Følg deretter ett av disse trinnene:

- Hvis du vil legge til en ny oversettelsen, velger du **Legg til** i hurtigruten. Velg språket som skal legges til, og skriv deretter inn den oversatte teksten i feltet **Oversatt tekst**.
- Hvis du vil redigere en eksisterende oversettelse, velger du et målspråk i feltet **Språk** og redigerer den oversatte teksten i feltet **Oversatt tekst** etter behov.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Hurtigfanen Materialstyring

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Materialstyring**.

| Felt | beskrivelse |
|---|---|
| Klasse | Velg hvilke klasser av farlig materiale produktet tilhører, slik det er definert av forskriften du overholder. Du må tilordne både en inndeling og en klasse til alle produkter som inneholder farlige materialer. |
| beskrivelse | Beskrivelsen som er definert for klassen som er valgt i feltet **Klasse**. Dette feltet er skrivebeskyttet. |
| Inndeling | Velg inndelingen av farlig materiale produktet tilhører, slik det er definert av forskriften du overholder. Inndelingen er et delsett av klassen. Du må tilordne både en inndeling og en klasse til alle produkter som inneholder farlige materialer. |
| Identifikasjon | Velg identifikasjonskode for det farlige materialet. Vanligvis er denne koden basert på en FN-standard. |
| Emballasjegruppe | Velg emballasjegruppen som gjelder for den gjeldende varen. |
| beskrivelse | Beskrivelsen som er definert for gruppen som er valgt i feltet **Emballasjegruppe**. Dette feltet er skrivebeskyttet. |
| Emballasjebeskrivelser | Velg den gjeldende pakkebeskrivelseskoden. Denne koden refererer til en beskrivelse som angir hvordan produktet må pakkes. |
| Etiketter for farlig materiale | Velg en kode som refererer til den aktuelle etiketten for farlige varer som skal brukes på produktet. |
| Begrenset antall | Sett dette alternativet til **Ja** for å rapportere den totale produktvekten som er inkludert i hver last og på hver lastlinje. |
| Antall | Angi mengden farlig materiale i produktet, i den angitte enheten. Denne verdien brukes til å beregne den totale poengsummen for farlig materiale for laster for forsendelser som inkluderer produktet. |
| Multiplikator | Angi multiplikatoren som brukes når poengsummen for farlig materiale beregnes for hver lastlinje som inkluderer produktet. Denne verdien angis av den gjeldende forskriften i henhold til typen farlig materiale som finnes i produktet. |
| Enhet | Velg måleenheten som gjelder for mengden farlig materiale i produktet, som angitt i **Antall**-feltet. Denne verdien brukes til å beregne den totale poengsummen for farlig materiale for laster for forsendelser som inkluderer produktet. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Hvordan poengsummen for farlig materiale beregnes

Flere av verdiene som er angitt på hurtigfanen for **Materialstyring** for et produkt, brukes til å beregne en *poengsum for farlig materiale* for hver lastlinje som inkluderer dette produktet. Denne poengsummen beregnes ved hjelp av følgende formel:

Poengsum for farlig materiale = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Her er en nøkkel til formelen:

- *&lt;LineQty&gt;* er mengden av produktet som er angitt for en lastlinje.
- *&lt;HazmatQty&gt;* er mengden av farlige materialer som er angitt for et produkt i feltet **Antall** i hurtigfanen **Materialstyring**.
- *&lt;UnitConversion&gt;* er en omregningsfaktor for konvertering mellom enheten som brukes for lastlinjemengden og enheten som er angitt for et produkt i feltet **Enhet** på hurtigfanen **Materialstyring**.
- *&lt;Multiplier&gt;* er multiplikatoren som er angitt for et produkt i feltet **Multiplikator** i hurtigfanen **Materialstyring**.

Denne poengsummen rapporteres for hver lastlinje som inneholder et produkt der disse verdiene er angitt. Hvis du vil ha mer informasjon, kan du se delene [Forsendelser som inneholder farlige materialer](#hazmat-shipments), og [Laster som inneholder farlige materialer](#hazmat-loads) senere i dette emnet.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Hvordan vekt for farlig materiale beregnes

Last- og lastlinjer som inneholder varer der alternativet **Begrenset antall** på hurtigfanen **Materialstyring** er satt til **Ja**, viser den totale vekten av farlig materiale, som beskrevet i delene [Forsendelser som inneholder farlige materialer](#hazmat-shipments) og [Laster som inneholder farlige materialer](#hazmat-loads) senere i dette emnet. Vekten av farlig materiale beregnes ved hjelp av følgende formel:

Vekt av farlig materiale = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Her er en nøkkel til formelen:

- *&lt;LineQty&gt;* er mengden av produktet som er angitt for en lastlinje.
- *&lt;ProductWeight&gt;* er nettovekten som er angitt for produktet i lagerenheten som er angitt for produktet.
- *&lt;UnitConversion&gt;* er en omregningsfaktor for konvertering mellom enheten som brukes for lastlinjemengden og lagerenheten som brukes for *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>Hurtigfanen Transportinformasjon

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien **Transportinformasjon**.

| Felt | beskrivelse |
|---|---|
| Transportkategori | Velg den tilknyttede transportkategorien. |
| Tunnelkode | Velg den tilknyttede tunnelrestriksjonskoden for varen. |
| Farlig materiale - stuing | Velg referansekoden som brukes til håndtering av skipsfrakt når varen sendes med sjøfrakt. |
| Flytype | Velg flybegrensningen som gjelder for materialet når den sendes via flyfrakt. |
| Emballasje - bare godsfly | Basert på verdien du valgte i feltet **Flytype**, velger du emballasjeinstruksjonskoden som gjelder når produktet bare kan leveres via luftlast. |
| Emballasje - passasjer- og godsfly | Basert på verdien du valgte i feltet **Flytype**, velger du emballasjeinstruksjonskoden som gjelder når produktet kan leveres som fraktflyfrakt eller passasjerflyfrakt. |
| IATA-stjerne | Sett dette alternativet til **Ja** for å angi at flytransportspesifikasjonene som angis i denne hurtigfanen, er knyttet til standarden i det internasjonale lufttransportforbundet (IATA) for farlig gods. Dette feltet er bare beregnet til informasjon. |
| Nødberedskap | Velg koden som henviser til instruksjoner for å behandle materialet i en krisesituasjon. |

### <a name="environmental-information-fasttab"></a>Hurtigfanen for Miljøinformasjon

Følgende tabell beskriver feltene som er tilgjengelige i hurtigkategorien for **Miljøinformasjon**.

| Felt | beskrivelse |
|---|---|
| Farlig for miljø | Sett dette alternativet til **Ja** for å angi at produktet er miljømessig farlig. Bruk dette feltet til dine egne rapporteringsformål. |
| Marin forurensningskilde | Sett dette alternativet til **Ja** for å angi at produktet fører til havforurensning. Bruk dette feltet til dine egne rapporteringsformål. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Angi lagringsgrenser for farlige produkter

Av sikkerhetsmessige årsaker må du kanskje begrense den totale mengden av et gitt produkt som kan lagerføres på ett sted. Hvis du vil angi lagringsgrenser for et frigitt produkt, følger du fremgangsmåten nedenfor.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg et produkt for å åpne siden **Detaljer om frigitt produkt**.
1. I handlingsruten, i kategorien **Administrer lager**, i gruppen **Samsvar** velger du valget for **Rapporteringsdetaljer**.
1. I feltene for **grense for farlig lagerbeholdning** og **grense for advarsel om fare** angir du de riktige verdiene for det valgte produktet.

Rapporten om **grense for farlig lagerbeholdning** lar deg overvåke lagernivåene for farlige materialer på lagerlokasjonene, for å sørge for at de forblir under de sikre grensene som blir opprettet her. Hvis du vil ha mer informasjon, se [rapporten om grense for farlig lagerbeholdning](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Salgsordretransaksjoner som inneholder farlige materialer

Hvis du vil inkludere et produkt som er klassifisert som et farlig materiale i en salgsordre, må du knytte den aktuelle transportøren til salgsordren. Åpne salgsordren, og deretter, på hurtigfanen **Levering**, angir du feltene **Transportør** og **Transportørservice** etter behov.

Transportøren er også knyttet til leveringsmåten. Derfor må du kontrollere at denne informasjonen er i tråd med forskriften for det farlige materialet. Med andre ord må leveringsmåten som er angitt i forskriften for det farlige materialet, samsvare med spesifikasjonene i salgsordrehodet. På denne måten er forskriften, transportøren og servicen koblet til forsendelseslinjene som brukes på en salgsordre.

Når en salgsordre er sluttført og klar til å sendes, kan den frigis til lageret for å vise overføringen mellom salgs- og lageroperasjoner.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Forsendelser som inneholder farlige materialer

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Vise poengsummer for farlige materialer for hver forsendelseslinje

Siden **Forsendelsesdetaljer** for en forsendelse viser de totale verdiene for poengsum og vekt for farlige materialer som er beregnet for hver lastlinje som er inkludert i denne forsendelsen. Følg denne fremgangsmåten for å vise poengsummene og vektene.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Velg en forsendelse for å åpne siden **Forsendelsesdetaljer**.
1. I hurtigfanen **Lastlinjer** kontrollerer du linjene. For hver linje vil du se beregningene for farlig materiale i følgende felt:

    - **Poengsum for farlig materiale** – Dette feltet viser poengsummen for farlig materiale for lastlinjen. Verdien beregnes i henhold til reglene og verdiene som er fastsatt for den aktuelle forskriften og i oppsettet for det frigitte produktet. Beregningen tar antallet på lastlinjen og refererer til multiplikatoren i [materialstyringsoppsettet](#material-management) for det frigitte produktet.
    - **Nettovekt for begrenset mengde** – For produkter som er merket som varer med begrenset mengde på grunn av deres innhold av farlig materiale, viser dette feltet den totale nettovekten av farlig innhold som er inkludert på lastlinjen. Beregningen er basert på produktene som er merket som farlige materialer i det frigitte produktoppsettet. Hvis en vare er merket som en begrenset vare, tar beregningen mengden på hver lastlinje og refererer til vekten i [materialstyringsoppsettet](#material-management) for det frigitte produktet.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Sjekke kompatibilitet mellom farlige materialer som er inkludert i en forsendelse

Systemet kan evaluere om alle farlige materialer som er inkludert i en forsendelse, er passende å bli sendt sammen. For å evaluere kompatibilitet kontrollerer systemet at kompatibilitetsnivået som er tilordnet hvert produkt, er inkludert i forsendelsen. Hvis du vil ha mer informasjon, se [Kompatibilitetsgrupper for farlig materiale](hazmat-setup.md#compatibility-groups).

Følg denne fremgangsmåten for å kjøre kompatibilitetssjekken.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Velg en forsendelse for å åpne siden **Forsendelsesdetaljer**.
1. Velg **Kompatibilitetskontroll** i gruppen **Handlinger** i fanen **Forsendelser**.

Du får en melding som gir deg beskjed om resultatet av sjekken.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Laster som inneholder farlige materialer

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Vise poengsummer for farlige materialer for hver lastlinje

Siden **Lastdetaljer** for en last viser de totale verdiene for poengsum og vekt for farlige materialer som er beregnet for lasten og hver lastlinje. Følg denne fremgangsmåten for å vise poengsummene og vektene.

1. Gå til **Lagerstyring \> Forsendelser \> Alle laster**.
1. Velg en last for å åpne siden **Lastdetaljer**. (Du kan også åpne lastdetaljer ved å velge en kobling fra en tilknyttet forsendelse.)
1. I hurtigfanen **Last** kan du gå gjennom totale poengsummer og vekter for farlige materialer for hele lasten ved å se på følgende felt:

    - **Poengsum for farlig materiale** – Dette feltet viser poengsummen for farlig materiale for lasten. Verdien beregnes i henhold til reglene og verdiene som er fastsatt for den aktuelle forskriften og i oppsettet for det frigitte produktet. Beregningen tar antallet som er inkludert i lasten og refererer til multiplikatoren i [materialstyringsoppsettet](#material-management) for det frigitte produktet.
    - **Nettovekt for begrenset mengde** – For produkter som er merket som varer med begrenset mengde på grunn av deres innhold av farlig materiale, viser dette feltet den totale nettovekten av farlig innhold som er inkludert i lasten. Beregningen er basert på produktene som er merket som farlige materialer i det frigitte produktoppsettet. Hvis en vare er merket som en begrenset vare, tar beregningen mengden i hver last og refererer til vekten i [materialstyringsoppsettet](#material-management) for det frigitte produktet.

1. Hvis du vil se over resultatene og vektene for enkeltlinjer, velger du hurtigfanen **Lastlinjer**. Verdiene som gis for hver linje, ligner på verdiene som oppgis for hele laste, som beskrevet i forrige trinn.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Sjekke kompatibilitet mellom farlige materialer som er inkludert i en last

Systemet kan evaluere om alle farlige materialer som er inkludert i en last, er passende å bli sendt sammen. For å evaluere kompatibilitet kontrollerer systemet at kompatibilitetsnivået som er tilordnet hvert produkt, er inkludert i lasten. Hvis du vil ha mer informasjon, se [Kompatibilitetsgrupper for farlig materiale](hazmat-setup.md#compatibility-groups).

Følg denne fremgangsmåten for å kjøre kompatibilitetssjekken.

1. Gå til **Lagerstyring \> Forsendelser \> Alle laster**.
1. Velg en forsendelse for å åpne siden **Lastdetaljer**. (Du kan også åpne lastdetaljer ved å velge en kobling fra en tilknyttet forsendelse.)
1. Velg **Kompatibilitetskontroll** i gruppen **Handlinger** i fanen **Laster**.

Du får en melding som gir deg beskjed om resultatet av sjekken.
