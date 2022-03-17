---
title: Tilkoblede programmer
description: Dette emnet forklarer hvordan du konfigurerer tilkoblede programmer i elektronisk fakturering.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 59b67589139c0ce332716acf998825c6a024bded
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371616"
---
# <a name="connected-applications"></a>Tilkoblede programmer

[!include [banner](../includes/banner.md)]

Tilkoblede programmer er forekomstene av Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management du kanskje vil nå via Regulatory Configuration Service (RCS). Gjennom de tilkoblede programmene kan du konfigurere deler av globaliseringsfunksjonen i Finance eller Supply Chain Management for å få hele scenarioet med elektronisk fakturering til å fungere.

Når du ruller ut globaliseringsfunksjonen, kan oppsettinformasjonen som gjelder for programmet Finance eller Supply Chain Management, publiseres direkte fra RCS til det aktuelle tilkoblede programmet.

Det er nyttig å ha parameterne for Finance eller Supply Chain Management tilgjengelige i RCS når du har flere programmiljøer, for eksempel UAT-miljøer (testing av brukeraksept) og produksjonsmiljøer, og du vil holde oppsettet konsekvent ved å rulle ut de samme parameterne til forskjellige miljøer.

## <a name="create-a-connected-application"></a>Opprette et tilkoblet program

1. Logg på RCS-kontoen.
2. I arbeidsområdet **Globaliseringsfunksjon** velger du flisen **Elektronisk fakturering** i delen **Miljø**.
3. Velg **Tilkoblede programmer** i handlingsruten på siden **Miljøoppsett**.
4. Velg **Ny** for å opprette et tilkoblet program.
5. I **Navn**-feltet angir du navnet på programmet som skal kobles til.
6. I **Type**-feltet velger du **Dynamics 365 Finance**.
7. I **Program**-feltet angir du nettadressen til miljøet som skal kobles til.
8. I **Leier**-feltet angir du leieren for miljøet.
9. Velg **Lagre**.
10. Velg **Kontroller tilkobling** i handlingsruten for å teste tilkoblingen til miljøet. Lukk deretter siden.

## <a name="link-connected-applications-to-environments"></a>Koble tilkoblede programmer til miljøer

1. På siden **Miljøoppsett** velger du **Ny** for å tilordne et tilkoblet program til et miljø.
2. I feltet **Tilkoblet program** velger du det tilkoblede programmet.
3. Velg et tjenestemiljø i feltet **Servicemiljø**.
4. Velg **Lagre**, og lukk deretter siden.
