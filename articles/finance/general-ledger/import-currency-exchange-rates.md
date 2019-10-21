---
title: Importer valutakurser
description: Hvis en juridisk enhet har mottatt fakturaer i fremmed valuta, er det nødvendig å konvertere den utenlandske valutaen til den lokale valutaen. Dette betyr at det kreves oppdaterte valutakurser for ulike valutaer. Dette emnet gir en oversikt over de nødvendige innstillingene og behandling for import av referansekurser for utenlandsk valuta publisert på Internett ved valutakursleverandører, for eksempel den europeiske sentralbanken og sentralbanken i Russland.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cdc9373ab22092e1f28bd087519f7476a7f2139a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186515"
---
# <a name="import-currency-exchange-rates"></a>Importer valutakurser

[!include [banner](../includes/banner.md)]

Hvis en juridisk enhet har mottatt fakturaer i fremmed valuta, er det nødvendig å konvertere den utenlandske valutaen til den lokale valutaen. Dette betyr at det kreves oppdaterte valutakurser for ulike valutaer. Dette emnet gir en oversikt over de nødvendige innstillingene og behandling for import av referansekurser for utenlandsk valuta publisert på Internett ved valutakursleverandører, for eksempel den europeiske sentralbanken og sentralbanken i Russland.

Delene nedenfor beskriver informasjonsflyten som brukes til å konfigurere og behandle importen av valutakurser.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurer en valutakursleverandør
Før du kan importere valutakurser, må du definere informasjonen som kreves av leverandører som tilbyr valutakursene. Bruk siden **Konfigurer valutakursleverandører** til å velge valutakursleverandører. Noen valutakursleverandører er inkludert i demodataene i Dynamics 365 Finance. Følgende tabell inneholder beskrivelser av kontrollene på denne siden.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt** | **Beskrivelse**                                                                                                                                                                                                             |
| **Navn**  | Navnet på valutakursleverandøren.                                                                                                                                                                                     |
| **Nøkkel**   | Den unike identifikatoren for del av konfigurasjonsinformasjonen som kreves av leverandøren. Denne informasjonen legges til automatisk for hver valutakursleverandør du legger til når du klikker **Legg til**-knappen. |
| **Verdi** | Informasjon for hver nøkkel. Denne informasjonen legges til for hver valutakursleverandør du legger til når du klikker **Legg til**-knappen.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importer valutakurser
Du kan importere valutakursene fra kilden for valutakursleverandører, og definere dem på **Valutakurser**-siden. Bruk siden **Importer valutakurser** til å importere valutakurser. Følgende tabell inneholder beskrivelser av feltene som er nødvendige for å utføre importen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt**                              | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                             |
| **Type valutakurs**                 | En type valutakurs.                                                                                                                                                                                                                                                                                                                                                      |
| **Valutakursleverandør**             | En valutakursleverandør.                                                                                                                                                                                                                                                                                                                                                  |
| **Importer per**                       | Denne parameteren styrer om du vil importere fra og med dagens dato eller for et datointervall. Hvis du vil bruke et datointervall, angir eller velger du start- og sluttdatoer.                                                                                                                                                                                                                |
| **Opprett nødvendige valutapar**    | Dette alternativet styrer automatisk oppretting av valutapar, hvis valutaparene som importeres, ikke finnes. Dette alternativet er kanskje ikke tilgjengelig for enkelte leverandører.                                                                                                                                                                                               |
| **Overstyr eksisterende valutakurser**   | Dette alternativet styrer oppdatering av den eksisterende valutakursen for et valutapar når valutakursen for en bestemt dato allerede finnes. Hvis du ikke velger denne avmerkingsboksen, importeres ikke valutakursen for de bestemte datoene hvis det allerede finnes en annen valutakurs.                                                                                       |
| **Hindre import på nasjonal helligdag** | Dette alternativet styrer importen av valutakursen for en dato som er en offentlig helligdag. Hvis du for eksempel velger denne avmerkingsboksen og bruker den europeiske sentralbanken som valutakursleverandøren, vil systemet ikke oppdatere valutakursen på en offentlig fridag som er knyttet til den gjeldende juridiske enheten. Dette alternativet er kanskje ikke tilgjengelig for enkelte leverandører. |




