---
title: Opprette en rentekode med et område
description: Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d77fc88f606f4e690583fbcda79f628a35f14f6a
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119480"
---
# <a name="create-an-interest-code-with-a-range"></a>Opprette en rentekode med et område

[!include [banner](../../includes/banner.md)]
Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde. Denne prosedyren viser hvordan du legger til en rentekode og legger til et område i den.

1. Gå til **Kreditt og innkreving > Rente > Definer rentekoder**.
2. Klikk på **Ny**.
3. Skriv inn navnet på rentekoden i **Rentekode**-feltet.
4. I **Beskrivelse**-feltet skriver du inn en beskrivelse for rentekoden.
5. Velg **Måned**.
6. Utvid delen **Inntekter**.
7. Utvid delen **Inntjening etter valuta**.
8. Angi ønskede verdier i feltet **Posteringskonto for finans**.
9. Velg Måneder i feltet **Rente etter intervall**.
10. Klikk på **Legg til**.
11. I **Beskrivelse**-feltet angir du en beskrivelse for valutaen og området.
12. Klikk på **Lagre**.
13. Klikk på **Områder**.
14. Klikk på **Ny**.
15. Sett **Fra-verdi** til 0, og angi deretter renteprosenten per måned som skal brukes til å beregne renten. I vårt eksempel er det 1,5.
16. Klikk på **Ny**.
17. Sett neste Fra-verdi til 4, som er den første måneden du skal beregne et nytt rentebeløp for.
18. Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 4. I vårt eksempel er det 2,0.
19. Klikk på **Ny**.
20. Sett neste Fra-verdi til 7, som er den neste måneden du skal beregne et nytt rentebeløp for.
21. Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 7. I vårt eksempel er det 2,5.
22. Klikk på **Lukk** for å fullføre oppsettet.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
