---
title: Angi parametere i Fordelsbehandling
description: Konfigurer parametere for Fordelsadministrasjon i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429994"
---
# <a name="set-benefits-management-parameters"></a>Angi parametere for fordelsbehandling

Før du kan definere permisjonsplaner i Microsoft Dynamics 365 Human Resources, må du konfigurere parametere for Fordelsadministrasjon. Disse parameterne angir standardverdier, årsakskoder og andre alternativer.

## <a name="configure-general-parameters"></a>Konfigurere generelle parametere

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.

2. I kategorien **Generelt** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Land/område** | Feltet **Land/område** bestemmer visningsrekkefølgen for postnumre/delstater. Det valgte landet vises først i rullegardinlisten. |
   | **Årsakskode for registrering** | Velg en standard årsakskode som skal brukes når det opprettes ansattplaner under åpen registreringsbehandling. |
   | **Årsakskode for avbrudd** | Årsakskoden som skal brukes når en ansattfordelsplan avbrytes. Den vises i en dialogboks under annulleringsprosessen. Brukerne kan endre **årsakskoden for annullering** om nødvendig. |
   | **Årsakskode for gjenåpning** | Årsakskoden som skal brukes når en ansattfordelsplan åpnes på nytt. Den vises i en dialogboks under annulleringsprosessen. Brukerne kan endre **årsakskoden for ny åpning** om nødvendig. | 
   | **Årsakskode for levetidshendelse** | Årsakskoden som skal brukes når en livshendelse inntreffer. |
   | **Årsakskode for satsendring** | Årsakskoden som skal brukes ved avbryting og nyåpning av en fordelsplan for ansatte i løpet av oppdateringsprosessen for frekvensendring. Det viser hvilke poster som ble endret av oppdateringsprosessen for frekvensendring. |
   | **Ny ansettelse kvalifisert** | Angir om nyansatte skal være berettiget. |
   | **Periode for registrering av ny ansettelse** | Tidsperioden når ny ansettelsesregistrering tillates.</br></br>**Obs!** Denne innstillingen overstyrer registreringsperioden for ny ansettelse som du angir i regelen for planrettigheter. | 
   | **Levetidshendelser aktivert** | Aktiverer livshendelser. |
   | **Skjul eldre fordelsskjemaer** | Lar deg skjule eldre fordelsskjemaer. |

3. Velg **Lagre**.

## <a name="configure-employee-self-service-parameters"></a>Konfigurere parametere for ansattselvbetjening

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Parametere**.

2. I kategorien **Ansattselvbetjening** angir du verdier for følgende felt:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Fordelsbekreftelse** | Bekreftelsesteksten som skal brukes i forbindelse med utsjekking av selvbetjeningsfordeler. |
   | **Velg utpekte personer automatisk** | Angir om avhengige og mottakere skal velges automatisk basert, på rettighetene for planalternativer. |

3. Velg **Lagre**.
