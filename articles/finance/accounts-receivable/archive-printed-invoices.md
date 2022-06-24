---
title: Arkivere utskrevne kundefakturaer med hash-numre
description: Denne artikkelen beskriver hvordan du aktiverer arkivering for å lagre utskrevne kundefakturaer med hash-numre.
author: ilkond
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3f19968b4f4cf76a48ac5485e915785e9be5c7db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909192"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Arkivere utskrevne kundefakturaer med hash-numre

[!include [banner](../includes/banner.md)]

I noen land er det et juridisk krav om å lagre beregnede hash-numre i systemet sammen med utskrifter av enkelte dokumenter. Hash-numrene kan brukes til rapportering til myndighetene og i løpet av revisjoner.

Denne artikkelen beskriver hvordan du konfigurerer arkivering for å lagre utskrevne kundefakturaer med hash-numre.

## <a name="prerequisites"></a>Forutsetninger

- I arbeidsområdet **Funksjonsstyring** aktiverer du funksjonen **Arkiver utskrevne kundefakturaer med hash-numre**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Konfigurer de utskriftsbare formatene for de obligatoriske dokumentene i **Utskriftsbehandling**.

Denne funksjonaliteten gjelder for dokumentene nedenfor.

**Kunde**
- Kundefaktura
- Kundekreditnota
- Fritekstfaktura
- Fritekstkreditnota

**Prosjektstyring og regnskap**
- Prosjektfaktura
- Prosjektkreditnota

## <a name="configure-customer-master-data"></a>Konfigurere kundehoveddata
Fullfør fremgangsmåten nedenfor for å konfigurere kundedata, og slå på muligheten til å lagre utskrevne fakturaer automatisk som vedlegg.

1. Gå til **Kunder** > **Alle kunder**. 
2. Velg en kunde, og velg **Ja** i feltet **Vedlegg til eFaktura** i delen **E-FAKTURA** i hurtigfanen **Faktura og levering**.

## <a name="print-invoices"></a>Skriv ut fakturaer
Du kan postere og skrive ut en hvilken som helst fritekst-, kunde- eller prosjektfaktura eller kreditnota for kunden som ble konfigurert i forrige fremgangsmåte.

Åpne siden **Vedlegg** for den utskrevne fakturaen. I feltet **Hash-nummer for dokument** i gruppen **Tilleggsdetaljer** i hurtigfanen **Vedlegg** finner du det lagrede hash-nummeret beregnet for den utskrevne fakturaen.

![Hash-nummer for vedlegg.](media/attach-hash-num.jpg)

