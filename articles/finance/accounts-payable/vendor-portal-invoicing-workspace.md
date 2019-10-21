---
title: Arbeidsområde for leverandørsamarbeidsfakturering
description: Dette emnet forklarer hvordan du kan vise leverandørfakturaer og sende fakturaer fra arbeidsområdet for leverandørsamarbeidsfakturering.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 626607814d6c747d74a13de284db097f0efd8a0c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179277"
---
# <a name="vendor-collaboration-invoicing-workspace"></a>Arbeidsområde for leverandørsamarbeidsfakturering

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kan vise leverandørfakturaer og sende fakturaer fra arbeidsområdet for leverandørsamarbeidsfakturering.

Arbeidsområdet **Fakturering av leverandørsamarbeid** kan brukes til å vise informasjon om leverandør og sende fakturaer til systemet som bruker funksjonene for arbeidsflyt.


<a name="vendor-collaboration-invoicing-workspace"></a>Arbeidsområde for leverandørsamarbeidsfakturering
----------------------------------------

### <a name="summary-tiles"></a>Sammendrag-fliser

Flisene **Sammendrag** gir en oversikt over fakturaer for den valgte leverandøren. Du kan vise fakturaer etter deres tilstand.
-   Fakturautkast er ikke sendt til arbeidsflyten.
-   Sendte, ikke-godkjente fakturaer er de fakturaene som leverandøren har sendt, men de ikke er postert i programmet.
-   Godkjente, ikke-betalte fakturaer er de fakturaene som er postert, men som ikke er fullstendig betalte.
-   Betalte fakturaer er de som er fullstendig betalte i programmet.

Ved å klikke en flis, vises det en filtrert visning av siden **Fakturaliste**.

### <a name="tabular-lists"></a>Tabellister

I delen **Tabellister** er statusen for fakturering delt inn på samme måte som sammendragsflisene: Utkast og Sendt, men ikke godkjente lister. Når du er i kladdemodus, kan en faktura sendes til arbeidsflyten eller slettes. Den siste tabellisten er et alternativ for å finne fakturaer. Du kan filtrere når du søker, slik at søk utføres raskere.

### <a name="all-vendor-invoices-list-page"></a>Side med liste over alle leverandørfakturaer

Du kan vise alle posterte og uposterte leverandørfakturaer på listesiden **Leverandørsamarbeidsfakturaer**. Du kan bruke denne listesiden til å vise betalingsstatusen for fakturaene. Betalingsstatusene inkluderer Ikke-bokført, Ubetalt, Delvis betalt og Fullt betalt.
Opprette en ny faktura fra en bestilling

Du kan opprette en ny leverandørfaktura ved å velge handlingen **Ny** i arbeidsområdet **Fakturering av leverandørsamarbeid**. Bestillingsnummeret og fakturanummeret må være oppgitt av leverandøren. Som standard vises alle linjene fra leverandørens bestilling på den nye fakturaen. Informasjon om antall og kostnad kan redigeres før du sender leverandørfakturaen til arbeidsflyten. Du kan knytte filer, notater, bilder og URL-adresser til en faktura før de sendes.

Hvis du vil ha mer informasjon, kan du se [Leverandørsamarbeid med eksterne leverandører](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)


