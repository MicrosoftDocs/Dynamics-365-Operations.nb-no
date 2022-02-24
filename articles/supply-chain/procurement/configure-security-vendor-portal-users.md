---
title: Brukersikkerhet for leverandørportal
description: Denne artikkelen forklarer hvordan du konfigurerer sikkerhet for eksterne leverandører som bruker leverandørportalen. Denne informasjonen i dette emnet gjelder bare for februar 2016- og mai 2016-versjonene av Dynamics AX.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be210728a6d5fa9a26daf9f13865ff08de03d2d
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018194"
---
# <a name="vendor-portal-user-security"></a>Brukersikkerhet for leverandørportal

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer sikkerhet for eksterne leverandører som bruker leverandørportalen. Denne informasjonen i dette emnet gjelder bare for februar 2016- og mai 2016-versjonene av Dynamics AX.

Funksjonen for leverandørportal er erstattet med utvidede leverandørsamarbeidsfunksjoner i Dynamics 365 for Operations versjon 1611. Hvis du vil ha mer informasjon om hvordan du konfigurerer sikkerhet for leverandørsamarbeid, kan du se [Konfigurere og vedlikehold leverandørsamarbeid](set-up-maintain-vendor-collaboration.md). Leverandørportalen viser et begrenset sett med informasjon om bestillinger for eksterne leverandører. Det er viktig at du riktig definerer brukertillatelser for leverandørportalen i Microsoft Dynamics AX, slik at leverandører ikke får utilsiktet tilgang til mer informasjon i Dynamics AX-installasjonen. **Viktig:** i motsetning til andre brukere, skal ikke eksterne leverandører rollen **SystemUser**. Rollen **SystemUser** gir tilgang til et sett med rettigheter som ikke er egnet for eksterne brukere.

## <a name="setting-up-a-vendor-portal-user"></a>Definere leverandørportalbruker
Før du oppretter en brukerkonto for en person som skal bruke leverandørportalen, må du definere leverandøren for å tillate leverandørportalsamarbeid. Bruk feltet **Bestillingssamarbeid** i **Generelt** fanen på **Leverandører** siden. Eksterne leverandører som bruker leverandørportalen må ha følgende oppsett:

-   En brukerkonto for Microsoft Azure Active Directory (AAD) må være registrert for leverandøren på **Brukere**-siden i Dynamics AX.
-   Leverandøren må ha **Leverandør (ekstern)** sikkerhetsrollen, ikke **SystemUser** rollen. **Obs!** Rollen **SystemUser** tildeles automatisk når du oppretter en ny brukerkonto i Dynamics AX. Derfor må du fjerne denne rollen og bekrefte advarselsmeldingen som du mottar.
-   Leverandørbrukeren må ikke gis tillatelse til å legge til flere felt fra bestillingstabellene i visningen av Bestillingen. På **Tilpassing** fanen, i **Brukere** fanen, angir du **Eksplisitt tilpasning tillatt** alternativet for brukeren som **Nei**.
-   Brukerkontoen må være tilknyttet en registrert kontaktperson. På siden **Brukere** velger du en kontaktperson i **Navn** feltet. Personen som du velger, skal ha **Kontakt**-rollen for den aktuelle leverandøren.

Hvis samme person krever tilgang til leverandørportalen for flere leverandørkontoer (for ulike juridiske enheter, kanskje), må hver av denne personens kontoer være tilknyttet samme registrerte kontaktperson. Rollen **Leverandør (ekstern)** inneholder alle de grunnleggende funksjonene som kreves for å bruke funksjonene som er tilgjengelig i leverandørportalen. Dette oppsettet hjelper med å garantere at brukergrensesnittet som den eksterne brukeren ser, fokuserer på det tiltenkte scenariet.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Samarbeide med leverandører ved hjelp av leverandørportalen](collaborate-vendors-vendor-portal.md)



