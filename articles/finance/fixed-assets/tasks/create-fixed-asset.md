---
title: Opprette et anleggsmiddel
description: Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for anleggsmidler.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000249"
---
# <a name="create-a-fixed-asset"></a>Opprette et anleggsmiddel

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for **anleggsmidler**.

Systemet tilordner anleggsmiddelnummeret basert på nummerserien som er tilordnet anleggsmiddelgruppen. Hvis du bruker anleggsmiddelmalen til å importere anleggsmidler via Microsoft Excel-tillegget, eller hvis du bruker en annen importjobb, oppretter systemet automatisk anleggsmiddelposter og øker anleggsmiddelnummeret.

Hvis du vil opprette en anleggsmiddelpost manuelt, følger du disse trinnene.

1. Gå til **Navigasjonsrute \> Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
2. I **handlingsruten** velger du **Ny**.
3. Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**. **Nummer** -feltet hentes hvis du har aktivert funksjonaliteten **Automatisk nummerering av anleggsmidler** i **anleggsmiddelparameterne** og **anleggsmiddelgruppen**. Hvis ikke må du skrive inn et unikt nummer for å identifisere anleggsmidlet.
4. Angi en verdi i feltet **Navn**. Angi tilleggsinformasjonen som forretningen trenger for dette aktivaet.
5. Velg **Tablåer** i **handlingsruten**.
6. Angi en dato i feltet **Anskaffelsesdato**.
7. Angi et tall i feltet **Anskaffelsespris**.

    - Angi tilleggsinformasjonen som forretningen trenger for dette tablået.
    - Angi tilleggsinformasjonen som forretningen trenger for de gjenværende tablåene.

8. Lukk siden.

Du kan også importere anleggsmidler ved hjelp av Excel-tillegget eller ved å kjøre en importjobb fra arbeidsområdet **Dataadministrasjon**. Før du kjører importen, må du angi verdiene for de nødvendige feltene i malen.

Hvis du ikke har definert anleggsmiddelnummeret i malen for Excel-tillegget, eller i databehandling, oppretter systemet et anleggsmiddelnummer for hvert importerte anleggsmiddel, og øker automatisk nummerserien for hver. Hvis du imidlertid importerer anleggsmidler og definerer anleggsmiddelnumre i malen, vil **ikke** systemet automatisk øke nummerserien. I dette tilfellet kan det hende at en administrator må oppdatere nummerserien manuelt. Hvis du har definert anleggsmiddelnummeret i malen for Excel-tillegget, bruker systemet det definerte anleggsmiddelnummeret og øker nummerserien.
