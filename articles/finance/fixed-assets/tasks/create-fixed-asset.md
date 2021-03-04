---
title: Opprette et anleggsmiddel
description: Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for anleggsmidler.
author: moaamer
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
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 481bdb55b813dad5366f382ae35d8345b0e67d9f
ms.sourcegitcommit: a9efbd69f2670fd6ba0ad0babf304fc206d01249
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2020
ms.locfileid: "4446624"
---
# <a name="create-a-fixed-asset"></a>Opprette et anleggsmiddel

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter en ny anleggsmiddelpost fra listesiden for **anleggsmidler**.

Systemet tilordner anleggsmiddelnummeret basert på nummerserien som er tilordnet anleggsmiddelgruppen. Hvis du bruker anleggsmiddelmalen til å importere anleggsmidler via Microsoft Excel-tillegget, eller hvis du bruker en annen importjobb, oppretter systemet automatisk anleggsmiddelposter og øker anleggsmiddelnummeret.

Hvis du vil opprette en anleggsmiddelpost manuelt, følger du disse trinnene.

1. Gå til **Navigasjonsrute \> Moduler \> Anleggsmidler \> Anleggsmidler \> Anleggsmidler**.
2. I **handlingsruten** velger du **Ny**.
3. Angi eller velg en verdi i feltet **Anleggsmiddelgruppe**. **Nummer**-feltet hentes hvis du har aktivert funksjonaliteten **Automatisk nummerering av anleggsmidler** i **anleggsmiddelparameterne** og **anleggsmiddelgruppen**. Hvis ikke må du skrive inn et unikt nummer for å identifisere anleggsmidlet.
4. Angi en verdi i feltet **Navn**. Angi tilleggsinformasjonen som forretningen trenger for dette aktivaet.
5. Velg **Tablåer** i **handlingsruten**.
6. Angi en dato i feltet **Anskaffelsesdato**.
7. Angi et tall i feltet **Anskaffelsespris**.

    - Angi tilleggsinformasjonen som forretningen trenger for dette tablået.
    - Angi tilleggsinformasjonen som forretningen trenger for de gjenværende tablåene.

8. Lukk siden.

Du kan også importere anleggsmidler ved hjelp av Excel-tillegget eller ved å kjøre en importjobb fra arbeidsområdet **Dataadministrasjon**. Før du kjører importen, må du angi verdiene for de nødvendige feltene i malen.

Hvis du ikke har definert anleggsmiddelnummeret i malen for Excel-tillegget, eller i databehandling, oppretter systemet et anleggsmiddelnummer for hvert importerte anleggsmiddel, og øker automatisk nummerserien for hver. Hvis du imidlertid importerer anleggsmidler og definerer anleggsmiddelnumre i malen, vil **ikke** systemet automatisk øke nummerserien. I dette tilfellet kan det hende at en administrator må oppdatere nummerserien manuelt. Hvis du har definert anleggsmiddelnummeret i malen for Excel-tillegget, bruker systemet det definerte anleggsmiddelnummeret og øker nummerserien.

> [!NOTE]                                                                                                         
> Når avskrivningen er postert, låses feltene **Tatt i bruk** og **Startdato for avskrivning** på **Tablå**-siden. Begge eller ingen av feltene blir i tillegg oppdatert fra dataenheten.

> [!WARNING]
> Anleggsmiddelposten blir ikke slettet hvis transaksjonene ble postert i det tilknyttede tablået, eller hvis det nylig opprettede anleggsmidlet angis på en journallinje, men ikke posteres. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]