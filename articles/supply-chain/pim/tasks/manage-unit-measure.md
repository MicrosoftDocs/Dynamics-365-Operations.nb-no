---
title: Administrere måleenhet
description: Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8d9b6f18fdc1c47d6a695ca6a2330f6f02fc1bd
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886998"
---
# <a name="manage-unit-of-measure"></a>Administrere måleenhet

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter. Du kan gå gjennom denne fremgangsmåten ved hjelp av demonstrasjonsdata eller ved hjelp av dine egne data.

1. Gå til **Navigasjonsrute > Moduler > Behandling av produktinformasjon > Vedlikehold av frigitt produkt**.
2. Klikk på **Enheter**.

## <a name="create-a-unit-of-measure"></a>Opprett en måleenhet
1. Klikk på **Ny**.
2. Skriv inn en verdi i feltet **Enhet**. Angi ID eller symbol som skal brukes ved referanse til måleenheten.  
3. Skriv inn en verdi i **Beskrivelse**-feltet. Angi et beskrivende navn for måleenheten på systemspråket.  
4. Velg et alternativ i feltet **Enhetsklasse**. Enhetsklassen definerer hvilken logisk gruppering, for eksempel område, masse eller antall, måleenheten er en del av.  
5. Angi et tall i feltet **Desimalpresisjon**. Angi antallet desimaler som den konverterte måleenheten må avrundes til når en beregning er fullført for måleenheten.  
6. Klikk **Lagre**.

## <a name="define-unit-translations"></a>Definer enhetsoversettelser
1. Gå til **handlingsruten**, og klikk på **Enhetstekster**.
2. Klikk på **Ny**. Bruk enhetsteksten til å opprette en oversettelse av ID-en eller et symbol som representerer måleenheten for bruk på eksterne dokumenter på kunde- eller leverandørspesifikke språk.  
3. Angi eller velg en verdi i feltet **Språk**.
4. Skriv inn en verdi i **Tekst**-feltet.
5. Klikk **Lagre**.
6. Lukk siden.
7. Gå til **handlingsruten**, og klikk på **Oversatte enhetsbeskrivelser**.
8. Klikk på **Ny**. Definer språkspesifikke beskrivelser for måleenheten.  
9. Angi eller velg en verdi i feltet **Språk**.
10. Skriv inn en verdi i **Beskrivelse**-feltet.
11. Klikk **Lagre**.
12. Lukk siden.

## <a name="define-unit-conversion-rules"></a>Definer enhetsomregningsregler
1. Gå til **handlingsruten**, og klikk på **Enhetsomregninger**. Definere regler for å konvertere måleenheten til og fra andre enheter i den valgte enhetsklassen.  
2. Klikk på **Ny** for å åpne nedtrekksdialogen.
3. Angi et tall i feltet **Faktor**. Omregningsfaktor mellom fra-enheten og til-enheten. Omregningsfaktoren fra centimeter til meter er for eksempel 100, fordi det er 100 centimeter i én meter.  
4. Angi eller velg en verdi i feltet **Til enhet**.
5. Velg et alternativ i feltet **Avrunding**. Definer hvordan den omregnede verdien skal avrundes.  
6. Klikk **OK**.
7. Lukk siden.

