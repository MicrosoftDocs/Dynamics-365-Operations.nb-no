---
title: Arkivere ER-måltype
description: Dette emnet inneholder informasjon om hvordan du konfigurerer et arkivmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679684"
---
# <a name="archive-er-destination-type"></a>Arkivere ER-måltype

[!include [banner](../includes/banner.md)]

Du kan konfigurere et arkivmål for hver **Mappe**- eller **Fil**-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter. Basert på målinnstillingen lagres et generert dokument som et vedlegg til en oppføring i ER-jobblisten. Hvis du vil vise resultatene, går du til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Arkiverte jobber for elektronisk rapportering**.

Du kan bruke dette alternativet for å sende det genererte dokumentet til en Microsoft SharePoint-mappe eller Microsoft Azure Storage. Sett **Aktivert** til **Ja** for å sende utdata til et mål som er definert av den valgte dokumenttypen. Bare dokumenttyper der gruppen er satt til **Fil** er tilgjengelige for valg. Du definerer dokumentets [typer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) under **Organisasjonsstyring** \> **Dokumentadministrering** \> **Dokumenttyper**. Konfigurasjonen for ER-mål er den samme som konfigurasjonen for systemet for dokumentbehandling.

[![Siden Dokumenttyper](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Plasseringen bestemmer hvor filen lagres. Etter at **Arkiv**-målet er aktivert, kan resultatene lagres i jobbarkivet. Du kan vise resultatene på **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Arkiverte jobber for elektronisk rapportering**.

> [!NOTE]
> Velg en dokumenttype for jobbarkivet ved å navigere til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering** \> **Parametere for elektronisk rapportering**. Hvis du vil ha mer informasjon, kan du se [Konfigurere rammeverket for elektronisk rapportering (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Du kan lagre en fil i en bestemt SharePoint-mappe. Hvis du vil definere standard SharePoint-server, går du til **Organisasjonsstyring** \> **Dokumentadministrering** \> **Parametere for dokumentadministrering**. I **SharePoint**-fanen konfigurerer du SharePoint-mappen. Deretter kan du velge den som mappen der ER-utdataene skal lagres. **SharePoint**-plasseringen må velges i denne dokumenttypen.

[![Velge en SharePoint-mappe](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure Storage

Når type dokumentplasseringen er satt til **Azure Storage**, kan du lagre en fil i Azure Storage.

> [!NOTE] 
> ER-rammeverket lagrer filer i Azure Blob Storage permanent, i motsetning til databehandlingsrammeverket som bruker policyinnstillingen for oppbevaring i sju dager for dokumenter som må behandles. Hvis du vil ha mer informasjon, se [API for å hente meldingsstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) og [API for statuskontroll for API](../data-entities/data-management-api.md#status-check-api). De ER-relaterte filene blir lagret i Azure Blob Storage som vedlegg til programtabellposter så lenge som nødvendig. En enkelt fil vil bli slettet fra Azure Blog Storage sammen med programtabellposten som denne filen var knyttet til.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Konfigurere dokumentstyring](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]