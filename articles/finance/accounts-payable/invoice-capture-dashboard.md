---
title: Instrumentbord for Invoice Capture-løsning
description: Denne artikkelen beskriver instrumentbordet for Invoice capture-løsning.
author: sunfzam
ms.date: 10/15/2022
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
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690125"
---
# <a name="invoice-capture-solution-dashboard"></a>Instrumentbord for Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

I Invoice capture inneholder instrumentbordet diagrammer som gir en oversikt over fakturaene som er importert. Disse diagrammene kan hjelpe AP-lederen med å analysere ytelsen til fakturagenereringsprosessen. AP-lederen kan vise statusen for fakturagenereringsprosessen, og ved å bruke ulike filtre kan du også vise detaljer.

## <a name="available-charts"></a>Tilgjengelige diagrammer

Følgende diagrammer er tilgjengelige på instrumentbordet:

- **Alle registrerte faktura etter status** – Dette diagrammet viser følgende statuser for en registrert faktura. Ved å velge en status kan brukere filtrere de registrerte fakturaene i den detaljerte listen.

    - Registrert
    - Fullfør
    - Til vurdering
    - Foreldet

- **Totalt registrert fakturavolum** – Dette diagrammet viser antallet registrerte fakturaer etter periode. Brukerne kan endre perioden ved hjelp av rullegardinlisten.
- **Registrert faktura fra viktigste leverandører** – Dette diagrammet viser totalt antall fakturaer per leverandør. Leverandørene som har flest fakturaer, vises øverst.
- **Dager for å fylle ut per faktura med unntak** – Dette diagrammet viser gjennomsnittlig antall dager som kreves for å registrere én faktura. Denne informasjonen kan hjelpe AP-lederen med å analysere tiden det tar å behandle en faktura når manuell inngripen kreves. Hvis det finnes en trend oppover, kan brukere gå gjennom prosessdetaljene og justere innstillinger for å redusere antallet dager som er nødvendige.
- **Ufullstendige fakturaer etter tid på vent** – Dette diagrammet viser antall dager en registrert faktura ikke har blitt generert i ERP-systemet (Enterprise Resource Planning). Jo større antall ventende dager, desto lenger tid tar fakturagenereringen. AP-lederen kan drille ned i de detaljerte, oppfangede fakturaene og generere fakturaer i ERP-systemet.
