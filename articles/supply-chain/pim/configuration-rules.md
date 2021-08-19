---
title: Konfigurasjonsregler
description: Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a9c4fe7ad8508a393ab4947340f77576627711042c6d2798be614a48971680
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715824"
---
# <a name="configuration-rules"></a>Konfigurasjonsregler

[!include [banner](../includes/banner.md)]

Denne artikkelen gir generell informasjon om konfigurasjonsregler. Konfigurasjonsregler definerer relasjoner mellom elementer i en stykkliste for produkter som bruker teknologi for dimensjonsbasert konfigurasjon.

Konfigurasjonsregler er tilgjengelige når du definerer dimensjonsbaserte konfigurasjonsmodeller. Konfigurasjonsregler brukes til å fremtvinge eller forby bestemte varekombinasjoner i en stykkliste. Du kan definere én eller flere konfigurasjonsregler når en stykkliste har blitt opprettet og de aktuelle varene er tilordnet til de respektive konfigurasjonsgruppene. Hvis to varer hører sammen, brukes operatoren **Velg** til å sikre inkludering. Hvis to varer er gjensidig utelukkende, brukes operatoren **Fjern merking** til å sikre utelatelse.  

**Obs!** Denne informasjonen gjelder bare for produktstandarder som bruker dimensjonsbasert konfigurasjonsteknologi.  

Eksisterende konfigurasjoner påvirkes ikke av etterfølgende endringer i konfigurasjonsreglene. Det er imidlertid viktig at du definerer reglene før du definerer en ny konfigurasjon, og at du kontrollerer reglene hvis du tror at de er endret.  

**Obs!** For metoden **Velg** velges den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen automatisk. For metoden **Fjern merking** kan ikke den avledede konfigurasjonsgruppen, det avledede varenummeret og den avledede konfigurasjonen velges.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over dimensjonsbasert produktkonfigurasjon](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]