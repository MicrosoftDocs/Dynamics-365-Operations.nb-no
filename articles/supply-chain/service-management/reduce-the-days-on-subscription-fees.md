---
title: Redusere dagene på abonnementsgebyr
description: Hvis du vil redusere antall dager for en eksisterende abonnementsavgift, kan du opprette en ny transaksjon der du fjerner tidsperioden som ikke lenger skal være del av abonnementsavgiftsintervallet.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370722d5c2f66e316d7c37f711cdd086bc53f6a8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014829"
---
# <a name="reduce-the-days-on-subscription-fees"></a>Redusere dagene på abonnementsgebyr 

[!include [banner](../includes/banner.md)]


Hvis du vil redusere antall dager for en eksisterende abonnementsavgift, kan du opprette en ny transaksjon der du fjerner tidsperioden som ikke lenger skal være del av abonnementsavgiftsintervallet.

## <a name="reduce-the-days-on-a-subscription-fee"></a>Redusere dager på en abonnementsavgift

1.  Klikk på **Servicestyring** \> **Serviceabonnementer** \> **Alle serviceabonnementer**. Velg serviceabonnementet, og klikk **Abonnementsavgifter** i handlingsruten.

2.  I feltet **Abonnementstype** velger du **Reduksjonsdager**.

3.  Bruk feltet **Fra dato** og feltet **Til dato** til å definere datointervallet for abonnementsavgiften du vil fjerne fra abonnementsavgiftsperioden, og klikk deretter **OK**.

Hvis du vil vise transaksjonene som ble opprettet, i skjemaet **Abonnement**, klikker du **Gebyrtransaksjoner**.

## <a name="example"></a>Eksempel

Hvis en periode for abonnementstransaksjon går fra 1. januar til 31. januar, og du vil redusere perioden med 10 dager, oppretter du en ny transaksjon der perioden er 1. januar til 10. januar. (Reduksjonsperioden kan også være 5. januar til 15. januar eller en vilkårlig periode på ti dager.)

I tillegg hvis **Fra dato** i reduksjonsperioden er 21. januar (31 minus 10), kan du angi **Til dato** til en hvilken som helst dato etter 31. januar, og det fjernes automatisk 10 dager fra avgiftstransaksjonsperioden.

## <a name="see-also"></a>Se også

[Reduksjonsdager – eksempel](reduction-days-example.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]