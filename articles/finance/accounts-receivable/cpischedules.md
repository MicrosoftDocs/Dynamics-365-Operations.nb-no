---
title: Tidsplan for konsumprisindeks
description: Dette emnet beskriver hvordan du oppretter listen over CPI-planer (Consumer Price Index – konsumprisindeks) som du henter fra Internett for å bidra til å fastslå eskaleringstillegget i abonnementsfakturering.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 54114fae25565ed1aae7056ef9be5a4a159291e9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686526"
---
# <a name="consumer-price-index-schedule"></a>Tidsplan for konsumprisindeks

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du oppretter, sletter, går gjennom og behandler CPI-planer (konsumprisindeks). En CPI-plan kan brukes til å fastslå prisene for forbruksvarer og -tjenester som du legger til som fakturaplanlinjer. CPI-planen kan deretter brukes med eskalerings- og rabattpriser i en faktureringsplan, eller den kan behandles manuelt for å oppdatere fakturabeløpene i faktureringsplaner. Du kan angi CPI-planer manuelt, eller du kan importere dem ved å bruke den sammensatte enheten for CPI-plan.

Hvis du vil legge til en CPI-plan, følger du disse trinnene.

1. Velg **Ny** på siden **Konsumprisindeks**.
2. Skriv inn et unikt navn i feltet **Tidsplan for konsumprisindeks**.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. Velg **Legg til** på fanen **Konsumprisindeks**.
5. I feltet **Dato for konsumprisindeks** angir du datoen når den nye CPI-planen blir aktiv.
6. I feltet **Tidsplan for konsumprisindeks** skriver du inn navnet du skrev inn i trinn 2.
7. Velg **Lagre**.

Hvis du vil slette en dato for en CPI-plan, følger du trinnene nedenfor.

1. På siden **Tidsplan for konsumprisindeks** velger du en flere linjer du vil slette, og deretter velger du **Fjern**.
2. Hvis du vil slette hele CPI-planen, velger du **Slett** i handlingsruten. Du kan ikke slette den valgte CPI-planen hvis den er knyttet til en faktureringsplan.
3. I handlingsruten velger du **Behandle** for å oppdatere faktureringsplanene som bruker den valgte CPI-planen. De siste CPI-datoene og tidsplanbeløpene vil bli brukt til å oppdatere faktureringsplanprisene.
4. På hurtigfanen **Behandle konsumprisindeks** går du gjennom de oppdaterte feltene **Faktureringsplannummer**, **Varenummer**, **Startdato for fakturering**, **Sluttdato for fakturering**, **Eskaleringsdato** og **Eskaleringsfrekvens**.

Når CPI-planer er definert, kan de brukes til eskalering og endringer av rabattpriser i fakturaplaner.

## <a name="cpi-calculation"></a>CPI-beregning

For disse eksemplene er perioden fra 1. januar 2020 til 31. desember 2022. CPI-basissatsen (CPI-verdien når kontrakten starter) er 105,65. 1. januar 2021 er gjeldende CPI 110,5. 1. januar 2022 er gjeldende CPI 114,25. Det opprinnelige beløpet er USD 1000.

**Eksempel 1**

På siden **Parametere for gjentakende kontraktfakturering** angir du feltet **Beregning av konsumprisindeks** til **Basisforbrukerprisindeks**.

For perioden 1. januar 2021 beregnes det første eskaleringsbeløpet på følgende måte, basert på det opprinnelige beløpet:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1045,91

For perioden 1. januar 2022 beregnes eskaleringsbeløpet på følgende måte:

1000 + (114,25 – 105,65) &divide; 105,65 &times; 1000 = 1081,40

**Eksempel 2**

På siden **Parametere for gjentakende kontraktfakturering** angir du feltet **Beregning av konsumprisindeks** til **Tidligere forbrukerprisindeks**.

For perioden 1. januar 2021 beregnes det første eskaleringsbeløpet på følgende måte, basert på det opprinnelige beløpet:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1045,91

For perioden 1. januar 2022 beregnes eskaleringsbeløpet på følgende måte, basert på det første eksaleringsbeløpet:

1045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1045,91 = 1081,40

> [!NOTE]
> Eskaleringsprosessen bruker alltid den siste CPI-verdien, uansett indeksdato. Hvis for eksempel eskaleringen er i september, men den siste CPI-verdien er for juli, brukes indeksen for juli. Det gjøres ingen justeringer etter at indeksen for september er angitt.

## <a name="prorated-escalation"></a>Fordelt eskalering

Hvis eskaleringen skjer midt i en faktureringsperiode, blir beløpet fordelt. Faktureringsperioden er for eksempel fra 1. august 2020 til 31. juli 2021. På CPI-datoen 1. september 2019 er CPI-verdien 244. På CPI-datoen 1. september 2020 er denne CPI-verdien 250. Hvis den forrige satsen er 1000, brukes følgende formler til å beregne faktureringsbeløpet for perioden:

* *CPI-endringer* = (250 – 244) &divide; 244 = 2,459 %
* *Gjeldende sats* = 1000 &times; 2,459 % = 1024,59
* *Antall dager med gjeldende sats* = 31. juli 2021 – 1. september 2020 = 334
* *Forrige sats* = 1000
* *Antall dager med forrige sats* = 31. august 2020 – 1. august 2020 = 31
* *Totalt antall dager i faktureringsperioden* = 31. juli 2021 – 1. august 2020 + 1 = 365
* *Faktureringsbeløp for denne perioden* = (1000 &times; 31 &divide; 365) + (1024,59 &times; 334 &divide; 365) = 1022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Eskalering som bruker CPI og prosent

Eskaleringer kan utføres ved hjelp av CPI. CPI pluss en 3-prosents eskalering starter 1. januar 2020, og den har en årlig frekvens.

- Beløpet som faktureres for 1. januar 2019 til og med 31. desember 2020, er 4000.
- Faktureringsperioden som skal eskaleres, er fra 1. januar 2020 til og med 31. desember 2020.
- På CPI-datoen 1. desember 2018 er CPI-verdien 205,3. På CPI-datoen 1. desember 2019 er CPI-verdien 219,6.

Hvis den forrige satsen er 4000, beregnes faktureringsbeløpet for denne perioden på følgende måte:

- *CPI-endringer* = (219,6 – 205,3) &divide; 205,3 = 6,965 %
- *Gjeldende sats* = (4000 &times; 6,965 %) – 4000 = 278,60
- *Endringer i prosent* = (4000 &times; 1,03) – 4000 = 120
- *Faktureringsbeløp* = 4000 + 278,6 + 120 = 4398,6
