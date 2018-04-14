--- 
title: " Betalingskonfigurasjoner for detaljhandelsutdrag"
description: "Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for detaljhandel, som påvirker hvordan detaljhandelsutdrag opprettes og posteres."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0ffd6dc5fff6d27ec3cfdcd68c53b2299c4100b9
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---
# <a name="payment-configurations-for-retail-statements"></a> Betalingskonfigurasjoner for detaljhandelsutdrag

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Denne prosedyren beskriver konfigurasjoner for betalingsmetoder for detaljhandel, som påvirker hvordan detaljhandelsutdrag opprettes og posteres.

Denne registreringen bruker demonstrasjonsfirmaet USRT.

1. Gå til Detaljhandel og handel > Kanaler > Detaljhandelbutikker > Alle detaljhandelsbutikker.
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


