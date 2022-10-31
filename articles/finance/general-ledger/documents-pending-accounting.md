---
title: Dokumenter som venter på regnskap
description: Denne artikkelen beskriver hvordan du bruker funksjonaliteten på siden Dokumenter som venter på regnskap.
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709257"
---
# <a name="documents-pending-accounting"></a>Dokumenter som venter på regnskap

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du bruker funksjonaliteten på siden **Dokumenter som venter på regnskap**.

I Microsoft Dynamics 365 Finance 10.0.30 er funksjonen **Forbedret ytelsen for regnskapsrammeverk for kildedokument** tilgjengelig. Denne funksjonen forbedrer posteringsprosessene for kildedokumentaktiverte dokumentposteringer og starter med posteringsprosessen for fritekstfakturaer.

Når denne funksjonen er aktivert, utføres postering av underfinansdokumentet separat fra regnskapsgenereringen eller *journalføringsprosessen* som oppretter de fullstendige regnskapsdetaljene som overføres til økonomimodulen. I posteringsprosessen for fritekstfaktura registreres for eksempel kundefakturaen i modulen **Utestående fordringer** før hele regnskapet genereres. Ved hjelp av denne utvidede ytelsesfunksjonen kan kundefakturaer registreres raskere mens regnskapsgenerering utsettes.

Følgende knapper er tilgjengelige på siden **Dokumenter som venter på regnskap**.

- **Generer regnskap** – Send et dokument som for øyeblikket venter på kontogenerering for journalføring.
- **Vis distribusjoner** – Vis regnskapsdistribusjonene for et valgt dokument i listen.
- **Vis feillogg** – Vis eventuelle feilmeldingsdetaljer som finnes for et dokument der regnskapstilstanden indikerer feil. Du kan vise de samme feilmeldingsdetaljene ved å velge koblingen **Feillogg** på dokumentlinjen.

Regnskapsgenerering utføres av en bakgrunnsprosess for prosessautomatisering kalt **Prosessor for regnskapsrammeverk**. Hvis du vil ha mer informasjon om oppsett og konfigurasjon av alle prosessautomatiseringer, kan du se [Prosessautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
