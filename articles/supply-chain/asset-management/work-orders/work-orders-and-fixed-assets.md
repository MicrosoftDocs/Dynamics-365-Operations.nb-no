---
title: Arbeidsordrer og anleggsmidler
description: Dette emnet forklarer arbeidsordrer og anleggsmidler i Aktivastyring.
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
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250835"
---
# <a name="work-orders-and-fixed-assets"></a>Arbeidsordrer og anleggsmidler


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


I Aktivastyring kan aktiva relateres til anleggsmidler, og du kan opprette arbeidsordrer for disse aktivaene. Hvis du bruker denne funksjonen, kan du få en fullstendig oversikt over anleggsmidler, tilknyttede investeringsprosjekter og kostnadene som er registrert på investeringsprosjektene, i **Prosjektstyring og regnskap**-modulen og **Anleggsmidler**-modulen.

>[!NOTE]
>**Anleggsmiddelnummer**-feltet fylles bare ut på arbeidsordrejobbprosjektet hvis typen Investering er valgt som prosjekttype i arbeidsordrejobbprosjektet.

![Figur 1](media/24-work-orders.png)

Følgende fremgangsmåte beskriver forholdet mellom aktiva, arbeidsordrer, arbeidsordrejobbprosjekter og anleggsmidler.

1. Du oppretter et aktivum som du knytter til et anleggsmiddel, som vist i figuren nedenfor.

![Figur 2](media/25-work-orders.png)

2. Når du definerer arbeidsordretyper (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper**), oppretter du en arbeidsordretype for behandling av investeringer. Se også [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).

![Figur 3](media/26-work-orders.png)

3. Når du definerer prosjektgrupper for arbeidsordrer (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett** > **Prosjektgruppe**-koblingen), oppretter du en relasjon mellom arbeidsordretypen som brukes for investeringer, og prosjektgruppen opprettet for investeringer i **Prosjektstyring og regnskap**-modulen (**Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Prosjektgrupper**).

![Figur 4](media/27-work-orders.png)

4. Når du oppretter en arbeidsordre som er knyttet til et anleggsmiddelobjekt, velger du arbeidsordretypen som brukes til å behandle investeringer, for eksempel Investering.

5. Når arbeidsordren opprettes, vises den tilknyttede arbeidsordretypen i **Alle arbeidsordrer**.

![Figur 5](media/28-work-orders.png)

6. Når arbeidsordren opprettes, opprettes prosjektet som er knyttet til arbeidsordren, i **Prosjektstyring og regnskap** > **Alle prosjekter**. Du kan vise prosjektrelatert informasjon ved å klikke på koblingen **Prosjekt-ID** i arbeidsordren (i **Aktivastyring** åpner du arbeidsordren i detaljvisningen > hurtigfanen **Linjedetaljer** > kategorien **Generelt** > feltet **Prosjekt-ID**).

![Figur 6](media/29-work-orders.png)

7. I **Anleggsmidler** kan du se en oversikt over prosjektene som er knyttet til et anleggsmiddel (**Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler**> klikk på anleggsmidlet i feltet **Anleggsmiddelnummer** > vis innholdet i **Relatert informasjon**-ruten > delen **Tilknyttede prosjekter**).

