---
title: Beholdningstilgjengelighet i dobbel skriving
description: Dette emnet inneholder informasjon om hvordan beholdningstilgjengelighet i dobbel skriving sjekkes.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4455827"
---
# <a name="inventory-availability-in-dual-write"></a>Beholdningstilgjengelighet i dobbel skriving

[!include [banner](../../includes/banner.md)]

Ve å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt på sidene **Tilbud**, **Ordre** eller **Fakturaer** i Microsoft Dynamics 365 Sales. Du kan for eksempel kontrollere beholdning og fastslå en fullføringsdato som én hovedoppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen.

Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer. Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.

## <a name="on-hand-inventory"></a>Lagerbeholdning

I Dynamics 365 Sales er en ny **Lagerbeholdning**-knapp lagt til i hodet på sidene **Tilbud**, **Ordrer** og **Fakturaer**. Når du velger denne knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for. Denne dialogboksen viser den samme informasjonen som [Lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogboksen returnerer lagerinformasjonen fra Dynamics 365 Supply Chain Management. Denne informasjonen inneholder følgende antall:

- Antall på lager
- Antall reservert på lager
- Antall tilgjengelig på lager
- Bestilt antall
- Antall i bestilling
- Reservert bestilt antall
- Totalt tilgjengelig antall

## <a name="atp-information"></a>ATP-informasjon

I Sales er det lagt til en ny **ATP-informasjon**-knapp for linjeelementer på sidene **Tilbud**, **Ordrer** og **Fakturaer**. Når du velger denne knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall. Denne dialogboksen har de samme innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogboksen returnerer ATP-informasjonen fra Supply Chain Management. Denne informasjonen inneholder følgende antall:

- ATP-antall
- Tilgangsantall
- Avgangsantall
- Antall på lager


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]