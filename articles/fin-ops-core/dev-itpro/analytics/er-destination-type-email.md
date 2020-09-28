---
title: Sende ER-måltype per e-post
description: Dette emnet inneholder informasjon om hvordan du konfigurerer et e-postmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745567"
---
# <a name="email-destination"></a>E-postmål

[!include [banner](../includes/banner.md)]

Du kan konfigurere et e-postmål for hver MAPPE- eller FIL-komponent i et elektronisk rapporteringsformat (ER) som er konfigurert til å generere utgående dokumenter. Basert på målinnstillingen leveres et generert dokument som et vedlegg til en elektronisk post.

Sett **Aktivert** til **Ja** for å sende en utdatafil via e-post. Når dette alternativet er aktivert, kan du angi e-postmottakere og redigere emnet og brødteksten i e-postmeldingen. Du kan definere konstante tekster for e-postemnet og meldingsteksten, eller du kan bruke ER-[formler](er-formula-language.md) for å opprette e-posttekster dynamisk. 

Du kan konfigurere e-postadresser for ER på to måter. Konfigurasjonen kan fullføres på samme måte som Utskriftsbehandling-funksjonen fullfører den, eller du kan løse en e-postadresse ved å bruke en direkte referanse til ER-konfigurasjonen via en formel.

[![Aktivere e-postmål](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Typer e-postadresser

Når du velger **Rediger** i **Til**- eller **Cc**-feltet, vises**E-post til**-dialogboksen. Du kan deretter velge hvilken type e-postadresse som skal brukes. E-posttypene **Konfigurasjons-e-post** og **Utskriftsbehandling** støttes for øyeblikket.

[![Velge e-posttype](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Utskriftsbehandling

Hvis du velger e-posttypen **Utskriftsbehandling**, kan du angi faste e-postadresser i **Til**-feltet. 

[![Konfigurere faste e-postadresser](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Hvis du vil bruke e-postadresser som ikke er faste, må du velge kildetypen e-post for et filmål. Følgende verdier støttes: **kunde**, **leverandør**, **kundeemne**, **kontakt**, **konkurrent**, **arbeider**, **søker**, **potensiell leverandør** og **sperret leverandør**. Når du har valgt en e-postkildetype, bruker du knappen ved siden av feltet **Kildekonto for e-post** til å åpne skjemaet **Formeldesigner**. Du kan bruke dette skjemaet til å legge ved en formel som ved kjøretid returnerer **partskontoen** for den valgte kildetypen fra det behandlede dokumentet til e-postmålet.

[![Konfigurere e-postkildekonto](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formler er spesifikke for ER-konfigurasjonen. Angi en dokumentspesifikk referanse til en kunde- eller leverandørparttype i **Formel**-feltet. I stedet for å skrive inn kan du finne en datakildenode som representerer kunde- eller leverandørkontoen, og deretter velge **Legg til datakilde** for å oppdatere formelen. Hvis du for eksempel bruker **ISO 20022-kredittoverføring**-konfigurasjonen, er noden som representerer en leverandørkonto, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Hvis du angir en strengverdi, for eksempel `"DE-001"` og lagrer en formel, sendes det en e-postmelding til leverandørens kontaktperson, **DE-001**.


[![ER-formelutforming-siden](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Konfigurere attributter for e-postkildekonto](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>E-post for konfigurasjon

Bruk denne e-posttypen hvis konfigurasjonen du bruker, har en node i datakildene som returnerer en **e-postadresse**. Du kan bruke datakilder og funksjoner i formeldesigner for å få en riktig formatert e-postadresse. Hvis du for eksempel bruker **ISO 20022-kredittoverføring**-konfigurasjonen, er noden som representerer en e-postadresse til en leverandørs kontaktperson, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurere e-postadressekilde](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)
- [Mål for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)
