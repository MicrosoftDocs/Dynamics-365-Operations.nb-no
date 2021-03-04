---
title: Arbeidsordrer og anleggsmidler
description: Dette emnet forklarer arbeidsordrer og anleggsmidler i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434617"
---
# <a name="work-orders-and-fixed-assets"></a>Arbeidsordrer og anleggsmidler

[!include [banner](../../includes/banner.md)]


I Aktivastyring kan aktiva relateres til anleggsmidler, og du kan opprette arbeidsordrer for disse aktivaene. Hvis du bruker denne funksjonen, kan du få en fullstendig oversikt over anleggsmidler, tilknyttede investeringsprosjekter og kostnadene som er registrert på investeringsprosjektene, i **Prosjektstyring og regnskap** og **Anleggsmidler**-modulene i Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Feltet **Anleggsmidlets nummer** fylles bare ut på arbeidsordrejobbprosjektet hvis **Investering** er valgt som prosjekttype i arbeidsordrejobbprosjektet.

Illustrasjonen nedenfor viser forholdet mellom et investeringsprosjekt i modulen **Prosjektstyring og regnskap** og et arbeidsordrejobbprosjekt.

![Figur 1](media/24-work-orders.png)

Følgende fremgangsmåte beskriver forholdet mellom aktiva, arbeidsordrer, arbeidsordrejobbprosjekter og anleggsmidler.

1. Du oppretter et aktivum som du knytter til et anleggsmiddel.

![Figur 2](media/25-work-orders.png)

2. Når du definerer arbeidsordretyper på siden **Arbeidsordretyper** (**Aktivabehandling** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper**), oppretter du en arbeidsordretype for behandling av investeringer. Se også [Arbeidsordretyper](../setup-for-work-orders/work-order-types.md).

![Figur 3](media/26-work-orders.png)

3. Når du definerer prosjektgrupper for arbeidsordrer i kategorien **Prosjektgruppe** på siden **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**), oppretter du en relasjon mellom arbeidsordretypen som brukes for investeringer, og prosjektgruppen som ble opprettet for investeringer på siden **Prosjektgrupper** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Oppsett** > **Postering** > **Prosjektgrupper**).

![Figur 4](media/27-work-orders.png)

4. Når du oppretter en arbeidsordre som er relatert til et anleggsmiddel, velger du arbeidsordretypen som brukes til å behandle investeringer, for eksempel **Investering**.

5. Når arbeidsordren opprettes, vises den tilknyttede arbeidsordretypen på siden **Alle arbeidsordrer**.

![Figur 5](media/28-work-orders.png)

6. Når arbeidsordren opprettes, opprettes prosjektet som er knyttet til arbeidsordren, på siden **Alle prosjekter** i modulen **Prosjektstyring og regnskap** (**Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**). Hvis du vil vise prosjektrelatert informasjon, velger du koblingen i feltet **Prosjekt-ID** i kategorien **Generelt** i hurtigfanen **Linjedetaljer** i detaljvisningen på siden **Alle arbeidsordrer** i modulen **Aktivabehandling** (**Aktivabehandling** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer**).

![Figur 6](media/29-work-orders.png)

7. Hvis du vil se en oversikt over prosjektene som er knyttet til et anleggsmiddel, velger du **Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler** og deretter, i feltet **Anleggsmidlets nummer**, velger du koblingen til anleggsmidlet for å åpne detaljvisningen. Utvid ruten **Beslektet informasjon** til høyre på siden, og velg hurtigfanen **Tilknyttede prosjekter**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]