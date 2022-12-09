---
title: Be om permisjon
description: Send en permisjonsforespørsel.
author: twheeloc
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveofAbsenceRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6c98246e94670dd5f882fcbbd1f269e57f66faf
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805294"
---
# <a name="request-a-leave-of-absence"></a>Be om permisjon

>[!Important]
>Funksjonaliteten som er nevnt i denne artikkelen, er for øyeblikket tilgjengelig for kunder i frittstående Dynamics 365 Human Resources. Noe av eller all funksjonaliteten vil være tilgjengelig som en del av en fremtidig versjon av Finance-infrastrukturen etter Finance versjon 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Du kan sende en permisjonsforespørsel og se statusen på forespørslene i Dynamics 365 Human Resources.

## <a name="request-a-leave-of-absence"></a>Be om permisjon

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mer** (...) på flisen **Avspaseringssaldoer**.

2. For å sende en permisjonsforespørsel velger du **Be om permisjon**.

3. Angi informasjon for **Permisjonstype**, **Startdato** og **Sluttdato**.

4. Hvis du må sende inn en eventuell støttedokumentasjon, velger du **Last opp** under **Vedlegg**.

5. Legg om nødvendig inn informasjon under **Kommentar**.

6. Velg **Send inn** når du er klar til å sende inn forespørselen. Ellers velger du **Lagre utkast**.


## <a name="view-leave-of-absence-request-status"></a>Vis status for permisjonsforespørsel

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mer** (...) på flisen **Avspaseringssaldoer**.

2. For å se permisjonsforespørslene dine velger du **Se permisjon**.

## <a name="update-a-leave-of-absence-request"></a>Oppdatere en permisjonsforespørsel

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mer (...)** på flisen **Permisjon**.
2. Velg fraværsforespørselen som skal oppdateres, og velg deretter **Oppdatert permisjon**.
3. Oppdater verdien i feltet **Sluttdato** etter behov for å forlenge eller forkorte fraværet.
4. Hvis sluttdatoen er bekreftet, setter du alternativet **Bekreft sluttdato** til **Ja**.
5. Når alternativet **Bekreft sluttdato** er satt til **Ja**, kan du laste opp et varsel om retur til arbeid. Merk deretter av for å bekrefte at en retur til-arbeid-melding er lastet opp.
6. Velg **Send** for å oppdatere fraværsforespørselen.

## <a name="cancel-a-leave-of-absence-request"></a>Avbryte en permisjonsforespørsel

1. I arbeidsområdet **Ansattselvbetjening** velger du **Mer (...)** på flisen **Permisjon**.
2. Velg fraværsforespørselen som skal avbrytes, og velg deretter **Oppdatert permisjon**.
3. Sett alternativet **Avbryt permisjon** til **Ja**.
4. Velg **Send** for å avbryte fraværsforespørselen.

## <a name="importing-leave-requests-from-other-systems-or-older-systems"></a>Importere permisjonsforespørsler fra andre systemer eller eldre systemer

Hvis du vil importere permisjonsforespørsler fra et annet system, må du gå gjennom den vanlige arbeidsflyten for å opprette de aktuelle permisjonstransaksjonene. Du kan også importere permisjonsbanktransaksjonene og permisjonsforespørsler i en fullført tilstand. Legg merke til at det ikke opprettes automatisk permisjonstransaksjoner hvis du bare importerer permisjonsforespørsler.

## <a name="see-also"></a>Se også

[Suspender permisjon](hr-leave-and-absence-suspend-leave.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
