---
title: Administrere måleenheter
description: Dette emnet beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d251f90675188426e74b8cbe672856eb4c9ecb8a391f54e735ba19b91b7e3f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746945"
---
# <a name="manage-units-of-measure"></a>Administrere måleenheter

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du definerer en målenhet, angir oversettelser for enheten og beskrivelsen og definerer omregningsreglene for relaterte enheter.

## <a name="open-the-units-page"></a>Åpne Enheter-siden

Hvis du vil opprette og arbeide med måleenhetene som er tilgjengelige i systemet, kan du gå til **Organisasjonsstyring \> Oppsett \> Enheter \> Enheter**.

Resten av delene i dette emnet beskriver hva du kan gjøre på **Enheter**-siden.

## <a name="create-standard-units-and-conversions"></a>Opprette standardenheter og konverteringer

Hvis systemet ikke allerede inneholder de mest vanlige måleenhetene for det metriske systemet og/eller det amerikanske målesystemet (USCS), kan installasjonsveiviseren hjelpe deg med å komme raskt i gang med grunnleggende enhetsdefinisjoner og konverteringer. Hvis du vil fullføre veiviseren, velger du **veiviseren for enhetsopprettelse** i handlingsruten, og deretter følger du instruksjonene på skjermen.

## <a name="create-or-edit-a-unit-of-measure"></a>Opprette eller redigere en måleenhet

Følg denne fremgangsmåten for å opprette eller redigere en måleenhet.

1. Følg ett av disse trinnene:

    - Hvis du vil redigere en eksisterende enhet, velger du den i listeruten.
    - For å opprette en ny enhet velger du **Ny** i handlingsruten.

1. I toppteksten for den nye posten angir du følgende felt:

    - **Enhet** – Angi IDen eller symbolet som skal brukes for å referere til enheten på systemspråket. IDen eller symbolet er vanligvis en felles forkortelse for enheten, for eksempel *hv* for hver eller *cm* for centimeter.
    - **Beskrivelse** – Angi et beskrivende navn for måleenheten på systemspråket. Dette navnet er vanligvis hele navnet på enheten, for eksempel *Hver* eller *Centimeter*.

1. Angi følgende felt i hurtigfanen **Generelt**:<!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - **Enhetsklasse** – Velg egenskapen som enheten måler (for eksempel lengde, område, masse eller antall).
    - **Enhetssystem** – Velg målingssystemet som enheten tilhører (*Metriske enheter* eller *Amerikanske måleenheter*).
    - **Basisenhet** – Sett dette alternativet til *Ja* for å bruke gjeldende enhet som basisenhet for enhetsklassen. I dette tilfellet må du bare angi omregningsfaktoren mellom basisenheten og hver tilleggsenhet i enhetsklassen. Systemet kan deretter konvertere mellom alle enheter i denne enhetsklassen. Det er derfor enklere å konfigurere konverteringer.

        Hvis for eksempel gallon er basisenheten for *Volum*-enhetsklassen, trenger du bare å angi omregningsfaktorer fra quart til gallon og fra pint til gallon. Systemet kan deretter også konvertere fra quart til pint.

        Du kan bare ha én basisenhet per enhetsklasse.

    - **Systemenhet** – Sett dette alternativet til *Ja* for å bruke gjeldende enhet som antatt enhet for alle uspesifiserte målinger i enhetsklassen. Hvis for eksempel et felt som brukes til å angi et antall, ikke tillater at det angis en enhet (hvis brukeren ikke velger en enhet), bruker systemet enheten som er angitt som systemenhet for *Antall*-enhetsklassen. Du kan bare ha én systemenhet per enhetsklasse.
    - **Desimalpresisjon** – Angi antall desimaler som verdier som er angitt for den gjeldende enheten eller konverteres til den, skal avrundes til.

1. Velg **Lagre** i handlingsruten.

## <a name="define-unit-translations"></a>Definer enhetsoversettelser

Følg denne fremgangsmåten for å definere oversettelser for IDen eller symbolet og beskrivelsen av en måleenhet.

1. Opprett eller velg enheten du vil opprette oversettelser for.
1. I handlingsruten velger du **Enhetstekster**.

    Siden **Enhetstekster** vises. Du bruker denne siden til å definere oversettelser for IDen eller symbolet for den valgte enheten. Disse oversettelsene kan deretter brukes på eksterne dokumenter på kundespesifikke eller leverandørspesifikke språk.

1. Velg **Ny** i handlingsruten.
1. I **Språk**-feltet velger du språket som enhets-IDen eller symbolet skal oversettes til.
1. I **Tekst**-feltet angir du oversettelsen av enhets-IDen eller symbolet på det valgte språket.
1. Velg **Lagre** i handlingsruten.
1. Lukk siden.
1. Gå til **Handlingsrute**, velg **Oversatte enhetsbeskrivelser**.

    Siden **Oversatte enhetsbeskrivelser** vises. Du bruker denne siden til å definere språkspesifikke beskrivelser for den valgte enheten.

1. Velg **Ny** i handlingsruten.
1. I **Språk**-feltet velger du språket som enhetsbeskrivelsen skal oversettes til.
1. I **Beskrivelse**-feltet angir du oversettelsen av enhetsbeskrivelsen på det valgte språket.
1. Velg **Lagre** i handlingsruten.
1. Lukk siden.

## <a name="define-unit-conversion-rules"></a>Definer enhetsomregningsregler

Følg denne fremgangsmåten for å definere regler for omregninger mellom måleenheter.

1. Opprett eller velg enheten du vil definere omregningsregler for.
1. I handlingsruten velger du **Enhetskonverteringer**.

    Siden **Enhetskonverteringer** vises. Du kan bruke denne siden til å definere regler for å konvertere måleenheten til og fra andre enheter i den valgte enhetsklassen.

1. Velg én av følgende kategorier, avhengig av hvilken type konvertering du vil definere:

    - **Standardkonverteringer** – Definer standard konverteringsregler for alle produkter.
    - **Klasseinterne konverteringer** – Definer produktspesifikke omregningsregler for enheter i samme enhetsklasse.
    - **Mellomklassekonverteringer** – Definer produktspesifikke omregningsregler for enheter på tvers av enhetsklasser.

1. Følg ett av disse trinnene:

    - For å opprette en ny konvertering velger du **Ny** på verktøylinjen.
    - Hvis du vil redigere en eksisterende konvertering, velger du konverteringen i rutenettet og velger deretter **Rediger** på verktøylinjen.

1. I rullegardinboksen som vises, angir du følgende felt:

    - **Produkt** – Velg det spesifikke produktet som omregningen gjelder. Dette feltet er bare tilgjengelig for klasseinterne konverteringer og mellomklassekonverteringer.
    - **Formeloppsett** – La dette feltet være satt til *Enkel* for å angi en enkel konvertering som har én enkelt faktor. Sett den til *Avansert* for å definere en mer kompleks ligning. Formatet for avanserte ligninger varierer, avhengig av enhetsklassen.
    - **Fra enhet** – Dette feltet viser den valgte enheten. Vanligvis bør du ikke endre verdien. (Hvis du endrer verdien, må du åpne siden **Enhetsomregninger** for den valgte enheten for å vise den nye omregningen etter at du har lagret den.)
    - **Til enhet** – Velg enheten du vil konvertere til.
    - **Avrunding** – Velg hvordan brøker skal avrundes basert på **Desimalpresisjon**-verdien til den valgte enheten (*Til nærmeste*, *Opp* eller *Ned*).
    - **Konverteringsformel** – Bruk de gjenværende feltene øverst i rullegardinlisten til å angi formelen for omregning mellom de to enhetene. De tilgjengelige feltene varierer avhengig av enhetsklassen og formeloppsettet du har valgt.

1. Velg **OK**.
1. Lukk siden.

> [!TIP]
> Du kan også definere enhetsomregninger per produktvariant. Hvis du vil ha mer informasjon, kan du se [Konvertering av måleenhet per produktvariant](../uom-conversion-per-product-variant.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
