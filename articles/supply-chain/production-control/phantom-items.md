---
title: Fantomvarer
description: Dette emnet beskriver detaljer hvordan linjetype Fantom kan brukes for linjene i en stykkliste (BOM) og en formel i Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434592"
---
# <a name="phantom-items"></a>Fantomvarer

[!include [banner](../includes/banner.md)]

Dette emnet beskriver detaljer hvordan linjetype Fantom kan brukes for linjene i en stykkliste (BOM) og en formel. I illustrasjonen nedenfor (a) er stykklisten for produkt H og der F og G, og (b) er rutearket for produkt H-og del F.

![Produkt H og del F](media/product-H-part-F.png)


Denne illustrasjonen viser et eksempel på en stykklistestruktur i to nivåer. Det ferdige produktet H representerer et produkt i en maskinmontering. Maskinmonteringen består av to deler, en elektrisk enhet (F) med to materialer (A og B) og en gruppe med emballasje (G) som også har to materialer (C og D). Et annet materiale (E) brukes under den generelle monteringen av maskinen.

![Produkt H og del F](media/product-H-part-B.png)

Den forrige illustrasjonen representerer konstruksjonsstykklisten for produkt H. Denne strukturen gir god oversikt over delene og komponentene i den generelle maskinmonteringen. Men selv om produktdesignere kanskje vil se stykklisten representert på denne måten, representerer denne strukturen kanskje ikke riktig måten maskinen bygges i butikken. 

Konstruksjonsstykklisten i den forrige illustrasjonen angir for eksempel at den elektriske enheten F er montert som en egen del i en egen arbeidsordre. I butikken kan det kanskje være mer optimalt å montere den elektriske enheten som en del av den generelle maskinmonteringen, ikke som en egen arbeidsordre.

Denne konstruksjonsstykklisten angir også at del G er en egen del. I denne strukturen representerer imidlertid ikke del G en fysisk del, men en samling av emballasje. 

Derfor, selv om en konstruksjonsstykkliste gir mye for pengene for utformingen av et produkt og vedlikehold av denne utformingen, er det kanskje ikke den mest logiske måten å støtte produksjonsprosessen av produktet. En produksjonstykkliste representerer derimot den beste måten å bygge et produkt på.

Illustrasjonen nedenfor viser hvordan den forrige konstruksjonsstykklisten er gått over i en produksjonsstykkliste. I denne illustrasjonen (a) er stykklisten for produkt H, og b er rutearket for produkt H.

I denne strukturen kan du se at del F og G ikke er nevnt, og materialene som disse delene består av, har blitt forhøyet til det neste stykklistenivået. 

I motsetning til konstruksjonsstykklisten, som har to operasjonsark, har produksjonsstykklisten bare ett ark operasjonsark. Emballasjeoperasjonen som var koblet til en del G, er også forhøyet og er nå en del av operasjonsarket for produkt H. Montering av elektriske enheten er den første operasjonen. Denne rekkefølgen kan være lur, fordi denne enheten brukes i den neste operasjonen, som er maskinmonteringen. Den siste operasjon er emballasjeoperasjonen, som bruker to emballasjematerialer (C og D).

Overgangen aktiveres mellom konstruksjonsstykklisten og produksjonsstykklisten gjennom stykklistelinjetypen Fantom. Som begrepet "fantom" hentyder, er del F og G forsvunnet under overgangen mellom de to stykklistetypene. I dette eksemplet brukes linjetypen Fantom på stykklistelinjene for del F og G i konstruksjonsstykklisten. Når det opprettes en produksjons- eller partiordre, kopieres konstruksjonsstykklisten til produksjons- eller partiordren. Deretter, når ordren er beregnet, oppstår overgangen fra konstruksjonsstykklisten til produksjonsstykklisten, som vist i illustrasjonene ovenfor. Fra operasjonsarket i den andre illustrasjonen er emballasjemateriale C og D inndata for operasjonen. 

## <a name="multilevel-phantom-bom-structures"></a>Stykklistestrukturer på flere nivåer for fantom
Linjetype Fantom kan brukes i stykklistestrukturer på flere nivåer, som vist i illustrasjonen nedenfor. I denne illustrasjonen (a) er stykklisten for produkt G, og (b) er rutearket for del E og F og produkt G. 

![Produkt G og del F med ruteark](media/product-G-route-sheet-G.png)


Illustrasjonen nedenfor viser den resulterende produksjonsstykklisten og rutearket hvis stykklistelinjene for dele E og F er konfigurert slik at linjetypen er Fantom. I denne illustrasjonen (a) er stykklisten for produkt G, og (b) er rutearket for produkt G.

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fantom og rutenettverk
Fantomstykklister kan også brukes for en stykkliste som har et rutenettverk. I et rutenettverk kjøres én eller flere operasjoner parallelt. Illustrasjonen nedenfor viser et eksempel på et rutenettverk som brukes i en stykkliste med flere nivåer. I denne illustrasjonen (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenettverk.

![Produkt G og del F](media/product-G-part-F.png)


I illustrasjonen nedenfor (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G-og del F.

![Produkt G og del F med ruteark](media/product-G-part-F-with-route-sheet.png)
