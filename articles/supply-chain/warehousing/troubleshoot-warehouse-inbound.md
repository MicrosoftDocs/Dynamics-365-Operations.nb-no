---
title: Feilsøke innkommende lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645978"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>Feilsøke innkommende lageroperasjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med innkommende lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>Jeg får følgende feilmelding: Kvalitetsordre %1 er generert. Finner ikke gruppeprofil. Kontroller konfigurasjonen.

### <a name="issue-description"></a>Problembeskrivelse

Denne feilmeldingen er knyttet til en mottaksprosess der kvalitetsstyring (QMS) er aktivert. Avhengig av konfigurasjonene i miljøet ditt kan flere detaljer om transaksjonen som genererer feilmeldingen, hjelpe deg med å løse problemet.

### <a name="issue-resolution"></a>Problemløsning

Først kontrollerer du konfigurasjonen for [gruppeplukking](set-up-cluster-picking.md) og kontrollerer at gruppeprofilene er riktig konfigurert. Du kan ikke bruke et menyelement på mobilenheten for gruppeplukking med mindre gruppeprofiler er konfigurert. Avhengig av miljøet kan det være at du også må se gjennom andre tilknyttede konfigurasjoner.

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>Mottak av kombinerte nummerskilter virker ikke for noen disposisjonskode, bortsett fra Kredit.

### <a name="issue-description"></a>Problembeskrivelse

Når **Handling**-feltet for en disposisjonskode er satt til *Kredit* eller *Svinn*, kan du bare bruke menyelementet [Mottak av kombinerte nummerskilter](mixed-license-plate-receiving.md) til å behandle returnerte varer.

### <a name="issue-resolution"></a>Problemløsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket er det bare [disposisjonskoder](../service-management/set-up-disposition-codes.md) der **Handling**-feltet er satt til *Kredit* eller *Svinn*, som støttes for mottak av kombinerte nummerskilter.

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>Når jeg kjører den periodiske oppgaven Oppdater produktkvitteringer, bekreftes ubekreftede bestillinger.

### <a name="issue-description"></a>Problembeskrivelse

Når du har kjørt den periodiske oppgaven *Oppdater produktkvitteringer*, bekrefter systemet automatisk ubekreftede bestillinger som har lagertransaksjonsstatusen *Registrert*.

### <a name="issue-resolution"></a>Problemløsning

En ny inngående lastbehandlingsfunksjon, *Overmottak for lastantall*, løser dette problemet. Hvis du aktiverer denne funksjonen, går du til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktiverer følgende funksjoner (i rekkefølgen de er oppført):

1. Knytt bestillingsbeholdningstransaksjoner til belastning
1. Overmottak for belastningsantall

Hvis du vil ha mer informasjon, kan du se [Poster registrerte produktantall mot bestillinger](inbound-load-handling.md#post-registered-quantities).
