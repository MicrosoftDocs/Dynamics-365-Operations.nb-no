---
title: Mobilt arbeidsområde for fakturagodkjenning
description: Denne artikkelen gir informasjon om det mobile arbeidsområdet for fakturagodkjenning.
author: abruer
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4cc05d9fcea129cfb2ed8ed8df4bd4034a1fed4c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066398"
---
# <a name="invoice-approvals-mobile-workspace"></a>Mobilt arbeidsområde for fakturagodkjenning

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

Denne artikkelen gir informasjon om det mobile arbeidsområdet for **fakturagodkjenning**. Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode. 

Dette mobile arbeidsområdet er ment å brukes sammen med økonomi- og driftsmobilappen.

## <a name="overview"></a>Oversikt

Med det mobilie arbeidsområdet **Fakturagodkjenninger**  kan regnskapsassistenter og -sjefer vise fakturaene som er tilordnet til dem, som en del av arbeidsflytprosessen leverandørfakturahode. Du kan vise fakturainformasjon, og til og med linje- og distribusjonsdetaljer, som hjelper deg å ta informerte beslutninger om godkjenning. Fra arbeidsområdet kan du utføre handlinger for å flytte fakturaen gjennom arbeidsflytprosessen. 

## <a name="prerequisites"></a>Forutsetninger

Før du kan bruke dette mobile arbeidsområdet, må du oppfylle følgende forutsetninger.

<table>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Rolle</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance må distribueres i organisasjonen.</td>
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

Laste ned og installere økonomi- og driftsmobilappen:

-   [For Android-telefoner](https://go.microsoft.com/fwlink/?linkid=850662)
-   [For iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Logge på mobilappen

1.  Start appen på mobilenheten.
2.  Angi URL-adressen for Microsoft Dynamics365.
3.  Første gang du logger deg på, blir du bedt om brukernavn og passord. Angi legitimasjon.
4.  Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet. Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.

    [![Hent for å oppdatere.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

