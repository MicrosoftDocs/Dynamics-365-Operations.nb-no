---
title: Feilsøke problemer knyttet til løsningsbevissthet
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b53e07f69992a567d5b300ae1f2b24b74541d176
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416358"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Feilsøke problemer knyttet til løsningsbevissthet

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="error-on-the-dual-write-page"></a>Feil på siden Dobbel skriving

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*

Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Dataverse. Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]