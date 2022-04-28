---
title: Lagring av kundealdersfordelingsdata
description: Dette emnet beskriver prosessen med å bruke ekstern lagring for aldersfordelingsdata for kunder. Du kan kjøre prosessen for lagring av aldersfordeling for kunder for å gjøre utdataene tilgjengelige for eksport til et eksternt system.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 497d49da84f4df90877908bef3031e079bc36066
ms.sourcegitcommit: d0e99545d722c924db57ae2bd06f72154a1f1f97
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/08/2022
ms.locfileid: "8557885"
---
# <a name="customer-aging-data-storage"></a>Lagring av kundealdersfordelingsdata

[!include [banner](../includes/banner.md)]


Dette emnet beskriver prosessen med å bruke ekstern lagring for aldersfordelingsdata for kunder. I Microsoft Dynamics 365 Finance kan du kjøre prosessen for lagring av aldersfordeling for kunder for å gjøre utdataene tilgjengelige for eksport til et eksternt system. Når du kjører prosessen, er de samme alternativene for aldersfordelingsrapport som er tilgjengelige i systemet, tilgjengelige for eksterne systemer. Detaljene tas alltid med i de eksporterte dataene.

Det kan være nyttig å gjøre aldersfordelingsdata for kunder tilgjengelig for et eksternt system for lagring i tilfeller der utdataene inneholder mange kunder og/eller mange transaksjoner. Hvis den eksisterende **aldersfordelte saldolisten** for kunder tidsavbrytes fordi den har for mye data å skrive ut, gir denne funksjonen en alternativ måte å hente de samme dataene på.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Aktivere funksjonen for lagring av aldersfordeling for kunder

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke innstillingene for funksjonsbehandling til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** Kredit og innkrevinger
- **Funksjonsnavn:** Lagring av aldersfordeling for kunder

## <a name="run-the-customer-aging-data-storage-process"></a>Kjør prosessen for lagring av aldersfordeling for kunder

1. Gå til **Kreditt og innkreving \> Forespørsler og rapporter \> Kunde \> Lagring av aldersfordeling for kunde**.
2. Velg **Ny**.
3. I **Navn**-feltet angir du et navn på prosessen.
4. Definer de gjenværende parameterne slik du ønsker.

    > [!NOTE]
    > Transaksjonsdetaljer inkluderes alltid, og behandlingen utføres alltid i en satsvis jobb.

5. Velg **OK**.
6. Oppdater siden **Lagring av aldersfordeling for kunde** for å se verdiene for **Bunkenavn** og **Kjøretid for parti** som vises sammen med **Behandlingsstatus**-verdien. Når den satsvise jobben er fullført, settes **Behandlingsstatus**-feltet til **Avsluttet**, og feltet **Antall aldersfordelingslinjer** angis. Hvis den satsvise jobben gjentas, settes **Behandlingsstatus**-feltet til **Venter**.
7. Velg **Filter**-knappen ved siden av feltet **Antall aldersfordelingslinjer** for å gå gjennom filtrene som er lagt til for den satsvise jobben.

Siden **Lagring av aldersfordeling for kunde** inkluderer ikke resultatene. Dataenheten **Lagring av aldersfordeling for kunde** lar deg imidlertid eksportere utdataene til et hvilket som helst format som dataadministrasjon støtter.

> [!NOTE]
> Før du eksporterer, legger du til et filter for å begrense de eksporterte resultatene til den nyeste aldersfordelingen. Du kan for eksempel legge til følgende kriterier for å returnere den nyeste satsvise kjøringen:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Du kan også legge til følgende kriterier for å returnere den nyeste satsvise kjøringen for gjeldende bruker:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
