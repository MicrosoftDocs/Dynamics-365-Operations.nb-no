---
title: Opprett et fraktbrev
description: Dette emnet beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434827"
---
# <a name="create-a-bill-of-lading"></a>Opprett et fraktbrev

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.  

Et fraktbrev er et juridisk dokument mellom firmaet som leverer varene, og transportøren. Dokumentet følger med de leverte varene og fungerer som en kvittering for forsendelsen når varene blir levert til målet. Hvis du bruker lagerstyring, er det to måter å generere et fraktbrev på:

  -   Opprette rapporten manuelt på **Fraktbrev**-siden.
  -   Generere rapporten fra **arbeidsområdet for lastplanlegging**.

Hvis du genererer fraktbrevet fra **arbeidsområdet for lastplanlegging**, må laststatusen være **Sendt.** Hvis det er mer enn én forsendelse i lasten, opprettes et fraktbrev for hver forsendelse. Når et fraktbrev er opprettet, kan du kan gjøre endringer i det på **Fraktbrev**-siden.

## <a name="master-bill-of-lading"></a>Hovedfraktbrev
Hvis det er mer enn én forsendelse i lasten, kan du generere et hovedfraktbrev. Dette har samme oppsett og informasjon som et fraktbrev, men inneholder en oppsummering av alle forsendelsene. Hvis alternativet **Opprett et hovedfraktbrev når det er mer enn én forsendelse i en last** er satt til **Ja** på **Parametere for transportstyring**-siden, genereres automatisk et hovedfraktbrev hvis du oppretter et fraktbrev fra **Arbeidsområde for lastplanlegging**, og det er mer enn én forsendelse. Du kan også få en oversikt over fraktbrev ved å klikke **Relatert informasjon** &gt; **Fraktbrev**. Hvis du oppretter fraktbrev manuelt, kan du opprette et hovedfraktbrev på **Fraktbrev**-siden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]