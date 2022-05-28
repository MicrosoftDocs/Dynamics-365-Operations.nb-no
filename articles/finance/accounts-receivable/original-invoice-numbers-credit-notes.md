---
title: Referanser til opprinnelige fakturaer i kreditnotaer
description: Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.
author: ilkond
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c1362bf41416202631dc4b966338e8166b26a67f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688353"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Referanser til opprinnelige fakturaer i kreditnotaer

[!include [banner](../includes/banner.md)]


I noen land og områder er det et juridisk krav at utskrevne kreditnotaer inkluderer referanser til de opprinnelige fakturaene. Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.

## <a name="prerequisites"></a>Forutsetninger

- I arbeidsområdet **Funksjonsbehandling** slår du på funksjonen for **Oppsett av fakturakreditering i salgs- og prosjektfakturarapporter**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- De utskriftsbare formatene for de nødvendige dokumentene må konfigureres i utskriftsbehandling.

Funksjonaliteten som er beskrevet i dette emnet, gjelder følgende dokumenter:

**Kunde**

- Fritekstkreditnota
- Kundekreditnota

**Prosjektstyring og regnskap**

- Prosjektkreditnota

## <a name="configure-accounts-receivable-parameters"></a>Konfigurere kundeparametre

Følg denne fremgangsmåten for å angi parameteren som styrer om referanser til de opprinnelige fakturaene skal skrives ut i relaterte kreditnotaer.

1. Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.
2. I kategorien **Oppdateringer**, i hurtigfanen **Faktura**, angir du alternativet **Bruk oppsettet for kreditering av fakturering i salgs- og prosjektfakturarapporter** til **Ja**.

![Konfigurere kundeparametre.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Definere referanser til opprinnelige fakturaer

Bruk følgende fremgangsmåter til å definere referanser til opprinnelige fakturaer basert på dokumenttypen.

### <a name="free-text-credit-note"></a>Fritekstkreditnota

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Opprett en ny kreditnota, eller velg en eksisterende kreditnota.
3. Åpne fakturaen.
4. I handlingsruten, på **Faktura**-fanen i **Funksjoner**-gruppen, velger du **Krediter fakturering**.
5. Angi referansen til den opprinnelige fakturaen, og velg årsaken til rettelsen.

![Definere referansen for en fritekstfaktura.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kundekreditnota

1. Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.
2. Velg og åpne den fakturerte salgsordren som må korrigeres.
3. I handlingsruten, på **Selg**-fanen i **Kreditnota**-gruppen, velger du **Kreditnota**.
4. Angi en årsak til korrigeringen. Referansen til den opprinnelige fakturaen opprettes automatisk.

![Definere referansen for en salgsordre.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Prosjektkreditnota

1. Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Prosjektfakturaer**.
2. Velg og åpne prosjektfakturaen som må korrigeres.
3. I handlingsruten, på **Prosjektfaktura**-fanen i **Funksjoner**-gruppen, velger du **Velg for kreditnota**.
4. Velg **Krediter fakturering**.
5. Angi en årsak til korrigeringen. Referansen til den opprinnelige fakturaen opprettes automatisk.

![Definere referansen for en prosjektfaktura.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Skrive ut kreditnotaer

Når du skriver ut kreditnotaer for fritekst, kunde og prosjekt, inneholder de referansen til den opprinnelige fakturaen og rettelsesårsaken.

![Utskrevet kreditnota.](media/credit-note-FTI.jpg)

> [!NOTE]
> Pass på at de utskriftsbare formatene til dokumentene er riktig konfigurert, under forutsetning av at referanser til opprinnelige fakturaer blir skrevet ut.

## <a name="references-to-original-invoices-in-debit-notes"></a>Referanser til opprinnelige fakturaer i debetnotaer

Som standard kan referanser til opprinnelige fakturaer angis for kreditnotaer. Du kan for eksempel angi referanser når du foretar negative (synkende) rettelser av opprinnelige fakturaer.

Hvis du vil angi referanser når du foretar positive (økende) rettelser av opprinnelige fakturaer, må du aktivere funksjonen **Referanser til opprinnelige fakturaer i debetnotaer** i arbeidsområdet for **Funksjonsbehandling**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
