---
title: Opprette forespørselstyper og poengkriterier for tilbudsforespørsler
description: Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf196711799b78d7f4106b6693127d7f356b1d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262219"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>Opprette forespørselstyper og poengkriterier for tilbudsforespørsler

[!include [banner](../../includes/banner.md)]

Denne veiledningen viser hvordan du oppretter en forespørsels og knytter den til en poengberegningsmetode. Den viser også hvordan du bruker forespørselstypen på en tilbudsforespørsel som deretter angir standard poengberegningsmetode. Disse oppgavene vil vanligvis utføres av en innkjøpssjef. Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data. Du må ha en poengberegningsmetode før du begynner.


## <a name="create-a-solicitation-type"></a>Opprette en forespørselstype
1. Gå til Innkjøp og leverandører > Oppsett > Tilbudsforespørsel > Forespørselstype.
2. Klikk på Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Skriv inn en verdi i feltet Beskrivelse.
5. I feltet Poengberegningsmetode velger du poengberegningsmetoden du vil bruke for denne forespørselstypen.
6. Klikk på Lagre.
7. Lukk siden.

## <a name="use-the-solicitation-type"></a>Bruke forespørselstypen
1. Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.
2. Klikk på Ny.
3. I Forespørselstype-feltet velger du forespørselstypen som du nettopp opprettet. 
    *   
4. Klikk på OK.
5. Klikk på Poengkriterier.
    * Poengkriteriene som vises, er de fra poengberegningsmetoden som du knyttet til forespørselstypen. Du kan velge å legge til eller slette kriteriene på denne siden. Du kan også legge til nye kriterier ved å kopiere dem fra andre poengberegningsmetoder.  
6. Klikk på Kopier kriterier.
7. Angi eller velg en verdi i Poengberegningsmetode-feltet.
8. Klikk på OK.
9. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]