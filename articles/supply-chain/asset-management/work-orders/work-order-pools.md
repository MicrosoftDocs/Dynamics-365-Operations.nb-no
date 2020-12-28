---
title: Arbeidsordresamlinger
description: Dette emnet beskriver hvordan du arbeider med arbeidsordresamlinger i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e95a4fdfaf4817867f3d2df7774df6a27ee6599
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434703"
---
# <a name="work-order-pools"></a>Arbeidsordresamlinger

[!include [banner](../../includes/banner.md)]


Du kan bruke arbeidsordresamlinger til å gruppere arbeidsordrer som har noe til felles. Her er noen eksempler på ting du kan opprette arbeidsordresamlinger for:

- Arbeidslag, for eksempel vedlikeholdslag A eller vedlikeholdslag B  

- Fagkompetanse, for eksempel elektrikere og rørleggere  

- Fysiske lokasjoner  

- Tidsplaner, for eksempel uker eller andre perioder  

Du kan du plassere én arbeidsordre i flere arbeidsordresamlinger, etter behov.


## <a name="create-a-work-order-pool"></a>Opprette en arbeidsordresamling

På listesiden **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger** kan du få en oversikt over arbeidsordresamlingene og opprette nye samlinger.

1. Velg **Aktivastyring** > **Felles** > **Arbeidsordresamlinger** > **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**.

2. Velg **Ny**.

3. Angi en ID for arbeidsordresamlingen i feltet **Pulje**.

4. Angi et navn i **Navn**-feltet.

5. Sett alternativet **Aktiv** til **Ja** for å angi at arbeidsordresamlingen er aktiv.

6. Sett alternativet **Slett arbeidsordrerelasjoner** til **Ja** hvis arbeidsordrer automatisk skal fjernes fra arbeidsordresamlingen.

7. I feltet **Slett livssyklustilstand** velger du livssyklustilstanden for arbeidsordren. For eksempel kan livssyklustilstanden for arbeidsordre for å fullføre en arbeidsordre settes til å slette relasjoner til arbeidsordresamlinger automatisk.

    Du kan begynne å legge til arbeidsordrer i arbeideordresamlingen med én gang.

8. Velg **Legg til linje** på hurtigfanen **Arbeidsordrer**.

9. Velg en arbeidsordre i feltet **Arbeidsordre**. De tilknyttede feltene oppdateres automatisk.

10. Gjenta trinn 8 til og med 9 hvis du vil legge til flere arbeidsordrer.

11. Hvis arbeidsordrene du la til, skal utføres i en bestemt rekkefølge, kan du angi tallene **1**, **2**, **3** og så videre i feltet **Sorteringsrekkefølge** for å angi rekkefølgen.

12. Hvis du vil vise en liste over alle arbeidsordrene som er inkludert i arbeidsordren, går du til handlingsruten, kategorien **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Arbeidsordrer** for å åpne listesiden **Alle arbeidsordrer**.

13. Hvis du vil beregne og vise kapasitetsbelastningen for vedlikeholdsplanen, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer, går du til handlingsruten, kategorien **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Kapasitetsbelastning** for å åpne dialogboksen **Beregn kapasitetsbelastning**.

14. Hvis du vil beregne og vise prognoser for elementene (reservedeler og andre nødvendige varer) som er relatert til vedlikeholdsplanen, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer, går du til handlingsruten, kategorien **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Vareprognose** for å åpne dialogboksen **Beregn vareprognose**.

15. Hvis du vil vise en liste over innkjøpsrekvisisjoner som er relatert til arbeidsordrene i arbeidsordresamlingen, går du til handlingsruten, kategorien **Arbeidsordresamling**, gruppen **Innkjøp** og velger **Innkjøpsrekvisisjon for arbeidsordre** for å åpne listesiden **Innkjøpsrekvisisjon for arbeidsordre**.

16. Hvis du vil vise en liste over bestillinger som er relatert til arbeidsordrene i arbeidsordresamlingen, går du til handlingsruten, kategorien **Arbeidsordresamling**, gruppen **Innkjøp** og velger **Innkjøp for arbeidsordre** for å åpne listesiden **Innkjøp for arbeidsordre**.

>[!NOTE]
>Når en arbeidsordresamling ikke lenger er relevant for arbeidsplanleggingen, setter du alternativet **Aktiv** for denne samlingen til **Nei** i listevisningen på siden **Arbeidsordresamling**.

Hvis du vil slette alle arbeidsordrelinjer, setter du alternativet **Slett arbeidsordrerelasjoner** til **Ja**. Dette alternativet er nyttig hvis du for eksempel vil opprette et tomt utvalg som du kan bruke senere for andre arbeidsordrer. Når du er klar til å bruke arbeidsordresamlingen til å opprette nye arbeidsordrerelasjoner senere, må du huske å sette **Slett arbeidsordrerelasjoner** til **Nei**.

Illustrasjonen nedenfor viser et eksempel på listesiden **Arbeidsordresamling**.

![Figur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Legge til en arbeidsordre i en arbeidsordresamling

Som beskrevet i forrige del, kan du legge til arbeidsordrer i en arbeidsordresamling når du oppretter samlingen. Du kan også legge til arbeidsordrer i en arbeidsordresamling på listesiden **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

1. Velg arbeidsordren, og deretter går du til handlingsruten, kategorien **Arbeidsordre**, gruppen **Vedlikehold** og velger **Arbeidsordresamling**.

2. Velg arbeidsordren i listen, og klikk på **Arbeidsordresamling**.

3. I dialogboksen **Vedlikehold arbeidsordresamling** i feltet **Legg til/fjern** velger du **Legg til**.

4. Velg arbeidsordresamlingen i **Pulje**-feltet.

5. Velg **OK**.

6. Hvis du vil plassere arbeidsordren du la til, i en bestemt rekkefølge i arbeidsordreutvalget, går du til listesiden **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**, velger samlingen og deretter **Rediger**. Deretter, på siden **Arbeidsordresamling** i hurtigfanen **Arbeidsordrer**, bruker du feltet **Sorteringsrekkefølge** til å justere sorteringsrekkefølgen for arbeidsordrene som er inkludert i samlingen.

Hvis du vil fjerne en arbeidsordre fra en arbeidsordresamling, gjentar du disse trinnene, men velger **Fjern** i trinn 3.

