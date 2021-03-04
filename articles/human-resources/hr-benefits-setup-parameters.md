---
title: Angi parametere for Fordelsbehandling og Ansattselvbetjening for alle firmaer
description: Konfigurer parametere Fordelsbehandling og Ansattselvbetjening i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692703"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Angi parametere for Fordelsbehandling og Ansattselvbetjening for alle firmaer

Før du kan definere fordelsplaner i Microsoft Dynamics 365 Human Resources, må du konfigurere parametere for Fordelsadministrasjon. Disse parameterne angir standardverdier, årsakskoder og andre alternativer. 

## <a name="configure-general-parameters"></a>Konfigurere generelle parametere

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Delte parametere for personaladministrasjon**.

2. I kategorien **Fordelsbehandling** angir du verdier for følgende felt:

   | Felt | beskrivelse |
   | --- | --- |
   | **Land/område** | Feltet **Land/område** bestemmer visningsrekkefølgen for postnumre/delstater. Det valgte landet vises først i rullegardinlisten. |
   | **Årsakskode for registrering** | Velg en standard årsakskode som skal brukes når det opprettes ansattplaner under åpen registreringsbehandling. |
   | **Årsakskode for avbrudd** | Årsakskoden som skal brukes når en ansattfordelsplan avbrytes. Den vises i en dialogboks under annulleringsprosessen. Brukerne kan endre **årsakskoden for annullering** om nødvendig. |
   | **Årsakskode for gjenåpning** | Årsakskoden som skal brukes når en ansattfordelsplan åpnes på nytt. Den vises i en dialogboks under annulleringsprosessen. Brukerne kan endre **årsakskoden for ny åpning** om nødvendig. | 
   | **Årsakskode for levetidshendelse** | Årsakskoden som skal brukes når en livshendelse inntreffer. |
   | **Årsakskode for satsendring** | Årsakskoden som skal brukes ved avbryting og nyåpning av en fordelsplan for ansatte i løpet av oppdateringsprosessen for frekvensendring. Det viser hvilke poster som ble endret av oppdateringsprosessen for frekvensendring. |
   | **Årlig fordelslønn** | Gir deg muligheten til å angi et **årlig lønnsbeløp for fordeler** for en ansatt. Human Resources bruker **årlig lønnsbeløp for fordeler** når de fastsetter dekningsbeløp i stedet for det årlige beløpet for fast kompensasjonen. |
   | **Ny ansettelse kvalifisert** | Angir om nyansatte skal være berettiget. |
   | **Periode for registrering av ny ansettelse** | Tidsperioden når ny ansettelsesregistrering tillates.</br></br>**Obs!** Denne innstillingen overstyrer registreringsperioden for ny ansettelse som du angir i regelen for planrettigheter. |
   | **Standard lønnsfrekvens** | Standard betalingsfrekvensen som skal brukes når nye arbeidere legges til. |
   | **Levetidshendelser aktivert** | Aktiverer livshendelser. |
   | **Skjul eldre fordelsskjemaer** | Lar deg skjule eldre fordelsskjemaer. |
   | **Fordelsbekreftelse** | Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler. |
   | **Velg utpekte personer automatisk** | Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer. |

3. Velg **Lagre**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurere parametere for ansattselvbetjening

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere for Human Resources**.

2. I kategorien **Fordelsbehandling** angir du verdier for følgende felt:

   | Felt | beskrivelse |
   | --- | --- |
   | **Fordelsbekreftelse** | Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler. |
   | **Velg utpekte personer automatisk** | Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer. |

3. Velg **Lagre**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]