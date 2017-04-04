---
title: Slip betalingsrapport for Europa
description: Dette emnet gir informasjon om betaling slip rapporter for Europa.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Slip betalingsrapport for Europa

Dette emnet gir informasjon om betaling slip rapporter for Europa.

Funksjonaliteten for betaling slip rapporter er tilgjengelig for juridiske enheter som har den primære adressen i Danmark, Belgia, Norge, Sveits og Finland. Bedrifter knytte ofte utskrevne betalingsbilag til fakturaer for å oppgi en betalingsreferanse for postering, utligning. Betalingsbilaget kan brukes til prosjekt- eller tjenestefakturaer, purringer, rentenotaer og kontoutdrag, i tillegg til salgsfakturaer og fritekstfakturaer.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Sette opp en kreditor ID-nummer (bare Danmark)
Følg disse trinnene for å angi firmaets kreditor identifikasjon (ID)-nummer. Finansinstitusjonen gir dette nummeret. Den brukes som referanse når du mottar kundebetalinger gjennom finansinstitusjoner.

1.  Klikk **organisasjonsadministrasjon**&gt;**Setup**&gt;**organisasjonen**&gt;**juridiske enheter**.
2.  På den **bankkontoinformasjon** hurtigfanen i den **ID for FI-kreditor** angir det unike kreditor i åtte-sifret ID-nummeret.
3.  Lukk skjemaet for å lagre endringene.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Definer en betalings slip Vedleggsformat for fakturaer, rentenotaer, purringer og kontoutdrag
Følg disse trinnene for å definere et format for betaling slip vedlegg som følger med salgsfakturaer, fritekstfakturaer, rentenotaer, purringer og kontoutdrag.

1.  Klikk **kunder**&gt;**Setup**&gt;**skjemaer**&gt;**skjemaoppsett**.
2.  På den **faktura** -kategorien i den **tilknyttet betalingsvedlegg på kundefaktura** velger betalingsformatet for slip-vedlegg.
3.  På den **fritekstfaktura**, **rentenotaen**, **purringen**, og **konto setningen** velger en betaling slip Vedleggsformat for hver dokumenttype.
4.  Lukk skjemaet for å lagre endringene.

Følg disse trinnene for å definere et format for betaling slip vedlegg som følger med prosjektfakturaer.

1.  Klikk **prosjekt prosjektstyring og regnskap**&gt;**Setup**&gt;**skjemaer**&gt;**skjemaoppsett**.
2.  I den **tilknyttet betalingsvedlegg** velger betalingsformatet for slip-vedlegg.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Tilordne en betalingsformatet for slip vedlegg til en kundekonto
Når du setter opp slip vedlegg betalingsformatet for salgsfakturaer, fritekstfakturaer, rentenotaer, purringer, kontoutdrag og prosjektfakturaer, kan du tilordne bestemte formater for en valgt kunde.

1.  Klikk **kunder**&gt;**vanlige**&gt;**kunder**&gt;**alle kunder**.
2.  Opprette en ny kunde, eller velg en eksisterende kunde.
3.  På den **faktura- og** hurtigfanen i den **på en kundefaktura**, **på en fritekstfaktura**, **på en rentenota**, **på en purring**, **på en prosjektfaktura**, og **på et kontoutdrag** felt, velger du formatet for betaling slip vedlegg som skal følge dokumenter for hver type som sendes til den valgte kunden.
4.  Lukk skjemaet for å lagre endringene.



