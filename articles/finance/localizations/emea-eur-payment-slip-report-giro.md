---
title: Betalingsseddelrapport for Europa
description: Denne artikkelen gir informasjon om betalingsseddelrapport for Europa.
author: mrolecki
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 99e06f383c94db6d2a1585d33d9f183b0984f5a3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689593"
---
# <a name="payment-slip-report-for-europe"></a>Betalingsseddelrapport for Europa

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om betalingsseddelrapport for Europa.

Funksjonaliteten for betalingsseddelrapport er tilgjengelig for juridiske enheter som har den primære adressen i Danmark, Belgia, Norge, Sveits og Finland. Bedrifter knytter ofte utskrevne betalingsbilag til fakturaer som skal gi en betalingsreferanse for postering og utligning. Betalingsbilaget kan brukes til prosjekt- eller tjenestefakturaer, purringer, rentenotaer og kontoutdrag, i tillegg til salgsfakturaer og fritekstfakturaer.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Definere et ID-nummer for kreditor (bare Danmark)
Følg disse trinnene for å angi firmakreditorens identifikasjonsnummer. Finansinstitusjonen gir dette nummeret. Dette nummeret brukes som referanse når du mottar kundebetalinger via finansinstitusjoner.

1.  Klikk **Organisasjonsstyring** &gt; **Oppsett** &gt; **Organisasjon** &gt; **Juridiske enheter**.
2.  På hurtigfanen **Bankkontoinformasjon** i feltet **ID for FI-kreditor** angir du det unike 8-sifrede ID-nummeret for kreditoren.
3.  Lukk skjemaet for å lagre endringene.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Definere et format for betalingsseddelvedlegg for fakturaer, rentenotaer, purrebrev og kontoutdrag
Følg denne fremgangsmåten for å definere et format for et betalingsbilagsvedlegg for salgsfakturaer, fritekstfakturaer, rentenotaer, purringer og kontoutdrag.

1.  Klikk **Kunder** &gt; **Oppsett** &gt; **Skjemaer** &gt; **Skjemaoppsett**.
2.  Velg format for betalingsseddelvedlegg i **Faktura**-kategorien i feltet **Tilknyttet betalingsvedlegg på kundefaktura**.
3.  Velg et format for betalingsseddelvedlegg for hver dokumenttype i kategoriene **Fritekstfaktura**, **Rentenota**, **Purring** og **Kontoutdrag**.
4.  Lukk skjemaet for å lagre endringene.

Følg denne fremgangsmåten for å definere et format for et betalingsseddelvedlegg som skal følge prosjektfakturaer.

1.  Klikk på **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Skjemaer** &gt; **Skjemaoppsett**.
2.  I feltet **Tilknyttet betalingsvedlegg** velger du format for betalingsseddelvedlegg.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Tilordne et format for betalingsseddelvedlegg til en kundekonto
Når du har satt opp formatet for betalingsseddelvedlegg for salgsfakturaer, fritekstfakturaer, rentenotaer, purringer, kontoutdrag og prosjektfakturaer, kan du tilordne bestemte formater for en valgt kunde.

1.  Klikk **Kunder** &gt; **Felles** &gt; **Kunder** &gt; **Alle kunder**.
2.  Opprett en ny kunde, eller velg en eksisterende kunde.
3.  På hurtigfanen **Faktura og levering** i feltene **På en kundefaktura**, **På en fritekstfaktura**, **På en rentenota**, **På en purring**, **På en prosjektfaktura** og **På et kontoutdrag**, velger du formatet for betalingsseddelvedlegg som skal følge dokumenter for hver type som sendes til den valgte kunden.
4.  Lukk skjemaet for å lagre endringene.


Hvis du vil ha mer informasjon om hvordan du definerer og vedlikeholder betalings-IDer, kan du se [NO-00002 Kundebetaling basert på betalings-ID](tasks/no-00002-customer-payment-based-payment-id.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
