---
title: Feilsøke utgående lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med utgående lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 919b6f433db47f24adc9a474942557a1467d1f71
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828184"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>Feilsøke utgående lageroperasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med utgående lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>Jeg får følgende feilmelding: Salgsordre kan ikke frigis.

### <a name="issue-description"></a>Problembeskrivelse

Dette problemet kan oppstå av flere årsaker. Ordren er for eksempel på vent for kredittbehandling, og ingen forsendelser kan opprettes før en gyldig postadresse angis for alle salgslinjer som er tilknyttet en salgsordre. Det finnes også en ordresperre som må løses før ordren kan frigis til lageret. Denne sperringen kan være ordrespesifikk, eller den kan være på kundekontoen.

### <a name="issue-resolution"></a>Problemløsning

Legg til eller oppdater adressen på salgsordren og ordrelinjene, og frigi deretter ordren til lageret. Ordrer kan bare frigis til lageret hvis de har en gyldig leveringsadresse (per adresseformatoppsettet i modulen **Organisasjonsstyring**).

Undersøk ordresperringen og løs problemene. Fjern deretter sperringen fra ordren eller kunden, og frigi ordren til lageret.

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>Jeg får følgendemelding: Forsendelsen for lasten 1% er bekreftet. Ingen linjer er imidlertid postert.

### <a name="issue-description"></a>Problembeskrivelse

En forsendelse på en last ble bekreftet, men det har ikke vært flere posteringer.

### <a name="issue-resolution"></a>Problemløsning

Forsendelsesbekreftelsen påvirker ikke postering. Den oppdaterer bare forsendelses- og laststatusen. Posteringen må forekomme i en egen prosess.

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>Jeg får følgende feilmelding: Direkte levering kan ikke behandle for lager 1% fordi lagerstyring er aktivert. Angi et annet lager som ikke er aktivert for lagerstyring.

### <a name="issue-description"></a>Problembeskrivelse

En vare legges til en salgslinje for direkte levering fra et lager som er aktivert for lagerstyring (WMS). Du får denne feilmeldingen når salgslinjen oppdateres. 

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket støtter ikke WMS direkte levering. Hvis du vil bruke direkte levering, må du derfor velge en vare og et lager som ikke er WMS.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]