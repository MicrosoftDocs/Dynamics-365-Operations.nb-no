---
title: Planlegg kontoplanen
description: Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.
author: aprilolson
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10906d7b30628dfe69907cfa69ae1022fde33243
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070642"
---
# <a name="plan-your-chart-of-accounts"></a>Planlegg kontoplanen

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon som hjelper deg med å planlegge kontoplanen for organisasjonen.

Hvis du vil spore og vedlikeholde økonomisk informasjon i en organisasjon, kan du definere en kontoplan. En kontoplan er en samling kontoer som definerer et økonomisk rammeverk. For å spore ytterligere transaksjonene i disse kontoene, kan du legge til segmenter. Disse segmentene kalles finansdimensjoner. En utgiftskonto kan for eksempel omfatte finansdimensjoner kalt Avdeling, Kostsenter og Formål. Brukerdefinerte regler fastsetter hvordan finansdimensjonene er knyttet til hovedkontoene og til andre finansdimensjoner, og også hvordan transaksjoner registreres. Disse brukerdefinerte reglene er kjent som kontostrukturer og avanserte regler.

Kontoplanen er en strukturert liste over den juridiske enhetens finanskontoer. Listen brukes til å utarbeide økonomiske rapporter til myndigheter og eiere. Kontoene grupperes først i kontotyper og aggregeres deretter ytterligere i større, overordnede kategorier. På det øverste nivået grupperes kontoene som henholdsvis inntekter og kostnader (driftskontoer) og aktiva og gjeld (balansekontoer).

En kontoplan kan deles og brukes av alle juridiske enheter i en organisasjon. Kontoplanen som brukes av en juridisk enhet, er definert på **Finans**-siden.

Her er noen av faktorene du må vurdere når du planlegger strukturen til kontoplanen for organisasjonen:

- Rapporteringskravene i landet eller området der organisasjonen holder til
- Rapporteringskravene til den juridiske enheten
- Graden av detaljer som kreves, både for den eksterne organisasjonen og organisasjonen din

Du kan definere kontoplanen på **Kontoplan**-siden. Du kan opprette hovedkontoer fra **Kontoplan**-siden eller **Hovedkontoer**-siden. Hovedkontoene kan ikke bruke spesialtegn som brukes som skilletegn for kontoplan. Ellers kan du oppleve ustabilitet, eller du må kanskje alltid bruke oppslag eller dialogboksen når du angir kombinasjoner av kontoer og dimensjoner. Hvis du vil ha mer informasjon, kan du se [Opprette en hovedkonto](tasks/create-main-account.md).

> [!NOTE]
> I Dynamics 365 Finance versjon 8.0 (april 2018) kan du endre skilletegn for kontoplan på siden **Parametere for økonomimodul**.

Det er lurt å koble hovedkontoene til hovedkontokategorier, slik at du kan dra nytte av standard økonomiske rapporter uten å måtte gjøre endringer. Derfor går det raskere og enklere å utforme og vedlikeholde rapporter.

Du kan opprette kontostrukturer på siden **Konfigurer kontostrukturer**. Kontostrukturer brukes til å definere gyldige kombinasjoner. Disse kombinasjonene, sammen med hovedkontoer, utgjør en kontoplan. Hvis du vil ha mer informasjon, kan du se [Opprette kontostrukturer](tasks/create-account-structures.md).

**Overstyringer for juridisk enhet**

Ikke alle hovedkontoer er gyldige for alle juridiske enheter, og noen hovedkontoer er kanskje bare relevante i en bestemt periode. I dette scenarioet kan du bruke delen **Overstyringer for juridisk enhet** til å identifisere firmaene som hovedkontoen skal suspenderes for, eieren, og perioden dimensjonen er aktiv. Overstyringene på det delte nivået kan ikke være mer begrensende enn overstyringer på nivået for juridisk enhet.

Hvis du vil ha mer informasjon, se følgende emner:

- [Finansdimensjoner](financial-dimensions.md)
- [Opprette og tilordne avanserte regelstrukturer](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

