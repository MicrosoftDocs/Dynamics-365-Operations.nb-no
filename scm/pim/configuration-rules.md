---
title: Konfigurasjonsregler
description: Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 271a780eec291455b433c0767246d79cb965ce02
ms.lasthandoff: 03/31/2017


---

# <a name="configuration-rules"></a>Konfigurasjonsregler

[!include[banner](../includes/banner.md)]


Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.

Konfigurasjonsregler er tilgjengelige når du definerer dimensjonsbaserte konfigurasjonsmodeller. Konfigurasjonsregler brukes til å fremtvinge eller forby bestemte varekombinasjoner i en stykkliste. Du kan definere én eller flere konfigurasjonsregler når en stykkliste har blitt opprettet og de aktuelle varene er tilordnet til de respektive konfigurasjonsgruppene. Hvis to varer hører sammen, brukes operatoren **Velg** til å sikre inkludering. Hvis to varer er gjensidig utelukkende, brukes operatoren **Fjern merking** til å sikre utelatelse.  

**Obs! ** Denne informasjonen gjelder bare for produktstandarder som bruker dimensjonsbasert konfigurasjonsteknologi.  

Eksisterende konfigurasjoner påvirkes ikke av etterfølgende endringer i konfigurasjonsreglene. Det er imidlertid viktig at du definerer reglene før du definerer en ny konfigurasjon, og at du kontrollerer reglene hvis du tror at de er endret.  

**Obs! ** For metoden **Velg** velges den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen automatisk. For metoden **Fjern merking** kan ikke den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen velges.

<a name="see-also"></a>Se også
--------

[Dimensjonsbasert produktkonfigurasjon](dimension-based-product-configuration.md)




