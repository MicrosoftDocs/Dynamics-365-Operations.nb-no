---
title: Klassifiser anleggsmidler på nytt
description: Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8935213c4629de408a48df5e54a2122324e1b3e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823938"
---
# <a name="reclassify-fixed-assets"></a>Klassifiser anleggsmidler på nytt

[!include [banner](../../includes/banner.md)]

Hvis du vil omklassifisere et anleggsmiddel, må du overføre det til den nye anleggsmiddelgruppen, eller gi det et nytt anleggsmiddelnummer i samme gruppe. 

Når et anleggsmiddel er omklassifisert:

* Alle tablåer for det eksisterende anleggsmiddelet opprettes for det nye anleggsmiddelet. All informasjon som ble definert for det originale anleggsmiddelet, kopieres til det nye anleggsmiddelet. Statusen til tablåene til det originale anleggsmiddelet er Lukket. 

* De nye tablåene til det nye anleggsmiddelet inneholder omklassifiseringsdatoen i **Anskaffelsesdato**-feltet. Datoen i feltet **Startdato for avskrivning** kopieres fra den opprinnelige anleggsmiddelinformasjonen. Hvis avskrivningen allerede har begynt, viser feltet **Datoen da avskrivningen sist ble kjørt** omklassifiseringsdatoen. 

* De eksisterende anleggsmiddeltransaksjonene for det originale anleggsmiddelet avlyses og genereres på nytt for det nye anleggsmiddelet.

Følg disse trinnene for å omklassifisere et anleggsmiddel:

1. Gå til **Anleggsmidler > Periodiske oppgaver > Omklassifisering**.
2. I feltet **Anleggsmiddelgruppe** velger du gruppen som skal omklassifiseres.
3. I feltet **Anleggsmiddelnummer** velger du anleggsmidlet som skal omklassifiseres.
4. Velg en gruppe som anleggsmidlet skal overføres til, i feltet **Ny anleggsmiddelgruppe**.
    * Hvis den nye anleggsmiddelgruppen er knyttet til en nummerserie, oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien til den nye anleggsmiddelgruppen. Ellers oppdateres feltet **Nytt anleggsmiddelnummer** med nummeret fra nummerserien som er definert på siden **Parametere for anleggsmidler**. Hvis en nummerserie ikke er definert på siden **Parametere for anleggsmidler**, angir du et nummer i feltet **Nytt anleggsmiddelnummer**.  
5. Angi en dato i feltet **Omklassifiseringsdato**.
6. Angi eller velg en verdi i feltet **Bilagsserie**.
7. Klikk **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]