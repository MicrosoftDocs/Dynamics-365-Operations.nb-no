---
title: Opprette en modulær permisjon
description: Denne artikkelen beskriver hvordan du oppretter en modulær permisjon i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805344"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Opprette en modulær permisjon

> [!IMPORTANT]
> Funksjonaliteten som beskrives i denne artikkelenm, vil være tilgjengelig i Finance-infrastrukturen som en del av en fremtidig utgivelse etter Microsoft Dynamics 365 Finance versjon 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan sende forespørsler om modulære permisjoner og se statusen på forespørslene i Dynamics 365 Human Resources.

## <a name="prerequisites"></a>Forutsetninger

1. Under **Funksjonsstyring** kontrollerer du at funksjonen **Åpen permisjon** er aktivert.

    > [!IMPORTANT]
    > Denne funksjonen er aktivert, kan den ikke deaktiveres.

2. Opprett fraværspermisjonstype.
3. Angi detaljer som permisjonstype, beskrivelse og arbeidsflyt-ID.
4. Velg **Fravær** i **Forespørselstype**-feltet .
5. I detaljer-delen angir du **Modulær** til **Ja**.
6. Angi alternativet **Varsel om retur til arbeid** til **Ja** eller **Nei**.
7. Du kan velge om du vil ha et varsel om retur til arbeid for åpne permisjoner for fravær.

> [!NOTE]
> Når denne funksjonen er aktivert vil funksjonen **Vedlegg kreves** være aktivert.

## <a name="request-an-open-ended-leave-of-absence"></a>Forespørre en modulær permisjon

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mer** (...) på flisen **Saldoer for fridager**.
2. For å sende en permisjonsforespørsel velger du **Be om permisjon**.
3. Angi informasjon i feltene **Permisjonstype** og **Startdato**. Angi foreløpig sluttdato i feltet **Sluttdato**.
4. Hvis må sende inn støttedokumentasjon, velger du **Last opp** under **Vedlegg**.
5. Velg **Send inn** hvis du er klar til å sende inn forespørselen. Ellers velger du **Lagre utkast**.
6. Hvis du vil oppdatere en åpen permisjonsforespørsel, velger du forespørselen, angir en sluttdato i **Sluttdato**-feltet, angir **Bekreft sluttdato** til **Ja** og laster opp dokumentasjon.
7. Hvis alternativet **Varsel om retur til arbeid** er satt til **Ja**, velger du **Last opp**, og deretter merker du av for å bekrefte at en gyldig retur-til-arbeid-melding er lastet opp.
8. Når alle detaljene er angitt, velger du **Send**.
