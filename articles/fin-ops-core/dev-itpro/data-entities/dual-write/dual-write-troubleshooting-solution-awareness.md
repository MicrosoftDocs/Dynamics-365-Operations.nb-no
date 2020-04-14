---
title: Feilsøke problemer knyttet til løsningsbevissthet
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172627"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Feilsøke problemer knyttet til løsningsbevissthet

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til løsningsbevissthet.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="error-on-the-dual-write-page"></a>Feil på siden Dobbel skriving

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Finner ikke enheten med\_navnet msdyn dualwriteentitymap med namemapping='Logisk i MetadataCache.*

Hvis du vil løse problemet, må du kontrollere at kjerneløsningen for dobbel skriving er installert i Common Data Service. Kjernløsningen for dobbel skriving er en forutsetning for løsningsbevissthet.
