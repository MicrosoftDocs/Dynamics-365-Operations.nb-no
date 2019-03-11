---
title: Klassifiser anleggsmidler på nytt
description: Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8e289e2c18fd28829fb4b749933ae1d84e0b631
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "323301"
---
# <a name="reclassify-fixed-assets"></a>Klassifiser anleggsmidler på nytt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe. 

Når et anleggsmiddel er omklassifisert:

• Alle verdimodellene til det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet. All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet. Statusen til verdimodellene til den originale anleggsmiddelet er Lukket. 

• De nye verdimodellene til det nye anleggsmiddelet inneholder omklassifiseringsdatoen i Anskaffelsesdato-feltet. Datoen i feltet Startdato for avskrivning kopieres fra den opprinnelige anleggsmiddelinformasjonen. Hvis avskrivningen allerede har begynt, viser feltet Datoen da avskrivningen sist ble kjørt omklassifiseringsdatoen. 

• De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.

1. Gå til Anleggsmidler > Periodiske oppgaver > Omklassifisering.
2. I feltet Anleggsmiddelgruppe velger du gruppen som skal omklassifiseres.
3. I feltet Anleggsmiddelnummer velger du anleggsmidlet som skal omklassifiseres.
4. Velg en gruppe som anleggsmidlet skal overføres til, i feltet Ny anleggsmiddelgruppe.
    * Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet Nytt anleggsmiddelnummer med nummeret fra nummerserien til den nye anleggsmiddelgruppen. Ellers oppdateres feltet Nytt anleggsmiddelnummer med nummeret fra nummerserien som er definert på siden Parametere for anleggsmidler. Hvis en nummerserie ikke er definert på siden Parametere for anleggsmidler, angir du et nummer i feltet Nytt anleggsmiddelnummer.  
5. Angi en dato i feltet Omklassifiseringsdato.
6. Angi eller velg en verdi i feltet Bilagsserie.
7. Klikk OK.

