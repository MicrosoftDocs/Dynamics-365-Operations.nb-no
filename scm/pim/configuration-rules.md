---
title: Konfigurasjonsregler
description: Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 74c8ffe4ab00e7afa1235e24327e18a65061636a
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="configuration-rules"></a>Konfigurasjonsregler

[!include[banner](../includes/banner.md)]


Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.

Konfigurasjonsregler er tilgjengelige når du definerer dimensjonsbaserte konfigurasjonsmodeller. Konfigurasjonsregler brukes til å fremtvinge eller forby bestemte varekombinasjoner i en stykkliste. Du kan definere én eller flere konfigurasjonsregler når en stykkliste har blitt opprettet og de aktuelle varene er tilordnet til de respektive konfigurasjonsgruppene. Hvis to varer hører sammen, brukes operatoren **Velg** til å sikre inkludering. Hvis to varer er gjensidig utelukkende, brukes operatoren **Fjern merking** til å sikre utelatelse.  

**Obs!** Denne informasjonen gjelder bare for produktstandarder som bruker dimensjonsbasert konfigurasjonsteknologi.  

Eksisterende konfigurasjoner påvirkes ikke av etterfølgende endringer i konfigurasjonsreglene. Det er imidlertid viktig at du definerer reglene før du definerer en ny konfigurasjon, og at du kontrollerer reglene hvis du tror at de er endret.  

**Obs!** For metoden **Velg** velges den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen automatisk. For metoden **Fjern merking** kan ikke den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen velges.

<a name="see-also"></a>Se også
--------

[Dimensjonsbasert produktkonfigurasjon](dimension-based-product-configuration.md)




