---
title: Oversikt over Invoice Capture-løsning
description: Denne artikkelen gir informasjon om Invoice capture-løsningen.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691211"
---
# <a name="invoice-capture-solution"></a>Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen gir informasjon om Invoice capture-løsningen som automatisk oppretter leverandørfakturaer fra digitale fakturabilder.

AP-avdelingen styrer og behandler fakturaer for varer og tjenester som mottas. AP-regnskapsføreren kontrollerer data på leverandørfakturaer av følgende årsaker:

- Du kan unngå ekstra arbeid hvis det kreves justeringer eller rettelser under periodelukking
- Betale leverandørfakturaer innen forfall og forhindre økonomisk tap på grunn av feil eller feil

Optisk tegngjenkjenning (OCR) har blitt mye brukt i forskjellige industrier i tidligere år. Nå er det vanlig at utskrevne tekster skal digitaliseres, slik at de kan redigeres elektronisk, søkes i, lagres mer enhetlig og vises elektronisk. Den digitale teksten kan brukes i maskinprosesser, for eksempel kognitiv databehandling, maskinoversettelse, tekst til tale, nøkkeldata og tekstutvinning.

Teknologi for kunstig intelligens har aktivert moderne OCR-løsninger til å lese forskjellige fakturaformater fra ulike leverandører uten at det kreves mye menneskelig inngripen. Flere firmaer erkjenner at de kan spare arbeid og forbedre nøyaktigheten ved å behandle fakturaer via automatisk behandling i stedet for å bruke manuell behandling.

## <a name="system-landscape"></a>Systemlandskap

Illustrasjonen nedenfor viser hovedkomponentene og trinnene i Invoice capture-løsningen.

[![Komponenter og trinn i Invoice capture-løsningen.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Nødvendige roller

Tabellen nedenfor viser rollene som kreves for å definere og bruke Invoice capture-løsningen.

| Rolle          | Handlinger | Systemer | Rollenavn |
|---------------|---------|---------|-----------|
| Administrator | <ul><li>Konfigurer miljøer i Microsoft Power Platform.</li><li>Distribuere løsninger i Microsoft Power Platform.</li><li>Definer tilkoblinger mellom Dynamics 365 og AI Builder.</li><li>Definer Azure Data Lake Storage-lokasjoner.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365-administrator</li><li>Power Platform-administrator</li><li>Storage Blob-dataeier</li></ul> |
| AI-oppretter      | <ul><li>Vedlikehold flyter.</li><li>Opprett egendefinerte AI-modeller.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Borgeropprettere</li></ul> |
| AP-assistent      | <ul><li>Gå gjennom og gjør handlinger i oppsamlingsområdet for leverandørfakturaer.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Ny AP-clerk-rolle i Power Platform</li></ul> |
| AP-assistent      | <ul><li>Utfør daglige operasjoner som AP-assistent.</li><li>Gå til oppsamlingsområdet for leverandørfaktura.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Regnskapsassistent</li></ul> |
  
Hvis du vil ha mer informasjon om å installere Invoice capture, kan du se [Installere Invoice capture](../accounts-payable/install-invoice-capture.md).  
