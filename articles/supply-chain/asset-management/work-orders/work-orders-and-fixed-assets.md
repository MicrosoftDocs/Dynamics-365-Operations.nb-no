---
title: Arbeidsordrer og anleggsmidler
description: Denne artikkelen forklarer arbeidsordrer og anleggsmidler i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ed83450592d85205743c9ff1aefd0e66e5d2b90c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111996"
---
# <a name="work-orders-and-fixed-assets"></a>Arbeidsordrer og anleggsmidler

[!include [banner](../../includes/banner.md)]


I Aktivastyring kan aktiva relateres til anleggsmidler, og du kan opprette arbeidsordrer for disse aktivaene. Hvis du bruker denne funksjonen, kan du få en fullstendig oversikt over anleggsmidler, tilknyttede investeringsprosjekter og kostnadene som er registrert på investeringsprosjektene, i modulene **Prosjektstyring og regnskap** og **Anleggsmidler** i økonomi- og driftsappene.

>[!NOTE]
>Feltet **Anleggsmidlets nummer** fylles bare ut på arbeidsordrejobbprosjektet hvis **Investering** er valgt som prosjekttype i arbeidsordrejobbprosjektet.

Illustrasjonen nedenfor viser forholdet mellom et investeringsprosjekt i modulen **Prosjektstyring og regnskap** og et arbeidsordrejobbprosjekt.

![Figur 1.](media/24-work-orders.png)

Følgende fremgangsmåte beskriver forholdet mellom aktiva, arbeidsordrer, arbeidsordrejobbprosjekter og anleggsmidler.

1. Du oppretter et aktivum som du knytter til et anleggsmiddel.

![Figur 2.](media/25-work-orders.png)

2. Når du definerer arbeidsordretyper på siden **Arbeidsordretyper** (**Aktivabehandling** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper**), oppretter du en arbeidsordretype for behandling av investeringer. Se også [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).

![Figur 3.](media/26-work-orders.png)

3. Når du definerer prosjektgrupper for arbeidsordrer i fanen **Prosjektgruppe** på siden **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**), oppretter du en relasjon mellom arbeidsordretypen som brukes for investeringer, og prosjektgruppen som ble opprettet for investeringer på siden **Prosjektgrupper** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Prosjektgrupper**).

![Figur 4.](media/27-work-orders.png)

4. Når du oppretter en arbeidsordre som er relatert til et anleggsmiddel, velger du arbeidsordretypen som brukes til å behandle investeringer, for eksempel **Investering**.

5. Når arbeidsordren opprettes, vises den tilknyttede arbeidsordretypen på siden **Alle arbeidsordrer**.

![Figur 5.](media/28-work-orders.png)

6. Når arbeidsordren opprettes, opprettes prosjektet som er knyttet til arbeidsordren, på siden **Alle prosjekter** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**). Hvis du vil vise prosjektrelatert informasjon, velger du koblingen i feltet **Prosjekt-ID** i fanen **Generelt** i hurtigfanen **Linjedetaljer** i detaljvisningen på siden **Alle arbeidsordrer** i modulen **Aktivabehandling** (**Aktivabehandling** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer**).

![Figur 6.](media/29-work-orders.png)

7. Hvis du vil se en oversikt over prosjektene som er knyttet til et anleggsmiddel, velger du **Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler** og deretter, i feltet **Anleggsmidlets nummer**, velger du koblingen til anleggsmidlet for å åpne detaljvisningen. Utvid ruten **Beslektet informasjon** til høyre på siden, og velg hurtigfanen **Tilknyttede prosjekter**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
