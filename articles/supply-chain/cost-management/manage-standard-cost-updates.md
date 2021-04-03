---
title: Administrere oppdateringer av standardkostnader
description: 'Oppdateringer av standard kostdata kan behandles på to ulike måter: enversjonsmåten eller toversjonsmåten.'
author: AndersGirke
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: fc4ae40e9740ce76e79b76c2bff2c690568abff2
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500604"
---
# <a name="manage-standard-cost-updates"></a>Administrere oppdateringer av standardkostnader

[!include [banner](../includes/banner.md)]

Oppdateringer av standard kostdata kan behandles på to ulike måter: enversjonsmåten eller toversjonsmåten.

Enversjonsmåten bruker én etterkalkuleringsversjon som inneholder alle kostnadsposter. Disse postene inneholder de opprinnelige kostnadene og alle kostnadsoppdateringer.

Toversjonsmåten bruker én versjon som inneholder poster for de opprinnelige kostnadene, og en ny versjon som inneholder poster for alle kostnadsoppdateringer. En viktig fordel med toversjonsmåten er den klare avmerkingen og sporingen av kostoppdateringer i en egen kostnadsberegningsversjon, uten at den opprinnelige kostnadsberegningsversjonen påvirkes. Toversjonsmåten kan brukes til å identifisere flere inkrementelle oppdateringer, hvor hver inkrementelle oppdatering har en egen etterkalkuleringsversjon som inneholder de inkrementelle kostprispostene.

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan enversjons- og toversjonsmåten kan brukes til å oppdatere standardkostnader i et produksjonsmiljø. For eksempel oppdateringer som gjenspeiler nye varer eller korrigeringer av feil. Anta at én enkelt etterkalkuleringsversjon representerer standardkostnadene for inneværende år. Identifikatoren for denne versjonen er 2020-STD. Versjon 2020-STD inneholder gjeldende aktive kostnader for alle varer. Den inneholder i tillegg alle rutingrelaterte kostpriskategorier og beregningsformler for indirekte kostnader som var kjent ved starten av 2020. 2020-STD er den opprinnelige etterkalkuleringsversjonen.

- **Enversjons tilnærming til oppdateringer av kostprisdata** − I enversjonsmåten inneholder den opprinnelige etterkalkuleringsversjonen 2020-STD alle kostprisposter. Kostnadsoppdateringer registreres i 2020-STD og settes til statusen Venter. De uavsluttede kostprisene kan legges inn manuelt for nye innkjøpte varer, eller de kan beregnes for en produsert vare for å gjenspeile korrigeringer. Når enversjonsmåten brukes, krever ikke stykklisteberegningene noe tilbakefallsdatakilde, fordi alle aktive kostpriser finnes i kostnadsberegningsversjonen. Nå de uavsluttede kostprisene blir aktivert, vil den opprinnelige etterkalkuleringsversjonen 2020-STD igjen inneholde alle gjeldende aktive kostpriser.
- **Toversjons tilnærming til oppdateringer av kostprisdata** − Toversjonsmåten krever en ekstra etterkalkuleringsversjon som bare inneholder kostnadsoppdateringene. Identifikatoren for denne versjonen er 2020-STD-ENDRINGER. Kostnadsoppdateringer registreres i 2020-STD-CHANGES og settes til statusen Venter. Med toversjonsmåten krever stykklisteberegninger av uavsluttede kostpriser for produserte varer tilbakefallsdatakilde. Dette skyldes at den ekstra etterkalkuleringsversjonen 2020-STD-ENDRINGER inneholder bare et delsett av kostnadsdata. Tilbakefallsprinsippet kan uttrykkes som de aktive kostprisene eller som etterkalkuleringsversjonen 2020-STD, fordi begge identifiserer kilden til kostnadsdataene når de ikke er inkludert i 2020-STD-ENDRINGER. Når de uavsluttede kostprisene blir aktivert, vil etterkalkuleringsversjonen 2020-STD-ENDRINGER inneholde gjeldende aktive kostpriser som gjenspeiler oppdateringene, mens den opprinnelige etterkalkuleringsversjonen 2020-STD ikke blir berørt. Når toversjonsmåten brukes, må det defineres sperrepolicyer for den opprinnelige kostnadsberegningsversjonen for å hindre oppdateringer. Det må defineres nøyaktig de samme blokkeringspolicyene for den andre kostnadsberegningsversjonen, med unntak av den angitte fra-datoen og den selektive bruken av sperrepolicyer for å tillate oppdateringer. Den angitte fra-datoen må oppdateres med hvert sett med endringer for å gjenspeile den planlagte aktiveringsdatoen.

Dette eksemplet brukte en ekstra kostnadsberegningsversjon til å håndtere oppdateringer gjennom hele 2020. Det er også mulig å bruke flere ekstra kostnadsberegningsversjoner, for eksempel en egen versjon for hvert sett med oppdateringer. Når mer enn én ekstra etterkalkulering brukes, må tilbakefallsprinsippet uttrykkes som de aktive kostprisene fordi de aktive kostprisene er spredt over flere etterkalkuleringsversjoner.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Finansdimensjoner for revalueringen av standardkostnad

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Hvis du aktiverer en ny standardpris, revalueres vanligvis lagerbeholdningsverdien av transaksjoner med revaluering av standardkostnad. Finansdimensjonene for varen blir vanligvis deretter postert i transaksjonene. Hvis du imidlertid vil kontrollere om og hvordan finansdimensjonene posteres, bruker du [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonen kalt *Alternativer for å angi standard finansdimensjoner for revaluering av standardkostnad for lager*. Etter at du har konfigurert denne funksjonen, kan du gå til **Kostnadsstyring > Oppsett av policy for lagerregnskap > Parametere** og angi en av følgende verdier i rullegardinlisten **Opprinnelse til finansdimensjon**:

- **Ingen** – Ingen finansdimensjoner er postert i transaksjonene for revaluering. Hvis du har en nødvendig finansdimensjon i kontostrukturen, kjøres revalueringsprosessen likevel, men den oppretter regnskapsoppføringer som ikke har noen finansdimensjoner. I dette tilfellet får brukerne en advarsel først, slik at de kan avbryte revalueringen om nødvendig.
- **Tabell** – Finansdimensjonene for varen posteres i transaksjonene for revaluering. Dette er standardinnstillingen og er i samsvar med den opprinnelige systemvirkemåten uten aktivering av funksjonen *Alternativer for å angi standard finansdimensjoner for revaluering av standardkostnad for lager*.
- **Postering** – Finansdimensjonene for transaksjonen som revalueres, posteres i transaksjonene for revaluering. Finansdimensjonene fra den opprinnelige transaksjonens lagerkonto brukes som standard både for lagerkontoen og revalueringskontoen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]