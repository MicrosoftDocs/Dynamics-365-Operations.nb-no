---
title: Overføre prosjektbudsjetter ved regnskapsårets avslutning
description: Denne artikkelen gir informasjon om hvordan du overfører gjenstående budsjettbeløp til fremtidige år og oppretter budsjettregisterdetaljer.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172336"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Overføre prosjektbudsjetter ved regnskapsårets avslutning

[!include [banner](../includes/banner.md)]

Når du arbeider med et prosjekt med flere år, kan du ha gjenværende budsjett på slutten av regnskapsåret. Du kan ovefføre de gjenstående budsjettbeløpene til et fremtidig år, og opprette budsjettregisterdetaljer for beløpene i de tilknyttede finanskontoene. Før du overfører de gjenværende beløpene, kan du se over og analysere de gjenværende budsjettbeløpene.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Gå gjennom og analysere gjenstående budsjettbeløp

Fullfør fremgangsmåten nedenfor for å gå gjennom budsjettbeløpene for prosjekter ved årsavslutning, men ikke overføre beløpene.

1. Gå til **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**. 
2. På siden **Overføringsprosess for prosjektbudsjett**, i kategorien **Alternativer for årsavslutning**, kontrollerer du at **Overfør gjenværende prosjektbudsjettbeløp** ikke er aktivert.
3. I kategorien **Parametere**, i feltet **Budsjettår for prosjekt** velger du regnskapsåret som du vil vise de gjenstående budsjettbeløpene for. 
4. Velg regnskapsåret som du vil vise de gjenstående budsjettbeløpene for, i feltet **Føste regnskapsår**. 
5. I feltet **Fra prognosemodell** velger du **Gjenstående budsjett**. 
6. Hvis du vil ta med prosjekter som oppfyller de valgte kriteriene og ikke har noe gjenstående budsjett, velger du **Vis null gjenværende**.  
7. I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene, og velg deretter **Behandle**. 
8. Hvis du vil utforme en databasespørring som laster inn et bestemt sett med budsjetter i ruten, velger du **Hent valgte budsjetter**.

Hvis du vil ha mer informasjon om en bestemt linje i ruten, velger du linjen og velger deretter **Vis budsjettdetaljer** eller **Vis kontoer**.

## <a name="carry-forward-remaining-budget-amounts"></a>Overfør gjenværende budsjettbeløp 

Når du behandler gjenstående budsjettbeløp, kan du opprette transaksjoner i økonomimodulen for beløpene du overfører. Hvis du vil opprette økonomimodultransaksjoner, fullfører du trinnene i delen [Overføre budsjettbeløp og opprette økonomimodultransaksjoner](#carry-forward). 

> [!NOTE]
> Budsjettbeløp som overføres, sendes til prognosemodellen som er valgt som prognosemodell for overføring på siden **Prognosemodeller**.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Overføre budsjettbeløp og opprette økonomimodultransaksjoner

1.  Velg **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**. 
2. På siden **Overføringsprosess for prosjektbudsjett** velger du **Årsavslutning**, og deretter aktiverer du **Overfør gjenværende prosjektbudsjettbeløp** og **Opprett budsjettregisteroppføringer i økonomimodul**. 
3. Velg følgende i kategorien **Parametere** i **Prosjektparametere**-feltgruppen:

   - **Budsjettår for prosjekt**: Velg begynnelsen på regnskapsåret som du vil vise de gjenstående budsjettbeløpene for. 
   - **Resultat**: Opprett resultattransaksjoner i økonomimodulen. 
   -  **VIA**: Opprett VIA-transaksjoner i økonomimodulen.
   -  **Lønn**: Opprett lønnsfordelingstransaksjoner i økonomimodulen. 

5. Angi følgende informasjon i **Økonomimodul**-feltgruppen: 

   - Velg regnskapsåret du vil overføre de gjenstående budsjettbeløpene for prosjektene til, i feltet **Første regnskapsår**. Standardverdien er ett år etter verdien i feltet **Budsjettår for prosjekt**.
   -  Velg perioden du vil opprette budsjettregisterdetaljene for i økonomimodulen i, i **Overføringsperiode**-feltet. Dette er vanligvis den første perioden i det første regnskapsåret.

6. Angi følgende informasjon i **Kopier til/fra**-feltgruppen:

   - Velg prognosemodellen for prosjektbudsjett som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene, i feltet **Fra prognosemodell**. 
   - Velg finansbudsjettmodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre til økonomimodulen, i feltet **Finansbudsjettmodell**. 
   -  Velg **Overfør salgsvaluta** hvis du vil bruke prosjektets salgsvaluta for økonomimodultransaksjoner som opprettes når du overfører budsjettbeløpene for prosjektene. Når alternativet ikke er valgt, bruker transaksjonene regnskapsvalutaen. 
   -  Velg **Vis null gjenværende** hvis du vil ta med prosjekter som ikke har gjenstående budsjettbeløp, men som oppfyller de andre kriteriene du velger blant prosjektene som vises i den nedre ruten.

7. I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene. Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.
8. Velg alternativet på begynnelsen av linjen for hvert prosjekt du vil behandle.

    > [!TIP]
    > Hvis du vil merke alle eller de fleste av prosjektene, velger du avmerkingsboksen øverst til venstre. Hvis du vil utelate behandling av prosjekter, fjerner du merket for dette prosjektet.

9. Velg **Behandle** hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret og opprette budsjettregisterdetaljer i økonomimodulen.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Overføre budsjettbeløp uten å opprette økonomimodultransaksjoner

1. Gå til **Prosjektstyring og regnskap** > **Tidsbestemt** > **Budsjetter** > **Overfør budsjetter**.
2. På siden **Overføringsprosess for prosjektbudsjett**, i feltet **Alternativer for årsavslutning**, velger du **Overfør gjenværende prosjektbudsjettbeløp**.
3. I **Parametere**-gruppen, i feltet **Budsjettår for prosjekt** velger du regnskapsåret som du vil vise det gjenstående budsjettbeløpet for.
4. Angi følgende informasjon i **Kopier til/fra**-gruppen:

   - Velg prognosemodellen for prosjektbudsjett som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene, i feltet **Fra prognosemodell**. 
   - Hvis du vil ta med prosjekter som oppfyller de valgte kriteriene, men ikke har noe gjenstående budsjettbeløp, velger du **Vis null gjenværende**.
   - I gruppen **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med de valgte kriteriene. Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.

5. Velg alternativet på begynnelsen av linjen for hvert prosjekt du vil behandle. 
6. Velg **Behandle** hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til valgt regnskapsår.

