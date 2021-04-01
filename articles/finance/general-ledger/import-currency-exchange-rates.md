---
title: Importere valutakurser
description: Dette emnet inneholder informasjon om kravene for import av referansesatser for utenlandsk valuta som er utgitt av valutakursleverandører.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 37f3897f9f2a0db0bb7ccb6851fba36814ab0c7b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249125"
---
# <a name="import-currency-exchange-rates"></a>Importere valutakurser

[!include [banner](../includes/banner.md)]

Hvis en juridisk enhet har mottatt fakturaer i fremmed valuta, må den utenlandske valutaen konverteres til den lokale valutaen. Dette betyr at det kreves oppdaterte valutakurser for ulike valutaer. Dette emnet gir en oversikt over innstillingene og behandlingen som kreves for å importer referansekurser for utenlandsk valuta som er publisert av valutakursleverandører, for eksempel den europeiske sentralbanken og sentralbanken i Russland.

Delene nedenfor beskriver informasjonsflyten som brukes til å konfigurere og behandle importen av valutakurser.

## <a name="configure-an-exchange-rate-provider"></a>Konfigurer en valutakursleverandør
Før du kan importere valutakurser, må du definere informasjonen som kreves av leverandører som tilbyr valutakursene. Bruk siden **Konfigurer valutakursleverandører** til å velge valutakursleverandører. Noen valutakursleverandører er inkludert i demodataene i Dynamics 365 Finance. Følgende tabell inneholder beskrivelser av kontrollene på denne siden.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt** | **Beskrivelse**                                                                                                                                                                                                             |
| **Navn**  | Navnet på valutakursleverandøren.                                                                                                                                                                                     |
| **Nøkkel**   | Den unike identifikatoren for del av konfigurasjonsinformasjonen som kreves av leverandøren. Denne informasjonen legges til automatisk for hver valutakursleverandør du legger til. |
| **Value** | Informasjon for hver nøkkel. Denne informasjonen legges til for hver valutakursleverandør du legger til.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Importere valutakurser
Du kan importere valutakursene fra kilden for valutakursleverandører, og legge dem til på **Valutakurser**-siden. Bruk siden **Importer valutakurser** til å importere valutakurser. Følgende tabell inneholder beskrivelser av feltene som er nødvendige for å utføre importen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Felt**                              | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                             |
| **Type valutakurs**                 | En type valutakurs.                                                                                                                                                                                                                                                                                                                                                      |
| **Valutakursleverandør**             | En valutakursleverandør.                                                                                                                                                                                                                                                                                                                                                  |
| **Importer per**                       | Denne parameteren styrer om du vil importere fra og med dagens dato eller for et spesifikt datointervall. Hvis du vil bruke et datointervall, angir eller velger du start- og sluttdatoer.                                                                                                                                                                                                                |
| **Opprett nødvendige valutapar**    | Dette alternativet styrer automatisk oppretting av valutapar, hvis valutaparene som importeres, ikke finnes. Dette alternativet er kanskje ikke tilgjengelig for enkelte leverandører.                                                                                                                                                                                               |
| **Overstyr eksisterende valutakurser**   | Dette alternativet styrer oppdatering av den eksisterende valutakursen for et valutapar når valutakursen for en bestemt dato allerede finnes. Hvis du ikke velger denne avmerkingsboksen, importeres ikke valutakursen for de bestemte datoene hvis det allerede finnes en annen valutakurs.                                                                                       |
| **Hindre import på nasjonal helligdag** | Dette alternativet styrer importen av valutakursen for en dato som er en offentlig helligdag. Hvis du for eksempel velger denne avmerkingsboksen og bruker den europeiske sentralbanken som valutakursleverandøren, vil systemet ikke oppdatere valutakursen på en offentlig fridag som er knyttet til den gjeldende juridiske enheten. Dette alternativet er kanskje ikke tilgjengelig for enkelte leverandører. |
| **Satsen fra forrige dag** | Denne avmerkingsboksen er tilgjengelig hvis du aktiverer funksjonen **ECB-import på dagens dato eller forrige dato** på siden **Funksjonsbehandling**. Denne avmerkingsboksen er bare tilgjengelig for leverandøren *Den europeiske sentralbank*. Merk av i denne avmerkingsboksen for å importere valutakursen som er publisert av den europeiske sentralbank på omtrent 16:00 CET. Boksen er merket som standard. Fjern merket i denne avmerkingsboksen for å importere valutakursen som publiseres på samme arbeidsdag.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]