---
title: Justere kostnadsverdier for lagerbeholdning
description: Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673305"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Justere kostnadsverdier for lagerbeholdning

[!include [banner](../includes/banner.md)]

Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt.

Du kan bruke siden **Justering av lagerbeholdning** til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt. **Obs!** Du åpner siden **Justering av lagerbeholdning** ved å velge posten for en fullført lagerlukkingsprosess på siden **Lukking og justering** og deretter klikke på **Justering** &gt; **Beholdning**. **Eksempel:** Du har følgende transaksjoner i februar:

-   1. februar: Et økonomisk lagermottak av et antall på 2 til en kostnad på USD 10,00
-   5. februar: Et økonomisk lagermottak av et antall på 1 til en kostnad på USD 13,00
-   19. februar: En økonomisk lageravgang av et antall på 1 til en løpende gjennomsnittlig kostnad på USD 11,00

Denne varen ble definert med først-inn-først-ut-lagermodellen, og lagerlukkingen ble utført per 28. februar. Den økonomiske avgangstransaksjonen på USD 11,00 vil bli utlignet til det økonomiske mottaket datert 1. februar, og en justering på USD 1,00 blir foretatt. Følgende lagermottak vil dermed inneholde åpne lagerantall:

-   1. februar: Et antall på 1 til en kostnad på USD 10,00
-   5. februar: Et antall på 1 til en kostnad på USD 13,00

Når du skal definere disse to varenes kost til USD 15,00, bruker du alternativet for lagerjustering til å justere åpne lagerantall per siste lagerlukkingsperiode. **Obs!** Posteringsdatoen for lagerjusteringstransaksjonen blir datoen for den siste lagerlukkingen. Denne datoen kan ikke endres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]