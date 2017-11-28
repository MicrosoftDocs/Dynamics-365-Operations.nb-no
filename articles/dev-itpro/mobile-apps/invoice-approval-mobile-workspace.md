---
title: "Mobilt arbeidsområde for fakturagodkjenning"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for fakturagodkjenning. Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: af673f076f684500b6ca84d04c01f7f773d65cd6
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-approvals-mobile-workspace"></a>Mobilt arbeidsområde for fakturagodkjenning

[!include[banner](../includes/banner.md)]

Dette emnet gir informasjon om det mobile arbeidsområdet **Fakturagodkjenning**. Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode. 

Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Oversikt

Med det mobilie arbeidsområdet **Fakturagodkjenninger**  kan regnskapsassistenter og -sjefer vise fakturaene som er tilordnet til dem, som en del av arbeidsflytprosessen leverandørfakturahode. Du kan vise fakturainformasjon, og til og med linje- og distribusjonsdetaljer, som hjelper deg å ta informerte beslutninger om godkjenning. Fra arbeidsområdet kan du utføre handlinger for å flytte fakturaen gjennom arbeidsflytprosessen. 

## <a name="prerequisites"></a>Forutsetninger

Før du kan bruke dette mobile arbeidsområdet, må du oppfylle følgende forutsetninger.

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) må være distribuert i organisasjonen din.</td>
<td>Systemansvarlig</td>
<td>Se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.
</td>
</tr>
<tr class="even">
<td>Det mobile arbeidsområdet <strong>Fakturagodkjenning</strong> må publiseres.</td>
<td>Systemansvarlig</td>
<td>Se <a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og installer mobilappen Dynamics 365 for Unified Operations:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1.  Start appen på mobilenheten.
2.  Skriv inn URL-adressen til Microsoft Dynamics 365.
3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

    [![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Godkjenne fakturaer ved hjelp av det mobile arbeidsrområdet Fakturagodkjenning
1.  Velg **Fakturagodkjenning**-arbeidsområdet på mobilenheten.
2.  Velg fakturaen som er tilordnet til deg av arbeidsflytprosessen leverandørfakturahode.
3.  På siden **Fakturaopplysninger** kan du se gjennom fakturahodeinformasjonen, for eksempel leverandør- og datoinformasjon.
4.  Velg en linje på fakturaen for å vise mer detaljert informasjon om den i  **fakturalinjedetaljer**-visningen.
5.  I visningen **Fakturalinjedetaljer** velger du **Distribusjoner** for å vise linjedistribusjonene. Her kan du vise regnskapet for fakturalinjen. Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoen.
6.  På siden **Fakturadetaljer** velger du **Distribusjoner** for å vise alle distribusjonene. Her kan du vise regnskapet for hele fakturaen. Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoene. 
7.  Velg **Vedlegg** for å vise notater eller filer som er knyttet til fakturaen.
8.  På siden **Fakturadetaljer** velger du riktig handling i arbeidsflyten forl å fullføre gjennomgangen.
9.  Velg **Ferdig**.

