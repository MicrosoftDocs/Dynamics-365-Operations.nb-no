---
title: Feilsøke problemer knyttet til løsningsbevissthet
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f83a064bfc8896bdf76bcd38f9187ed0e1ea56cf
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062319"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Feilsøke problemer knyttet til løsningsbevissthet

[!include [banner](../../includes/banner.md)]





Dette emnet inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="error-on-the-dual-write-page"></a>Feil på siden Dobbel skriving

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*

Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Dataverse. Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]