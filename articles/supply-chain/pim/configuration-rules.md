---
title: Konfigurasjonsregler
description: Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13f37cb4e472e91862e963a4952adcf61e6adcea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "319368"
---
# <a name="configuration-rules"></a>Konfigurasjonsregler

[!include [banner](../includes/banner.md)]

Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.

Konfigurasjonsregler er tilgjengelige når du definerer dimensjonsbaserte konfigurasjonsmodeller. Konfigurasjonsregler brukes til å fremtvinge eller forby bestemte varekombinasjoner i en stykkliste. Du kan definere én eller flere konfigurasjonsregler når en stykkliste har blitt opprettet og de aktuelle varene er tilordnet til de respektive konfigurasjonsgruppene. Hvis to varer hører sammen, brukes operatoren **Velg** til å sikre inkludering. Hvis to varer er gjensidig utelukkende, brukes operatoren **Fjern merking** til å sikre utelatelse.  

**Obs!** Denne informasjonen gjelder bare for produktstandarder som bruker dimensjonsbasert konfigurasjonsteknologi.  

Eksisterende konfigurasjoner påvirkes ikke av etterfølgende endringer i konfigurasjonsreglene. Det er imidlertid viktig at du definerer reglene før du definerer en ny konfigurasjon, og at du kontrollerer reglene hvis du tror at de er endret.  

**Obs!** For metoden **Velg** velges den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen automatisk. For metoden **Fjern merking** kan ikke den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen velges.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Dimensjonsbasert produktkonfigurasjon](dimension-based-product-configuration.md)



