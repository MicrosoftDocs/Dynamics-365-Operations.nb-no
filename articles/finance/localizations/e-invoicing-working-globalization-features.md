---
title: Komponenter for globaliseringsfunksjon
description: Dette emnet gir en oversikt over komponenter for globaliseringsfunksjon.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 87d7dd231b9ccda7761c91f129659c18039f3299
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371700"
---
# <a name="globalization-feature-components"></a>Komponenter for globaliseringsfunksjon

[!include [banner](../includes/banner.md)]

En globaliseringsfunksjon er et sett med komponenter som definerer reglene for datatransformasjon i konfigurasjoner for elektronisk rapportering (ER). Disse komponentene omfatter instruksjoner for behandling av elektroniske dokumenter og sender dem deretter til eller mottar dem fra eksterne kanaler. De omfatter også betingelser som definerer når en funksjon skal kjøres for de innkommende forretningsdataene.

Alle komponentene er avhengige av hverandre. Globaliseringsfunksjoner gjør det enkelt å opprette og vedlikeholde denne avhengigheten og å støtte administrasjon av livssyklus og versjonskontroll av settet med komponenter.

## <a name="access-electronic-invoicing-feature-components"></a>Tilgang til komponenter for funksjonen for elektronisk fakturering 

1. Logg deg på kontoen for Regulatory Configuration Service (RCS).
2. I arbeidsområdet **Globaliseringsfunksjon**, i **Funksjoner**-delen velger du flisen **Elektronisk fakturering**.

    Globaliseringsfunksjoner består av flere komponenter. Siden **Funksjoner for elektronisk fakturering** inneholder en egen fane for hver komponent.

    - **Versjon** – Denne komponenten støtter administrasjon av livssyklusen til funksjonen. Du kan bruke den til å administrere status for ulike versjoner av funksjonen.
    - **Konfigurasjoner** – Med denne komponenten kan du styre, vise og redigere relaterte konfigurasjoner for ER-format og -formattilordning som brukes i datasamlebåndet for behandling.
    - **Oppsett** – denne komponenten gjør det mulig for brukere av globaliseringstjenester, for eksempel en e-faktureringstjeneste, å styre oppsettet av den relaterte funksjonsversjonen. Derfor støtter den den fleksible konstruksjonen av kommunikasjons- og svarregler.
    - **Miljøer** – Med denne komponenten kan brukere av globaliseringstjenester, for eksempel en e-faktureringstjeneste, administrere miljøet der funksjonsversjonsoppsettet brukes. Den lar dem også gi autorisasjon til brukere som skal ha tilgang til funksjonsversjonsoppsettet.
    - **Organisasjoner** – Med denne komponenten kan brukere dele funksjonen med eksterne organisasjoner.
    - **Koder** – Med denne komponenten kan du merke funksjoner som kan brukes i globaliseringsplanen for referansen.
