---
title: Feilsøk problemer i forbindelse med forståelse av løsningen
description: Denne artikkelen inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c70287cb8ec29fb622f3aefff971b884339e4205
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289432"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Feilsøk problemer i forbindelse med forståelse av løsningen

[!include [banner](../../includes/banner.md)]





Denne artikkelen inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.

> [!IMPORTANT]
> Noen av problemene som denne artikkelen løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="error-on-the-dual-write-page"></a>Feil på siden Dobbel skriving

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*

Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Dataverse. Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
