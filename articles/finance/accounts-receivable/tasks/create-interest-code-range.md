---
title: Opprette en rentekode med et område
description: Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c18269d277f64433da35e7dc1675cd3afda8e070
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835034"
---
# <a name="create-an-interest-code-with-a-range"></a>Opprette en rentekode med et område

[!include [banner](../../includes/banner.md)]
Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde. Denne prosedyren viser hvordan du legger til en rentekode og legger til et område i den.

1. Gå til Kreditt og innkreving > Rente > Definer rentekoder.
2. Klikk Ny.
3. Skriv inn navnet på rentekoden i Rentekode-feltet.
4. I Beskrivelse-feltet skriver du inn en beskrivelse for rentekoden.
5. Velg Måned.
6. Utvid delen Inntekter.
7. Utvid delen Inntjening etter valuta.
8. Angi ønskede verdier i feltet Posteringskonto for finans.
9. Velg Måneder i feltet Rente etter intervall.
10. Klikk Legg til.
11. I Beskrivelse-feltet angir du en beskrivelse for valutaen og området.
12. Klikk Lagre.
13. Klikk Områder.
14. Klikk Ny.
15. Sett Fra-verdien til 0, og angi deretter renteprosenten per måned som skal brukes til å beregne renten. I vårt eksempel er det 1,5.
16. Klikk Ny.
17. Sett neste Fra-verdi til 4, som er den første måneden du skal beregne et nytt rentebeløp for.
18. Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 4. I vårt eksempel er det 2,0.
19. Klikk Ny.
20. Sett neste Fra-verdi til 7, som er den neste måneden du skal beregne et nytt rentebeløp for.
21. Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 7. I vårt eksempel er det 2,5.
22. Klikk Lukk for å fullføre oppsettet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]