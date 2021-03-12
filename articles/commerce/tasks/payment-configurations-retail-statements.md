---
title: " Betalingskonfigurasjoner for detaljhandelsutdrag"
description: Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for handel, som påvirker hvordan utdrag opprettes og posteres.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982321"
---
# <a name="payment-configurations-for-retail-statements"></a> Betalingskonfigurasjoner for detaljhandelsutdrag

[!include [banner](../includes/banner.md)]

Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for handel, som påvirker hvordan utdrag opprettes og posteres.

Denne registreringen bruker demonstrasjonsfirmaet USRT.

1. Gå til Retail og Commerce > Kanaler > Butikker > Alle butikker.
2. Finn og velg ønsket post i listen.
3. Klikk koblingen i den valgte raden i listen.
4. Klikk Oppsett i handlingsruten.
5. Klikk Betalingsmåter.
6. Vis eller skjul delen Postering.
7. Klikk Rediger.
    * Velg om beløpene som er mottatt for denne betalingsmåten, skal posteres til en finanskonto eller bankkonto.  
    * Velg kontoen som beløp som er mottatt for denne betalingsmåten, skal posteres til.  
    * Velg en konto for postering av mulige forskjeller mellom det totale transaksjonsbeløpet som er mottatt, og beløpet som er telt opp for denne betalingsmåten.  
    * I dette feltet kan du angi et beløp for å kontrollere når differansebeløpet skal posteres til en annen differansekonto. Du kan bruke dette til å spore store forskjeller.  
    * Velg en konto for postering av mulige forskjeller mellom det totale transaksjonsbeløpet som er mottatt, og beløpet som er telt opp, når det overskrider verdien som er definert i feltet Største differansebeløp.  
    * Velg Ja for å postere bankdeponeringsbeløp til en separat konto.  
    * I dette feltet kan du velge om bankdeponeringsbeløp skal posteres til en finanskonto eller en bankkonto.  
    * Velg kontoen bankdeponeringsbeløp skal posteres på.  
    * Velg banktransaksjonstypen som skal brukes ved postering av bankdeponeringsbeløp til bankkontoen.  
    * Velg Ja for å postere safedeponeringsbeløp på en separat konto.  
    * Velg om safedeponeringsbeløp skal posteres til finanskontoen eller bankkontoen.  
    * Velg kontoen safedeponeringsbeløp skal posteres på.  
8. Klikk Lagre.

