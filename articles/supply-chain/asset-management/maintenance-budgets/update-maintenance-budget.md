---
title: Oppdatere vedlikeholdsbudsjetter
description: Dette emnet forklarer hvordan du oppdaterer et vedlikeholdsbudsjett i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87c054cb96d56e40e35ee44142396f59d61395263ff41232423f6c7911478b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724946"
---
# <a name="update-maintenance-budgets"></a>Oppdatere vedlikeholdsbudsjetter

[!include [banner](../../includes/banner.md)]

 

Siden **Vedlikeholdsbudsjettlinjer** viser alle budsjettlinjene som er opprettet for budsjettet som er valgt på siden **Vedlikeholdsbudsjetter**. (Hvis du vil ha mer informasjon, se [Opprette vedlikeholdsbudsjetter](create-maintenance-budget.md).) Du kan beregne på nytt og justere linjer for vedlikeholdsbudsjett til vedlikeholdsbudsjettet er godkjent. Når budsjettperioden er passert, og kostnadene er postert i Aktivastyring, kan du også oppdatere budsjettlinjene med faktiske kostnader.

## <a name="recalculate-a-maintenance-budget"></a>Beregne et vedlikeholdsbudsjett på nytt

Du kan beregne et vedlikeholdsbudsjett på nytt på siden **Vedlikeholdsbudsjettlinjer**. Når du beregner et vedlikeholdsbudsjett på nytt, slettes de eksisterende budsjettlinjene, og det gjøres en ny beregning.

1. Velg **Beregn på nytt** på siden **Vedlikeholdsbudsjettlinjer**.
2. I dialogboksen **Beregn budsjett på nytt** utfører du de nødvendige endringene for den nye beregningen, og deretter velger du **OK**.

Nye budsjettlinjer opprettes i henhold til verdiene du angir.

## <a name="adjust-budget-lines"></a>Justere budsjettlinjer

I stedet for å beregne hele vedlikeholdsbudsjettet på nytt, kan du justere valgte linjer som er knyttet til budsjettkostnader.

1. På siden **Vedlikeholdsbudsjettlinjer** velger du linjene du vil oppdatere budsjettkostnadene for.
2. Velg **Juster**.
3. Hvis du vil legge til et beløp på de valgte linjene, merker du av for **Legg til kostnad**, og deretter angir du verdien i **Legg til verdi**-feltet.
4. Hvis du vil multiplisere budsjettkostnaden på de valgte budsjettlinjene med en faktor, merker du av for **Multipliser kostnad** og angir faktoren i feltet **Multipliser verdi**.

    Hvis du for eksempel angir **1,2** i feltet **Multipliser verdi**, øker du budsjettkostnaden på de valgte linjene med 20 prosent. Hvis du angir **0,7**, reduserer du budsjettkostnaden på de valgte linjene med 30 prosent.

5. Velg **OK**.

De valgte budsjettlinjene oppdateres i henhold til verdiene du angir i trinn 3 eller 4.

## <a name="update-actual-costs"></a>Oppdatere faktiske kostnader

Når datoene på budsjettlinjene er passert, og faktiske kostnader er postert i Aktivastyring, kan du oppdatere de faktiske kostnadene i vedlikeholdsbudsjettet.

1. Velg **Oppdater kostnad** på siden **Vedlikeholdsbudsjettlinjer**.
2. I dialogboksen **Beregn faktisk kostnad** velger du **OK**.

**Faktisk kostnad**-feltene på budsjettlinjene oppdateres hvis faktiske kostnader er postert. Nye budsjettlinjer kan genereres hvis det er opprettet nye aktivatyper etter at du opprettet budsjettet, og hvis disse aktivatypene er brukt på aktiva som arbeidsordrer er opprettet for og tilknyttede kostnader er postert for. Nye budsjettlinjer viser bare faktiske kostnader fordi det ikke er beregnet noen budsjettkostnader for dem.

> [!NOTE]
> Hvis du vil vise en oversikt over faktiske kostnader delt inn i forebyggende, korrigerende og investeringskostnader, kan du utføre en beregning for den samme perioden på siden **Kostnadskontroll for aktivum**. 

## <a name="manually-add-budget-lines"></a>Legge til budsjettlinjer manuelt

På siden **Vedlikeholdsbudsjettlinjer** kan du manuelt legge til en ny budsjettlinje ved å velge **Ny** og deretter foreta valg på linjen. Her er noen eksempler på situasjoner der denne fremgangsmåten kan være nyttig:

- Du vet at reparasjon av enkelte aktiva er for øyeblikket i planleggingsfasen, men tilknyttede jobber er ennå ikke opprettet i Aktivastyring. Du vil imidlertid at budsjettkostnader for disse jobbene skal være med i vedlikeholdsbudsjettet.
- Det er opprettet nye aktiva eller aktivatyper siden du opprettet vedlikeholdsbudsjettet, men vedlikeholdsplaner er ennå ikke definert for disse aktivaene eller aktivatypene. Du vil imidlertid at budsjettkostnader for disse aktivatypene skal være med i vedlikeholdsbudsjettet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]