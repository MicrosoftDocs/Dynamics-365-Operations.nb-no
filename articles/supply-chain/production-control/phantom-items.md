---
title: Fantomvarer
description: Denne artikkelen beskriver hvordan linjetypen Fantom kan brukes for linjene i en stykkliste og en formel i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893330"
---
# <a name="phantom-items"></a>Fantomvarer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver detaljer hvordan linjetype Fantom kan brukes for linjene i en stykkliste (BOM) og en formel.

I figur 1 (a) er stykklisten for produkt H og der F og G, og (b) er rutearket for produkt H og del F.

![Figur 1: konstruksjonsstykkliste.](media/product-H-part-F.png)
*Figur 1: konstruksjonsstykkliste*

Figur 1 viser et eksempel på en stykklistestruktur i to nivåer. Det ferdige produktet H representerer et produkt i en maskinmontering. Maskinmonteringen består av to deler, en elektrisk enhet (F) med to materialer (A og B) og en gruppe med emballasje (G) som også har to materialer (C og D). Et annet materiale (E) brukes under den generelle monteringen av maskinen.

Figur 1 representerer konstruksjonsstykklisten for produkt H. Denne strukturen gir god oversikt over delene og komponentene i den generelle maskinmonteringen. Men selv om produktdesignere kanskje vil se stykklisten representert på denne måten, representerer denne strukturen kanskje ikke riktig måten maskinen bygges i butikken.

Konstruksjonsstykklisten i figur 1 angir for eksempel at den elektriske enheten F er montert som en egen del i en egen arbeidsordre. I butikken kan det kanskje være mer optimalt å montere den elektriske enheten som en del av den generelle maskinmonteringen, ikke som en egen arbeidsordre.

Denne konstruksjonsstykklisten angir også at del G er en egen del. I denne strukturen representerer imidlertid ikke del G en fysisk del, men en samling av emballasje.

Derfor, selv om en konstruksjonsstykkliste gir mye for pengene for utformingen av et produkt og vedlikehold av denne utformingen, er det kanskje ikke den mest logiske måten å støtte produksjonsprosessen av produktet. En produksjonstykkliste representerer derimot den beste måten å bygge et produkt på.

Figur 2 viser hvordan den forrige konstruksjonsstykklisten er gått over i en produksjonsstykkliste. I figur 2 (a) er stykklisten for produkt H, og b er rutearket for produkt H.

![Figur 2: produksjonsstykkliste.](media/product-H-part-B.png)
*Figur 2: produksjonsstykkliste*

I denne strukturen kan du se at del F og G ikke er nevnt, og materialene som disse delene består av, har blitt forhøyet til det neste stykklistenivået.

I motsetning til konstruksjonsstykklisten, som har to operasjonsark, har produksjonsstykklisten bare ett ark operasjonsark. Emballasjeoperasjonen som var koblet til en del G, er også forhøyet og er nå en del av operasjonsarket for produkt H. Montering av elektriske enheten er den første operasjonen. Denne rekkefølgen kan være lur, fordi denne enheten brukes i den neste operasjonen, som er maskinmonteringen. Den siste operasjon er emballasjeoperasjonen, som bruker to emballasjematerialer (C og D).

Overgangen aktiveres mellom konstruksjonsstykklisten og produksjonsstykklisten gjennom stykklistelinjetypen Fantom. Som begrepet "fantom" hentyder, er del F og G forsvunnet under overgangen mellom de to stykklistetypene. I dette eksemplet brukes linjetypen Fantom på stykklistelinjene for del F og G i konstruksjonsstykklisten. Når det opprettes en produksjons- eller partiordre, kopieres konstruksjonsstykklisten til produksjons- eller partiordren. Deretter, når ordren er beregnet, oppstår overgangen fra konstruksjonsstykklisten til produksjonsstykklisten, som vist i figur 2. Fra operasjonsarket i figur 2 er emballasjemateriale C og D inndata for operasjonen.

## <a name="multilevel-phantom-bom-structures"></a>Stykklistestrukturer på flere nivåer for fantom

Linjetypen Fantom kan brukes i stykklistestrukturer på flere nivåer, som vist i figur 3. I figur 3 (a) er stykklisten for produkt G, og (b) er rutearket for del E og F og produkt G.

![Figur 3: konstruksjonsstykkliste for del G.](media/product-G.png)
*Figur 3: konstruksjonsstykkliste for del G*

Figur 4 viser den resulterende produksjonsstykklisten og rutearket hvis stykklistelinjene for del E og F er konfigurert slik at linjetypen er Fantom. I figur 4 (a) er stykklisten for produkt G, og (b) er rutearket for produkt G.

![Figur 4: produksjonsstykkliste for del G.](media/product-G-route-sheet-G.png)
*Figur 4: produksjonsstykkliste for del G*

## <a name="phantom-and-route-network"></a>Fantom og rutenettverk

Fantomstykklister kan også brukes for en stykkliste som har et rutenettverk. I et rutenettverk kjøres én eller flere operasjoner parallelt. Figur 5 viser et eksempel på et rutenettverk som brukes i en stykkliste med flere nivåer. I figur 5 (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G og del F, som har et rutenettverk.

![Figur 5: konstruksjonsstykkliste for del G, rutenettverk.](media/product-G-part-F.png)
*Figur 5: konstruksjonsstykkliste for del G, rutenettverk*

I figur 6 (a) er stykklisten for produkt G og del F, og (b) er rutearket for produkt G og del F.

![Figur 6: produksjonstykkliste for del G, rutenettverk.](media/product-G-part-F-with-route-sheet.png)
*Figur 6: produksjonstykkliste for del G, rutenettverk*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]