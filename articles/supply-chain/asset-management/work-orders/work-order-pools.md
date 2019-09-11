---
title: Arbeidsordresamlinger
description: Dette emnet beskriver hvordan du arbeider med arbeidsordresamlinger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875820"
---
# <a name="work-order-pools"></a>Arbeidsordresamlinger


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan bruke arbeidsordresamlinger til å gruppere arbeidsordrer som har noe til felles. Du kan for eksempel opprette arbeidsordresamlinger for

- arbeidslag, for eksempel vedlikeholdslag A, vedlikeholdslag B  

- fagkompetanse, for eksempel elektrikere og rørleggere  

- fysiske lokasjoner  

- tidsplaner, for eksempel uker eller andre perioder  


Hvis det er nødvendig, kan én arbeidsordre plasseres i mange arbeidsordresamlinger.


## <a name="create-work-order-pool"></a>Opprette arbeidsordresamling

I **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger** kan du få en oversikt over arbeidsordresamlingene og opprette nye samlinger.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordresamlinger** > **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**.

2. Klikk på **Ny**.

3. Sett inn en ID for arbeidsordresamling i **Samling**-feltet og et navn i **Navn**-feltet.

4. Velg Ja på **Aktiv**-veksleknappen for å angi at arbeidsordresamlingen er aktiv.

5. Velg Ja på veksleknappen **Slett arbeidsordrerelasjoner** hvis du vil at arbeidsordrer skal fjernes automatisk fra arbeidsordresamlingen.

6. I feltet **Slett livssyklustilstand** velger du livssyklustilstanden for arbeidsordren. For eksempel kan livssyklustilstanden for arbeidsordre for å fullføre en arbeidsordre settes til å slette relasjoner til arbeidsordresamlinger automatisk.

7. Du kan begynne å legge til arbeidsordrer i arbeideordresamlingen med én gang. Klikk på **Legg til linje** på hurtigfanen **Arbeidsordrer**.

8. Velg en arbeidsordre i feltet **Arbeidsordre**. De tilknyttede feltene oppdateres automatisk.

9. Gjenta trinn 7-8 hvis du vil legge til flere arbeidsordrer.

10. I feltet **Sorteringsrekkefølge** kan du angi om arbeidsordrene skal utføres i en bestemt rekkefølge. Sett inn tallene 1, 2, 3 og så videre for å angi en bestemt rekkefølge for de valgte arbeidsordrene.

11. Klikk på **Arbeidsordrer**-knappen for å vise en liste over alle arbeidsordrene som er inkludert i arbeidsordresamlingen.

12. Klikk på knappen **Kapasitetsbelastning** for å åpne **Kapasitetsbelastning** for å beregne og vise kapasitetsbelastning for vedlikeholdsplan, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer.

13. Klikk på knappen **Vareprognose** for å åpne **Vareprognose** for å beregne og vise prognoser for varer (reservedeler og andre nødvendige varer) knyttet til vedlikeholdsplan, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer.

14. Klikk på knappen **Innkjøpsrekvisisjon for arbeidsordre** for å åpne listen **Innkjøpsrekvisisjon for arbeidsordre** for å vise en liste over innkjøpsrekvisisjoner knyttet til arbeidsordrene i arbeidsordresamlingen.

15. Klikk på knappen **Arbeidsordrekjøp** for å åpne listen **Arbeidsordrekjøp** for å vise en liste over bestillinger knyttet til arbeidsordrene i arbeidsordresamlingen.

>[!NOTE]
>Når en arbeidsordresamling ikke lenger er relevant for arbeidsplanleggingen, setter du **Aktiv**-avmerkingsboksen for denne samlingen til Nei i listevisningen **Arbeidsordresamling**.

Merk av for **Slett arbeidsordrerelasjoner** hvis du vil slette alle arbeidsordrelinjene, for eksempel for å opprette en tom samling som du kan bruke senere i andre arbeidsordrer. Husk å fjerne merket for **Slett arbeidsordrerelasjoner** hvis du vil bruke arbeidsordresamlingen til å opprette nye arbeidsordrerelasjoner senere.


![Figur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Legge til arbeidsordre i en arbeidsordresamling

Som beskrevet i delen ovenfor, kan du legge til arbeidsordrer i en arbeidsordresamling når du oppretter samlingen. Du kan også legge til en arbeidsordre i en arbeidsordresamling fra **Alle arbeidsordrer**-listen.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren i listen, og klikk på **Arbeidsordresamling**.

3. Velg Legg til i **Legg til / fjern**-feltet.

4. Velg arbeidsordresamlingen i **Samling**-feltet.

5. Klikk **OK**.

6. Når du har lagt til en arbeidsordre i en arbeidsordresamling, og du vil plassere arbeidsordren i en bestemt rekkefølge i puljen: Åpne en av listesidene for arbeidsordresamlinger, velg samlingen, klikk på **Rediger**, og juster sorteringsrekkefølgen for arbeidsordrene som er inkludert i samlingen, i **Arbeidsordresamling**-skjemaet > **Arbeidsordrer**-hurtigfanen > **Sorteringsrekkefølge**-feltet.

Hvis du vil fjerne den valgte arbeidsordren fra en arbeidsordresamling, velger du Fjern i trinn 3.

