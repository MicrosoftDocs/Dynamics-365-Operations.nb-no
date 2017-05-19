---
title: Treveis kontrollpolicyer
description: "Denne artikkelen inneholder eksempler på treveis samsvar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e564405420c261a172447daa7044fc1e8477039a
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="three-way-matching-policies"></a>Treveis kontrollpolicyer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder eksempler på treveis samsvar.

<a name="example-three-way-matching-for-items"></a>Eksempel: Treveis kontrollpolicyer for varer
-------------------------------------

**Sammendrag:** Ken er kontrolleren i firmaets hovedkontor for en juridisk enhet kalt Fabrikam. Ken bestemmer seg for at alle leverandørfakturaer som er basert på bestillinger, skal sammenlignes med bestillingslinjer (toveis kontroll). For innkjøp av varer som skal brukes som anleggsmidler, skal fakturaer sammenlignes med både bestillingslinjene og produktkvitteringslinjene (treveis kontroll).

Fabrikam opererer med flere juridiske enheter og ansatte i alle deler av verden. Når antall transaksjoner øker, øker også avvik mellom kvitteringer og fakturaer. Dette fører til at anleggsmidler avskrives. Fakturaer fra leverandører blir betalt, men prosessen omfatter ikke identifikasjon av avvik når det mottas færre varer enn bestilt, eller når varene ikke mottas i det hele tatt. Forbruket øker også fordi ansatte fremdeles trenger verktøy og andre materialer for å gjøre jobben sin. Ken ønsker å være sikker på at leverandørene sender produktene som er bestilt, og at varene mottas av ansatte i Fabrikam. Ken krever derfor toveis og treveis kontroll for alle juridiske enheter i organisasjonen. Fakturakontroll sørger for at problemer med varer som har forsvunnet eller ikke er mottatt, kan spores og løses. 

Fakturakontrollpolicyer i dette eksemplet hjelper personer i følgende roller med å oppfylle dette:

-   Ken er kontrolleren til Fabrikam-organisasjonen. Han kan hjelpe personer i organisasjonen med å identifisere og løse problemer med bestilling, mottak og betaling av varer (varer og tjenester) fra leverandører.
-   Phyllis og April er ledere i leverandøravdelingen for Fabrikam i USA. De kan håndheve firmaets policy og sørge for at fakturaer bare betales etter at fakturaene er sammenlignet med bestillingen og mottaket av varer og tjenester, der det er aktuelt.
-   Tony er produksjonssjefen for Fabrikam i USA Han og andre ansatte i produksjonen kan sørge for at varene mottas slik de ble bestilt fra leverandørene, og blir inkludert slik at ansatte har det de trenger for å utføre jobben sin.

### <a name="prerequisites"></a>Forutsetninger

-   Ken setter kontrollpolicyen for det juridiske enhetsnivået til treveis kontroll.
-   Ken angir statusen for automatisk oppdatering av hodekontroll for den juridiske enheten til Ja.
-   Ken setter feltet Tilpass samlet pris for den juridiske enheten til Prosent og setter inn 15 % som toleranseprosent.
-   Ken setter kontrollpolicyen på varenivå for vare 1500 – CNC Milicron maskin til Treveis samsvar. Denne varen en anleggsmiddelvare som skal brukes til produksjon i Fabrikam. Fakturaer for denne varen sammenlignes med bestillingslinjer for priser og med produktkvitteringer for antall.
-   Tony angir en innkjøpsrekvisisjon for fem CNC Milicron maskiner. Alicia, en kontormedarbeider hos Fabrikam, utsteder en bestilling til en juridisk enhet kalt Contoso for levering av varene.

    | Varenummer                 | Antall | Enhetspris | Nettobeløp | Tilleggskode        | Gebyrverdi |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron maskin | 5        | 8 000,00   | 40 000,00  | Forsendelse og behandling | 3 000,00      |

-   Magnus, en regnskapsmedarbeider hos Contoso, ser gjennom forsendelser for uken. Arnie velger forsendelsestransaksjoner for å fakturere Fabrikam for levering av CNC Milicron-maskinene. Magnus inkluderer et tillegg for forsendelse og håndtering. Fabrikam anser tillegget som en del av anleggsmiddelkostnaden.

### <a name="scenario"></a>Scenario

1.  Sammy, en arbeider i mottaksavdelingen i Fabrikam, mottar det totale antallet maskiner som sendes fra Contoso. Han angir et antall på 5 på en produktkvittering. Fordi bestillingen er fullstendig mottatt, endres statusen for bestillingen til Mottatt.
2.  April, en leverandørkoordinator på Fabrikam, legger inn og bekrefter fakturaen som er sendt av Contoso. Hun kontrollerer følgende informasjon:
    -   Ved varer som krever treveis samsvar, samsvarer antallet på fakturalinjen med antallet som ble mottatt. Det mottatte antallet er angitt på produktkvitteringen som er samsvart med fakturaen.
    -   For varer som krever toveis eller treveis samsvar er prisene på fakturalinjen innenfor toleransene som er definert i Microsoft Dynamics 365 for Operations. Dette inkluderer følgende typer prissamsvar:
        -   Nettoenhetspriskontroll – Nettoenhetsprisen på fakturalinjen samsvarer med nettoenhetsprisen på bestillingslinjen, innenfor toleranseprosenten. I dette eksemplet er toleransen for nettoenhetsprisen +8 %.
        -   Pristotalkontroll – Nettobeløpet på fakturalinjen samsvarer med nettobeløpet på bestillingslinjen, innenfor toleranseprosenten, beløpet eller prosenten og beløpet. I dette eksemplet er toleransen for pristotalkontroll +15 %.

Papirfakturaen fra Contoso inneholder følgende informasjon.

| Vare                        | Antall | Enhetspris | Nettobeløp |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron maskin | 5        | 8 100.00   | 40 500,00  |
| Forsendelse og behandling       |          |            | 4 000,00   |
| Mva                         |          |            | 0,00       |
| Sum                       |          |            | 44 500,00  |

Fakturalinjen inneholder følgende informasjon i Microsoft Dynamics 365 for Operations.

| Varenummer                 | Antall | Enhetspris | Nettobeløp for linje | Kontrollpolicy    | Samsvar i antall i produktkvittering | Prissamsvar | Pristotalsamsvar |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron maskin | 5        | 8 100.00   | 40 500,00       | Treveis samsvar | Sendt                         | Sendt      | Sendt            |

Fordi denne linjen består fakturakontrollprosessen, kan fakturaen posteres.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Eksempel: Treveis samsvar for vare- og leverandørkombinasjoner
Sammendrag: Ken er kontrolleren i firmaets hovedkontor for en juridisk enhet kalt Fabrikam. Ken bestemmer seg for at alle fakturaer som er basert på bestillinger, skal sammenlignes med bestillingslinjer (toveis kontroll). Cassie er regnskapsføreren i Malaysia-kontoret til Fabrikam. Hun angir at valgte varer som bestilles fra bestemte leverandører i Malaysia, bør kontrolleres mot både bestillingslinjer og produktkvitteringslinjene (treveis samsvar). Hun kan også overstyre kontrollpolicyen til et høyere kontrollnivå for bestemte bestillinger. 

Volumet og beløpene er små, og det har vært problemer med leveringen fra noen leverandører i Malaysia. Derfor setter Cassie kontrollnivået for enkelte vare- og leverandørkombinasjoner som er kjøpt i Malaysia, til treveis kontroll. 

Fakturakontrollpolicyer i dette eksemplet hjelper personer i følgende roller med å oppfylle dette:
-   Ken er kontrolleren til Fabrikam-organisasjonen. Han kan hjelpe personer i organisasjonen med å identifisere og løse problemer med bestilling, mottak og betaling av varer (varer og tjenester) fra leverandører.
-   Cassie er regnskapsføreren for Malaysia-kontoret til Fabrikam. Hun kan håndheve firmaets policy og sørge for at fakturaer bare betales etter at de er sammenlignet med bestillingslinjene og produktkvitteringene som representerer mottaket av varer og tjenester. Hun kan også øke kontrollnivået til treveis samsvar for bestemte varer for å kontrollere driftskostnader.

### <a name="prerequisites"></a>Forutsetninger

-   Ken setter kontrollpolicyen for det juridiske enhetsnivået til toveis kontroll.
-   Ken setter feltet Tilpass samlet pris for den juridiske enheten til Prosent og setter inn 10 % som toleranseprosent.
-   Ken setter enhetsprisetoleransen for alle varer til 2 %.
-   Cassie setter kontrollpolicyen for vare- og leverandørskombinasjonsnivået for vare PH2500 – datamaskin og leverandøren Contoso til treveis samsvar.
-   Alicia, en kontormedarbeider på Malaysia-kontoret til Fabrikam, sender bestillinger på tre varer til Contoso, som vist i følgende tabell. Når hun oppretter bestillingen, overstyrer hun kontrollpolicyen for den trådløse musen til treveis kontroll i stedet for toveis.

    | Varenummer           | Antall | Enhetspris | Nettobeløp | Kontrollpolicy (standardoppføring) | Kontrollpolicy (på bestillingslinjen) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – datamaskin     | 2        | 2 500,00   | 5 000,00   | Treveis samsvar              | Treveis samsvar                           |
    | MM01 – trådløs mus | 2        | 40,00      | 80,00      | Toveis samsvar                | Treveis samsvar                           |
    | USB-enhet             | 200      | 10,00      | 2 000,00   | Toveis samsvar                | Toveis samsvar                             |

### <a name="scenario"></a>Scenario

1.  Varene ankommer. Sammy, en arbeider i mottaksavdelingen på Malaysia-kontoret til Fabrikam, blir avbrutt og bokfører ikke produktkvitteringen med en gang.
2.  April, en leverandørkoordinator på Fabrikam, legger inn og bekrefter fakturaen som er sendt av Contoso. Hun kontrollerer følgende informasjon:
    -   Ved varer som krever treveis samsvar, samsvarer antallet på fakturalinjen med antallet som ble mottatt. Det mottatte antallet er angitt på produktkvitteringen som er samsvart med fakturaen.
    -   For varer som krever toveis eller treveis samsvar er prisene på fakturalinjen innenfor toleransene som er definert i Microsoft Dynamics 365 for Operations. Dette inkluderer følgende typer prissamsvar:
        -   Nettoenhetspriskontroll – Nettoenhetsprisen på fakturalinjen samsvarer med nettoenhetsprisen på bestillingslinjen, innenfor toleranseprosenten. I dette eksemplet er toleransen for nettoenhetsprisen +2 %.
        -   Pristotalkontroll – Nettobeløpet på fakturalinjen samsvarer med nettobeløpet på bestillingslinjen, innenfor toleranseprosenten, beløpet eller prosenten og beløpet. I dette eksemplet er toleransen for pristotalkontroll +10 %.

Papirfakturaen fra Contoso inneholder følgende informasjon.

| Vare                  | Antall | Enhetspris | Nettobeløp |
|-----------------------|----------|------------|------------|
| PH2500 – datamaskin     | 2        | 2 500,00   | 5 000,00   |
| MM01 – trådløs mus | 2        | 41,00      | 82,00      |
| USB-enhet             | 200      | 10,05      | 2 010,00   |
| Totalt faktura         |          |            | 7 092,00   |

Fakturalinjen inneholder følgende informasjon i Microsoft Dynamics 365 for Operations.

| Varenummer           | Antall | Enhetspris | Nettobeløp for linje | Kontrollpolicy    | Samsvar i antall i produktkvittering | Prissamsvar | Pristotalsamsvar |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – datamaskin     | 2        | 2 500,00   | 5 000,00        | Treveis samsvar | Mislykket                         | Sendt      | Sendt            |
| MM01 – trådløs mus | 2        | 41,00      | 82,00           | Treveis samsvar | Mislykket                         | Mislykket      | Sendt            |
| USB-enhet             | 200      | 10,05      | 2 010,00         | Toveis samsvar   |                                | Sendt      | Sendt            |

Merk følgende:
-   I linjen for PH2500 – datamaskin inneholder kolonnen Samsvar i antall i produktkvittering et varselikon fordi fakturalinjen ikke er kontrollert mot en produktkvittering.
-   I linjen for MM01 – trådløs mus inneholder kolonnen Samsvar i antall i produktkvittering et varselikon fordi fakturalinjen ikke er kontrollert mot en produktkvittering. Enhetsprissamsvar-kolonnen inneholder et advarselsikon fordi nettopristoleransen på 2 % er overskredet.
-   I linjen for USB-enhet er kolonnen Samsvar i antall i produktkvittering tom fordi toveis samsvar ikke har samsvar mellom antallet på fakturalinjen og produktkvitteringslinjen.

Hvis godkjenning er nødvendig for at fakturaer kan posteres med fakturauoverensstemmelser, må Godkjenn postering med samsvarende avvik på siden Fakturakontrolldetaljer velges før fakturaen kan posteres med prissamsvarsfeil og antallsamsvarsfeil. Hvis godkjenning ikke kreves, kan fakturabehandlingen fortsette hvis det ikke er andre posteringsfeil.


Hvis du vil ha mer informasjon, kan du se [Fakturasamsvar for leverandører](accounts-payable-invoice-matching.md).




