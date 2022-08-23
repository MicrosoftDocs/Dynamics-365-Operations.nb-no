---
title: Referere til opprinnelige fakturaer i kreditnotaer (leverandørfakturaer)
description: Denne artikkelen beskriver hvordan du oppretter en referanse til en opprinnelig faktura når du oppretter en kreditnota.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277378"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Referere til opprinnelige fakturaer i kreditnotaer (leverandørfakturaer)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter en referanse til en opprinnelig faktura når du oppretter en kreditnota.

## <a name="prerequisites"></a>Forutsetninger

I arbeidsområdet **Funksjonsbehandling** aktiverer du funksjonen for å **aktivere kreditering av fakturering for leverandørfakturaer**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Funksjonaliteten som er beskrevet i denne artikkelen, gjelder følgende forretningsdokumenter.

**Leverandør:**

- Bestilling
- Fakturajournal
- Ankomstregistrering

**Økonomi:**

- Økonomijournal

## <a name="define-a-reference-to-an-original-invoice"></a>Definere en referanse til en opprinnelig faktura

Bruk følgende fremgangsmåter til å definere referanser til opprinnelige fakturaer i de angitte forretningsdokumenttypene.

### <a name="vendor-credit-note-purchase-order"></a>Leverandørkreditnota (bestilling)

1. Gå til **Leverandører** \> **Bestillinger** \> **Alle bestillinger**.
2. Opprett en ny bestilling, eller bruk en eksisterende til å opprette en kreditnota.
3. I handlingsruten, på **Faktura**-fanen i **Introduser**-gruppen, velger du **Krediter fakturering**.
4. Angi årsaken til rettelsen og referansen til den opprinnelige fakturaen.

### <a name="vendor-credit-note-ledger-journals"></a>Leverandørkreditnota (finansjournaler)

1. Følg ett av disse trinnene:

    - Gå til **Leverandører** \> **Fakturajournaler**.
    - Gå til **Leverandører** \> **Ankomstregistrering**.
    - Gå til **Økonomimodul** \> **Journaloppføringer** \> **Økonomijournaler**.

2. Opprett en ny journal og nye journallinjer.
3. Velg **Funksjoner** \> **Krediter fakturering** i handlingsruten.
4. Angi årsaken til rettelsen og referansen til den opprinnelige fakturaen.

> [!NOTE]
> Kommandoen **Krediter fakturering** er synlig i et generelt journalbilag hvis **Kontotype**-feltet er satt til **Leverandør**.
