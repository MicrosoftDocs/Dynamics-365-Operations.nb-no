---
title: Beholdningstilgjengelighet i dobbel skriving
description: Dette emnet inneholder informasjon om å sjekke beholdningstilgjengelighet i dobbel skriving.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426988"
---
# <a name="inventory-availability"></a>Beholdningstilgjengelighet

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Ved å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i modelldrevne apper i Dynamics 365. Det å kontrollere beholdning og fastslå en fullføringsdato er for eksempel en nøkkeloppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen. Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer. Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.

## <a name="on-hand-inventory"></a>Lagerbeholdning 

I toppteksten i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i Dynamics 365 Sales, legges det til en ny knapp for **Lagerbeholdning**. Når du klikker på knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for. Den returnerer beholdningsinformasjonen fra Dynamics 365 Supply Chain Management, og viser den samme informasjonen som [Tilgjengelig beholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Informasjonen inkluderer disse antallene:

- **Antall på lager**
- **Antall reservert på lager**
- **Antall tilgjengelig på lager**
- **Antall bestilt**
- **Antall i bestilling**
- **Antall reservert og bestilt**
- **Totalt tilgjengelig antall**

## <a name="atp-information"></a>ATP-informasjon

På linjeelementer i skjemaene **Tilbud**, **Ordre** eller **Fakturaer** i Dynamics 365 Sales, legges det til en ny knapp for **ATP-informasjon**. Når du klikker på knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall. Den returnerer **ATP-informasjon** fra Supply Chain Management, og viser innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Informasjonen omfatter **ATP-antall**, **Tilgangsantall**, **Avgangsantall** og **Beholdningsantall**.
