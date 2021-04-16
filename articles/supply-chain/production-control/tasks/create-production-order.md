---
title: Opprette en produksjonsordre
description: Denne fremgangsmåten viser hvordan du oppretter en produksjonsordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e9358811f35e0417099ae65b0206e32a1455f84
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828976"
---
# <a name="create-a-production-order"></a>Opprette en produksjonsordre

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en produksjonsordre. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. Dette er den første fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.


## <a name="create-a-production-order"></a>Opprette en produksjonsordre
1. Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.
2. Klikk på Ny produksjonsordre.
3. Skriv inn D0001 i feltet Varenummer.
4. Angi en leveringsdato i Levering-feltet.
    * Leveringsdatoen angir når produksjonsordren skal avsluttes for å levere i tide. Denne datoen kan brukes i planleggingsprosessen. Du kan for eksempel planlegge ordren baklengs fra leveringsdatoen.  
5. Sett verdien for Antall til 20.
    * Merk: Feltet for stykklistenummer viser automatisk nummeret til eventuelle aktive stykklister for den gjeldende varen, men du kan endre stykklisten for produksjonsordren ved å velge en aktiv stykkliste fra listen over godkjente stykklisteversjoner.    Feltet for rutenummer viser automatisk nummeret til eventuelle aktive ruter for den gjeldende varen, men du kan endre ruten for produksjonsordren ved å velge en aktiv rute fra listen over godkjente ruteversjoner.  
6. Klikk på Opprett.

## <a name="validate-the-production-order"></a>Validere produksjonsordren
1. Klikk på koblingen i den valgte raden i listen.
    * Klikk på koblingen for produksjonsordrenummeret du nettopp opprettet. Dette åpner siden med detaljer for ordren.  
2. Klikk på Rediger.
3. Angi en leveringsdato i Levering-feltet.
    * Du kan for eksempel endre leveringsdatoen for produksjonsordren.  
4. Klikk på Lagre.
5. Lukk siden.

## <a name="update-the-bom"></a>Oppdatere stykklisten
1. Klikk på Produksjonsordre i handlingsruten.
2. Klikk på Stykkliste.
    * Åpne stykklistesiden for å validere stykklistedataene som ble kopiert fra standarddataene da produksjonsordren ble opprettet. I denne prosedyren må du oppdatere antallet for en stykkliste.  
3. Klikk på Rediger.
4. Angi et tall i feltet Antall.
    * Endring av antallet på stykklistelinjen påvirker kostnadsestimatet av materialforbruk for produksjonsordren.  
5. Klikk på Lagre.
6. Lukk siden.

## <a name="update-the-production-route"></a>Oppdatere produksjonsruten
1. Klikk på Produksjonsordre i handlingsruten.
2. Klikk på Rute.
    * Åpne rutesiden for å validere dataene i produksjonsruten som ble kopiert fra standarddataene da produksjonsordren ble opprettet. I denne prosedyren må du oppdatere antallet for en av operasjonene i produksjonsruten.  
3. Finn og velg ønsket post i listen.
4. Klikk på Rediger.
5. I feltet Prosessantall angir du et nummer.
    * Endring av behandlingstiden påvirker det estimerte ruteforbruket og kostnadene for produksjonsordren.  
6. Klikk på Lagre.
7. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]