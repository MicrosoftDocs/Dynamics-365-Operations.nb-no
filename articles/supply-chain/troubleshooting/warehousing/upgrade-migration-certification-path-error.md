---
title: Feil under sertifiseringsbane ved oppgradering eller migrering til WMS
description: Hvis appen viser feilen " Finner ikke klareringsanker for sertifiseringsbane" ved oppgradering eller migrering til WMS, gir denne siden informasjon om hvordan du retter problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477174"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Klareringsanker for sertifiseringsbane ble ikke funnet under oppdatering og overføring til WMS

## <a name="symptoms"></a>Symptomer

Når du oppgraderer og migrerer til til avansert lagerstyring (WMS), kan det hende at Warehouse Management-appen viser følgende feilmelding:

> java.security.cert.certPathValidatorException: Finner ikke klareringsanker for sertifiseringsbane.

## <a name="cause"></a>Årsak

Dette skjer fordi selvsignerte sertifikater ikke er klarert på Android 8+ i lokaler miljøer.

## <a name="resolution"></a>Løsning

Bruk en ekstern (offentlig) sertifiseringsinstans (CA). En hurtigreparasjon for dette problemet er tilgjengelig i versjon 1.9.0.0 av Warehouse Management-appen. Hvis du vil ha mer informasjon om dette problemet og hvordan du retter det, kan du se [Klareringsanker for sertifiseringsbane som ikke blir funnet ved konfigurasjon av apptilkobling](certification-path-app-connection-error.md).
