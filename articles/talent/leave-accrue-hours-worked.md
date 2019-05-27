---
title: Avsette fridager basert på arbeidstimer
description: Dette emnet beskriver hvordan permisjonsplaner kan konfigureres for å avsette fridager basert på arbeidstimer.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8589527f75f48c16244c93c3fdbe3ce7fcd4e366
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518729"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Avsette fridager basert på arbeidstimer

[!include [banner](includes/banner.md)]


## <a name="overview"></a>Oversikt

Organisasjoner med timebaserte ansatte kan belønne dem med fridager basert på antall arbeidstimer i stedet for ansiennitet i organisasjonen. Data om arbeidstimer lagres vanligvis i et system for tid og fremmøte. I Talent: Core HR, vanlige og overtidstimer kan importeres og brukes som grunnlag for en ansatts belønning.

## <a name="leave-plans"></a>Permisjonsplaner

I permisjonsplanen kan avsetningstypen enten være måneder i tjeneste eller arbeidstimer. Når arbeidstimer er valgt, finnes det to typer timer skal brukes for avsetningen: vanlig og overtid.

Hvis du vil definere en permisjonsplanen som skal arbeidstimer, gjør du følgende:

1. På siden **Permisjons- og fraværsplaner** klikker du **Opprett ny plan**.
2. Angi et navn for permisjonsplanen.
3. Velg avsetningshyppigheten for planen.
5. Velg startdatoen for planen.
6. Velg periodegrunnlaget for avsetningen, og velg den ansattspesifikke datoen, hvis det er aktuelt.
7. For avsetningsplanen velger du **Arbeidstimer** for avsetningstypen.
8. Velg typen timer som skal brukes for avsetningen.
9. Angi antall arbeidstimer og det tilknyttede avsetningsbeløpet, minimumssaldo og maksimum overføring eller tilskuddsbeløp.

Avsetningsbehandling for planer av arbeidstimer bruker avsetningsfrekvensen, sammen med periodebasisen, til å bestemme timene som skal avsettes.

## <a name="annual-accrual-frequency"></a>Årlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2085                | 144                 |        
| 31/12/2018            | 2080                 | 144                   | 1/1/2018-12/31/2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Månedlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 160                  | 12                    | 8/1/2018-8/31/2018   | 184                 | 12                  |        
| 31/8/2018             | 160                  | 3                     | 8/1/2018-8/31/2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Avsetningsfrekvens annenhver måned

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 81                  | 6                  |        
| 31/8/2018             | 80                   | 6                     | 8/16/2018-8/31/2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Ukentlig avsetningsfrekvens

| Belønningsdato for avsetning    | Arbeidstimernivå    | Avsetningsbeløp        | Arbeidstimer datoer   | Arbeidstimer faktisk| Belønning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31/8/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 42                  | 3                  |        
| 31/8/2018             | 40                   | 3                     | 8/27/2018-8/31/2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Tilordnede permisjonsplaner for ansatte

I den ansattes tilordnede permisjonsplaner vises nivågrunnlaget og typen timer for planer der arbeidstimer er definert som avsetningstypen. For aktive planer vises de faktiske arbeidstimene for avsetningsperiodene per gjeldende dato også for referanse. 

## <a name="loading-data"></a>Laster inn data

Faktiske timer kan importeres ved hjelp av enheten Antall arbeidstimer for permisjon og fravær i databehandling. Hvis du bruker arbeidstidskalendre, validerer importen at normaltimer som er utført, ikke overstiger de planlagte timene på en dag definert av kalenderen. Importen validerer også at antallet arbeidstimer for en gitt dag ikke overskrider 24 timer. 

Følgende informasjon er nødvendig for å importere faktisk antall timer som skal brukes i denne avsetningsprosessen for permisjon:

+ Personalnummer 
+ Arbeidsdag
+ Type
+ Timeantall

En enkelt dato kan bare ha én av hver type knyttet til seg.

| PERSONALNUMMER       | ARBEIDSDAG           | TYPE                  | TIMER                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6/8/2018             | Vanlig               | 8                    |       
| 000337                | 7/8/2018             | Vanlig               | 8                    |
| 000337                | 7/8/2018             | Overtid              | 3                    |
| 000337                | 8/8/2018             | Vanlig               | 8                    |
| 000337                | 7/8/2018             | Vanlig               | 8                    |
| 000337                | 9/8/2018             | Vanlig               | 8                    |
