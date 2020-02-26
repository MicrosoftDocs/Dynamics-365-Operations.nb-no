---
title: Angi parametere i Fordelsbehandling
description: Konfigurer parametere for Fordelsadministrasjon i Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010079"
---
# <a name="set-benefits-management-parameters"></a>Angi parametere i Fordelsbehandling

[!include [banner](includes/preview-feature.md)]

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
   | **Årlig lønnsøkning** | Angir om beløpet for **Årlig fordel lønn** skal beregnes automatisk i **Fordelsdetaljer for ansatt**. Dette er basert på **Fast kompensasjonssats**, **Gjennomsnittlig timer** og **Betalingsfrekvens**.</br></br>**Gjennomsnittlig timer** x **Fast betalingssats** x **Betalingsfrekvens** (antall betalingsperioder) = **Årlig fordel lønn** </br></br>Hvis noen av verdiene i feltene **Gjennomsnittlig timer**, **Fast kompensasjonssats** eller **Betalingsfrekvens** endres, beregner systemet automatisk beløpet for **Årlig fordel lønn** på nytt for den ansatte basert på de endrede verdiene. Systemet oppretter en **Gyldig dato**-post for å identifisere nøyaktig dato og klokkeslett for når endringen ble utført. Du kan manuelt redigere beløpet for **Årlig fordel lønn** hvis det er nødvendig. |
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
