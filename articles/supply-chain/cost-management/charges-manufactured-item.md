---
title: Vise tillegg for en produsert vare
description: De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235514"
---
# <a name="display-charges-for-a-manufactured-item"></a>Vise tillegg for en produsert vare

[!include [banner](../includes/banner.md)]

De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.

Det beregnede beløpet for en vares tillegg kan vises med varens enhetskostnader. Tilleggene vises imidlertid noen ganger som separate felt, og de er ikke inkludert i varens enhetskostnader. Når tilleggene vises som separate felt, viser ett felt det samlede tilleggsbeløpet, og det andre feltet viser kostnadspartistørrelsen (som kalles prisenheten) som ble brukt da beløpet ble nedbetalt. Varepris-siden viser for eksempel tilleggene som to separate felt. Siden Fullført viser imidlertid varens totale kostnad per enhet, og nedbetalte kostnader er inkludert i enhetskosten.

Tilleggene for en produsert vare inkluderes alltid i varens enhetskostnad til standardkostformål. De kan om ønskelig inkluderes også til planlagt kost-formål. En policy i etterkalkuleringsversjonen implementerer beslutningen om å inkludere tillegg i en produsert vares kostnader. Når du aktiverer en vares kostnadspost, oppdaterer du tilleggene for varens basiskostinformasjon, som vises på Varepris-siden. Tilleggene vises som to separate felt, og de er ikke inkludert i varens enhetskostnader. Hver aktivering oppdaterer varens basiskostinformasjon, selv om aktiveringen gjenspeiler forskjellige områder. Du bør derfor vise basiskostinformasjonen som referanseinformasjon.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]