---
title: Handlingsmeldinger
description: En handlingsmelding er et systemgenerert forslag til endring av en eksisterende planlagt eller autorisert ordre.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570261"
---
# <a name="action-messages"></a>Handlingsmeldinger

[!include [banner](../includes/banner.md)]

En handlingsmelding er et systemgenerert forslag til endring av en eksisterende planlagt, godkjent eller autorisert ordre.

Handlingsmeldinger genereres av hovedplanleggingsberegningen som svar på endrede krav. Forsendelsesdatoen eller antallet kan for eksempel være endret på en salgsordre etter at du allerede har opprettet en bestilling for å innfri behovet for denne salgsordren. I så fall genererer hovedplanleggingsberegningen én eller flere handlingsmeldinger som foreslår at du oppdaterer bestillingen. Du bestemmer om du vil gjøre endringene som foreslås.

Du kan konfigurere hvordan handlingsmeldinger skal beregnes for en dekningsgruppe som du legger ved en vare.

## <a name="select-action-messages"></a>Velge handlingsmeldinger

På **Dekningsgrupper**-siden kan du velge handlingsmeldingene som du vil at systemet skal generere, og dekningsgruppene eller -varene som meldingen gjelder for. Tabellen nedenfor inneholder handlingsmeldingene du kan velge.

| Melding | Beskrivelse |
|---|---|
| Fremskynd | Systemet genererer handlingsmeldinger, etter behov, for å flytte ordrer til en tidligere dato. I feltet **Fremskyndingsmargin** kan du angi maksimalt antall dager mellom et mottak og en avgang uten en fremskyndelseshandling. |
| Utsett | Systemet genererer handlingsmeldinger, etter behov, for å flytte ordrer til en senere dato. I feltet **Utsettelsesmargin** kan du også angi maksimalt antall dager mellom et mottak og en avgang uten en utsettelseshandling. |
| Nedskriv | Systemet genererer handlingsmeldinger når produksjonsordrer, bestillinger og andre mottakstransaksjoner må nedskrives for å unngå for store lagernivåer. |
| Oppskriv | Systemet genererer handlingsmeldinger når produksjonsordrer, bestillinger og andre mottakstransaksjoner må oppskrives for å forhindre for lave lagernivåer. |
| Avledede handlinger | Handlingsmeldinger som opprettes for mottakstransaksjoner, overføres til eventuelle avledede krav, og de nødvendige handlingsmeldingene genereres for mottakstransaksjonene som oppfyller disse kravene. |

De følgende delene viser noen detaljerte scenarioer.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Oppskrivings- og nedskrivingshandlinger med produktstandardordreantall

På siden **Standard ordreinnstillinger** for en vare kan du definere et minste ordreantall, et maksimalt ordreantall og flere verdier. Systemet tar da hensyn til disse innstillingene når det foreslår handlinger, for å sikre at forslagene aldri vil føre til underlevering.

Du har for eksempel en vare med følgende innstillinger på siden **Standard ordreinnstillinger**:

- **Minste ordreantall:** *0*
- **Største ordreantall:** *90*
- **Flere:** *20*

Hvis det er behov for et antall på 60 av denne varen, vil hovedplanleggingen opprette et bestillingsforslag for et antall på 60. Hvis behovet økes med 30, vil hovedplanleggingen foreslå en økning på 40, fordi den vil følge regelen om multiplum av 20 og aldri forårsake underlevering.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Handlingsmeldinger for ordrer relatert til sikkerhetslager

Handlingsmeldinger for ordrer som leverer sikkerhetslager, vil aldri foreslå å redusere antallet under antallet som er nødvendig for sikkerhetslageret. Hvis det med andre ord finnes en ordre som forsyner sikkerhetslager og kundebehov, og behovet reduseres eller annulleres, vil hovedplanleggingen foreslå en reduksjon av den planlagte bestillingen med det reduserte behovet. Den vil imidlertid aldri foreslå en verdi som er lavere enn sikkerhetslageret som er nødvendig.

Systemet vil ikke foreslå utsettelseshandlinger for forsyning av sikkerhetslager, fordi det forutsettes at sikkerhetslageret må leveres på et bestemt tidspunkt og på den nødvendige datoen.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Fremskyndelses- og utsettelseshandlinger relatert til stykklister

Handlinger som er knyttet til komponenter i stykklister, må brukes før handlingene til de overordnede varene, fordi ytterligere ordrer som er knyttet til stykklister på høyere nivå, kan påvirkes. Deretter må du kjøre hovedplanleggingen på nytt for å beregne på nytt og foreslå riktige handlinger.

Du har for eksempel følgende situasjon:

- Sluttvaren *FG* av typen *produksjon* har en stykkliste som inkluderer råvaren *RM*.
- Dagens dato er 21. januar.
- En eksisterende, frigitt produksjonsordre for *FG* er planlagt til 25. januar.
- Hovedplanleggingen har opprettet et bestillingsforslag for den nødvendige råvaren *RM* for å støtte den eksisterende produksjonsordren. Denne ordren har behovsdatoen 25. januar.
- En ny salgsordre for *FG* opprettes i dag. Den har kravdatoen i dag (21. januar).
- 21. januar er lukket for levering i *RM*-kalenderen, men 22. januar er åpen.

Når hovedplanleggingen kjøres, genererer den fremskytelseshandlingsmeldinger som foreslår å flytte opp den tidligere planlagte produksjonen, slik at du kan innfri dagens ordre.

- For å møte det nye behovet foreslår den å flytte produksjonsordren for *FG* frem til 21. januar. (Den kommer med dette forslaget uten å vurdere den lukkede datoen for *RM*.)
- Ettersom *RM* fremdeles er nødvendig for produksjonsorden, foreslår den at bestillingsforslaget også flyttes opp. Denne gangen kontrollerer den imidlertid *RM*-kalenderen. Derfor foreslår den å flytte den planlagte bestillingen for *RM* til 22. januar (fordi 21. januar er lukket).

Som du kan se, vil den nødvendige råvaren *RM* nå ankomme for sent for den planlagte produksjonen av *FG*. Derfor må du først bruke fremskyndingshandlingen på den planlagte bestillingen for *RM* og deretter kjøre hovedplanleggingen på nytt. På dette tidspunktet vil hovedplanleggingen generere en ny handlingsmelding som foreslår å flytte produksjonsordren for *FG* til 22. januar.
