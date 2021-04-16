---
title: Oversikt over hovedplanlegging og multisite-funksjonalitet
description: Hovedplanlegging tar hensyn til innstillingene for område- og lagerdimensjonene.
author: roxanadiaconu
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30bb8dfb790958b30cb3be807847ee737fb5026
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833575"
---
# <a name="master-planning-and-multisite-functionality-overview"></a>Oversikt over hovedplanlegging og multisite-funksjonalitet

[!include [banner](../includes/banner.md)]

Hovedplanlegging tar hensyn til innstillingene for område- og lagerdimensjonene. 

Områdedimensjonen er obligatorisk, og du må angi at lagerdimensjonen er obligatorisk.

Når en dimensjon er obligatorisk, må du angi en dimensjonsverdi for alle lagertransaksjoner. I hovedplanleggingen er derfor området og lageret for det opprinnelige behovet kjent. Områdedimensjonen er også konsekvent slik at stedsverdien ikke endres i løpet av nedbrytingen av lavnivåbehov.

Når lageret ikke er satt til obligatorisk, kan det være at det ikke er kjent fra det opprinnelige behovet. Planleggingsmotoren må bestemme hvilket lager som skal brukes, basert på innstillingene som er angitt for varen, individuelle lagre og detaljene i ordrelinjen.

Følgende emner beskriver hvordan planleggingsmotoren fungerer når forskjellige innstillinger er definert for å bestemme hvilket lager som skal brukes.

[Hovedplanlegging for område- og lagerdekning, lager obligatorisk](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Hovedplanlegging for områdedekning, obligatorisk lager](master-plan-site-coverage-warehouse-mandatory.md)

[Hovedplanlegging for område- og lagerdekning, lager ikke obligatorisk](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Hovedplanlegging for områdedekning, lager ikke obligatorisk](master-plan-site-coverage-warehouse-not-mandatory.md)

[Fastslå stykklisteversjonen](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]