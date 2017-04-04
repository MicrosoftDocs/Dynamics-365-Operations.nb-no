---
title: Hybrid kundeordrer
description: "En kundeordre hybrid er en enkelt ordre som inneholder produkter som kan overføres ut av butikken av kunden, i tillegg til produktene som skal plukkes opp eller sendt senere."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid kundeordrer

En kundeordre hybrid er en enkelt ordre som inneholder produkter som kan overføres ut av butikken av kunden, i tillegg til produktene som skal plukkes opp eller sendt senere.

I Microsoft Dynamics 365 for operasjoner - detaljhandel, kan du velge enten bære alle produkter eller utføre valgte produkter for en kundeordre. Produktet linjer som er merket som utfører automatisk faktureres etter at bestillingen er opprettet, på samme måte dette er det samme for en ordre som skal plukkes opp når ordren opprettes. Det forfalte beløpet på hybrid bestemmes ordrer ved å legge prosenten innskudd på plukke og Lever produktlinjene med full mengden bære ut linjer. For hybrid ordrer veksler systemet mellom kunde bestilling modus og kontant og ta modus som følger:

-   Hvis alle produkter i handlekurven er satt til **utføre levering**, bestillingen vil bli behandlet som en kontant og ta med transaksjon.
-   Hvis noen av eller alle linjene i handlekurven er satt til enten **plukke** eller **leverer levering**, bestillingen vil bli behandlet som en kundetransaksjon rekkefølge.

Hvis en handlevogn linje er valgt og **Velg valgt**, **Lever valgt**, eller **utfører valgte** er valgt, settes bare bestemte handlekurv linjen med den leveringsmetoden. I så fall fortsetter nedstrøms flyten av operasjonen som vanlig. Imidlertid Hvis **Velg valgt**, **Lever valgt**, eller **utfører valgte** velges uten en handlevogn linje blir valgt, en ny side åpnes som viser alle linjene for handlekurv. På dette skjermbildet kan du velge flere linjer samtidig for å angi leveringsmåte. Når du bruker denne metoden for å velge linjer, vil bli overstyrt forrige leveringsmåte som er knyttet til linjen.

<a name="see-also"></a>Se også
--------

[Oversikt over ordrer for kunde](customer-orders-overview.md)


