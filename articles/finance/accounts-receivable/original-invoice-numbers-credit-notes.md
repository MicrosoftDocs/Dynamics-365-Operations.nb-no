---
title: Referanser til opprinnelige fakturaer i kreditnotaer
description: Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811516"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Referanser til opprinnelige fakturaer i kreditnotaer

[!include [banner](../includes/banner.md)]


I noen land og områder er det et juridisk krav at utskrevne kreditnotaer inkluderer referanser til de opprinnelige fakturaene. Dette emnet beskriver hvordan du definerer og skriver ut de opprinnelige fakturanumrene i tilknyttede kreditnotaer.

## <a name="prerequisites"></a>Forutsetninger

- I arbeidsområdet **Funksjonsbehandling** slår du på funksjonen for **Oppsett av fakturakreditering i salgs- og prosjektfakturarapporter**. Hvis du vil ha mer informasjon, kan du se [Oversikt over funksjonsbehandling](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
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

![Konfigurere kundeparametre](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Definere referanser til opprinnelige fakturaer

Bruk følgende fremgangsmåter til å definere referanser til opprinnelige fakturaer basert på dokumenttypen.

### <a name="free-text-credit-note"></a>Fritekstkreditnota

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Opprett en ny kreditnota, eller velg en eksisterende kreditnota.
3. Åpne fakturaen.
4. I handlingsruten, på **Faktura**-fanen i **Funksjoner**-gruppen, velger du **Krediter fakturering**.
5. Angi referansen til den opprinnelige fakturaen, og velg årsaken til rettelsen.

![Definere referansen for en fritekstfaktura](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kundekreditnota

1. Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.
2. Velg og åpne den fakturerte salgsordren som må korrigeres.
3. I handlingsruten, på **Selg**-fanen i **Kreditnota**-gruppen, velger du **Kreditnota**.
4. Angi en årsak til korrigeringen. Referansen til den opprinnelige fakturaen opprettes automatisk.

![Definere referansen for en salgsordre](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Prosjektkreditnota

1. Gå til **Prosjektstyring og regnskap** \> **Prosjektfakturaer** \> **Prosjektfakturaer**.
2. Velg og åpne prosjektfakturaen som må korrigeres.
3. I handlingsruten, på **Prosjektfaktura**-fanen i **Funksjoner**-gruppen, velger du **Velg for kreditnota**.
4. Velg **Krediter fakturering**.
5. Angi en årsak til korrigeringen. Referansen til den opprinnelige fakturaen opprettes automatisk.

![Definere referansen for en prosjektfaktura](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Skrive ut kreditnotaer

Når du skriver ut kreditnotaer for fritekst, kunde og prosjekt, inneholder de referansen til den opprinnelige fakturaen og rettelsesårsaken.

![Utskrevet kreditnota](media/credit-note-FTI.jpg)

> [!NOTE]
> Pass på at de utskriftsbare formatene til dokumentene er riktig konfigurert, under forutsetning av at referanser til opprinnelige fakturaer blir skrevet ut.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
