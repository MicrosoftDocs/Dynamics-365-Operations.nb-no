---
title: Opprett et fraktbrev
description: Denne artikkelen beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e84fee13dcff574f1700ba2b8f577f4c401cbc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885790"
---
# <a name="create-a-bill-of-lading"></a>Opprett et fraktbrev

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter et fraktbrev ved hjelp av lagerstyringsprosesser.  

Et fraktbrev er et juridisk dokument mellom firmaet som leverer varene, og transportøren. Dokumentet følger med de leverte varene og fungerer som en kvittering for forsendelsen når varene blir levert til målet. Hvis du bruker lagerstyring, er det to måter å generere et fraktbrev på:

  -   Opprette rapporten manuelt på **Fraktbrev**-siden.
  -   Generere rapporten fra **arbeidsområdet for lastplanlegging**.

Hvis du genererer fraktbrevet fra **arbeidsområdet for lastplanlegging**, må laststatusen være **Sendt.** Hvis det er mer enn én forsendelse i lasten, opprettes et fraktbrev for hver forsendelse. Når et fraktbrev er opprettet, kan du kan gjøre endringer i det på **Fraktbrev**-siden.

## <a name="master-bill-of-lading"></a>Hovedfraktbrev
Hvis det er mer enn én forsendelse i lasten, kan du generere et hovedfraktbrev. Dette har samme oppsett og informasjon som et fraktbrev, men inneholder en oppsummering av alle forsendelsene. Hvis alternativet **Opprett et hovedfraktbrev når det er mer enn én forsendelse i en last** er satt til **Ja** på **Parametere for transportstyring**-siden, genereres automatisk et hovedfraktbrev hvis du oppretter et fraktbrev fra **Arbeidsområde for lastplanlegging**, og det er mer enn én forsendelse. Du kan også få en oversikt over fraktbrev ved å klikke **Relatert informasjon** &gt; **Fraktbrev**. Hvis du oppretter fraktbrev manuelt, kan du opprette et hovedfraktbrev på **Fraktbrev**-siden.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]