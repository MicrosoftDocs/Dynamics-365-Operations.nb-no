---
title: Konfigurere import av avansert bankavstemming ved hjelp av elektronisk rapportering
description: Dette emnet beskriver hvordan du bruker elektronisk rapportering til å konfigurere importprosessen for avansert bankavstemming.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 30530a9870ba2ff0546237d2698d1675afa78104
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770201"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Konfigurere import av avansert bankavstemming ved hjelp av elektronisk rapportering

[!include [banner](../includes/banner.md)]

Funksjonen Avansert bankavstemming lar deg importere elektroniske bankkontoutdrag og automatisk avstemme dem med banktransaksjoner i Microsoft Dynamics 365 Finance. Dette emnet beskriver hvordan du definerer funksjonen for import av dine bankkontoutdrag. Oppsettet for import av bankkontoutdrag varierer, avhengig av formatet på der elektroniske bankkontoutdraget. Microsoft Dynamics 365 Finance støtter tre formater for bankkontoutdrag: ISO20022, MT940 og BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Sett opp konfigurasjonen av elektronisk rapportering

1. Gå til **Arbeidsområder \> Elektronisk rapportering**.
2. Velg **Repositorier** på flisen for **Microsoft**-konfigurasjonsleverandøren.
3. Velg **Global**, og velg deretter **Åpne**.
4. Hvis det må opprettes en tilkobling til repositoriet, velger du den blå koblingen i dialogboksen.
5. I konfigurasjonslisten finner du **Bankkontoutdragsmodell \> Bankkontoutdragsmodell BAI2**.
6. Velg **BAI2**-formatet.
7. På hurtigfanen **Versjoner** velger du den nyeste versjonen, og deretter velger du **Importer**.

## <a name="set-up-the-bank-statement-format"></a>Definer formatet for bankkontoutdrag

1. Gå til **Kontant- og bankbehandling \> Oppsett \> Oppsett for avansert bankavstemming \> Bankkontoutdragsformat**.
2. Velg **Ny**.
3. Angi feltene **Utdragsformat** og **Navn**.
4. Merk av for **Generelt elektronisk importformat**.
5. Sett feltet **Importer konfigurasjon av format** til **BAI2**-formatet.

## <a name="set-up-the-bank-account"></a>Konfigurer bankkontoen

1. Gå til **Kontant- og bankbehandling \> Bankkontoer \> Bankkontoer**.
2. Åpne bankkontoen.
3. På hurtigfanen **Avstemming** setter du alternativet **Avansert bankavstemming** til **Ja**.
4. Sett feltet **Utdragsformat** til **BAI2**-formatet som ble opprettet tidligere.

## <a name="import-the-bank-statement"></a>Importer bankkontoutdraget

1. Gå til **Kontant- og bankbehandling \> Avstemming av bankkontoutdrag \> Bankkontoutdrag**.
2. Øverst på siden **Bankkontoutdrag** velger du **Importer utdrag**.
3. Sett **Bankkonto**-feltet til bankkontoen i kontoutdraget.
4. Sett feltet **Utdragsformat** til **BAI2**-formatet som ble opprettet tidligere.
5. Velg **Bla gjennom**, og velg **BAI**-filen.
6. Velg **Last opp**.
7. Velg **OK** for å importere den valgte filen.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Eksempler på bankkontoutdragsformater og tekniske oppsett
Nedenfor følger eksempler på definisjonene av tekniske oppsett for avansert bankavstemmingsimportfil og tre tilknyttede filer med eksempler på bankkontoutdrag: [Importer fileksempler](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Definisjon av teknisk oppsett                             | Fil med bankkontoutdragseksempler          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

