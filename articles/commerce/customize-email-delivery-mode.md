---
title: Tilpasse transaksjons-e-poster etter leveringsmåte
description: Dette emnet beskriver hvordan du definerer egendefinerte e-postmaler for bestemte meldingstyper og leveringsmåter i Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031854"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Tilpasse transaksjons-e-poster etter leveringsmåte

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du definerer egendefinerte e-postmaler for bestemte meldingstyper og leveringsmåter i Microsoft Dynamics 365 Commerce.

Transaksjons-e-postmeldinger kan nå tilpasses for en kombinasjon av en varslingstype (for eksempel **Ordre opprettet**, **Ordre pakket** eller **Ordre fakturert**) og en leveringsmåte (for eksempel over natten, hent i butikk eller hent utenfor butikk). Egendefinerte transaksjons-e-poster lar forhandlere levere kundens bestilling med oppfyllelsesfunksjoner som er skreddersydd til ordrens leveringsmåte. En Ordre pakket-hendelse tilpasses slik at instruksjoner om henting utenfor butikk for kunder som velger henting utenfor butikk. Den kan også gi informasjon om transportøren og levering for kunder som velger å få bestillingen levert.

> [!NOTE]
> Hvis du vil bruke funksjonaliteten for egendefinerte transaksjons-e-postmeldinger, må du først aktivere funksjonen **Tilpass transaksjons-e-postmaler etter leveringsmåte** ved å gå til **Arbeidsområder \> Funksjonsbehandling** i Commerce Headquarters.

E-poster kan tilpasses etter leveringsmåte for følgende varslingstyper:

- **Ordreannullering** – Denne typen e-postvarsling er ny.
- **Ordre opprettet**
- **Ordre bekreftet**
- **Ordre fakturert** – Denne typen e-postvarsling er ny. Den kan brukes i stedet for varslingstypen **Ordre sendt** som sender en varsling for en hvilken som helst fakturahendelse som har en sendt leveringsmåte (ikke en henting, utbæring eller elektronisk leveringsmåte).
- **Ordre plukket**
- **Ordre pakket**
- **Ordre klar for henting** – Denne varslingstypen kan tilpasses etter leveringsmåte bare hvis funksjonen **Støtte for flere leveringsmåter** er aktivert. I så fall tilsvarer denne varslingstypen **Ordre pakket**-varslingstypen.
- **Betaling mislyktes**
- **Erstatningsordre opprettet**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Konfigurer e-postmaler for bestemte leveringsmåter

I denne fremgangsmåten er forutsetningen at du allerede har opprettet de nye, egendefinerte e-postmalene, og har lagt dem til på siden **E-postmaler for organisasjon**. Hvis du vil ha informasjon om hvordan du oppretter og laster opp e-postmaler, kan du se [Opprett e-postmaler for transaksjonshendelser](email-templates-transactions.md).

Følg denne fremgangsmåten for å konfigurere e-postmaler for bestemte leveringsmåter i Commerce Headquarters.

1. Gå til **Handelsprofil for e-postvarsling**.
1. Under **Varslingsinnstillinger for handelshendelse** velger du en eksisterende varslingstype.
1. Mens varslingstypen fremdeles er valgt, velger du **Konfigurer leveringsmåter**.
1. Velg **Ny** i dialogen **Leveringsmåter**.
1. Velg en leveringsmåte i feltet **Leveringsmåte**.
1. I feltet **E-post-ID** velger du e-postmalen som skal tilordnes leveringsmåten.
1. Merk av i **Aktiv**-avmerkingsboksen.
1. Gjenta trinn 4 til og med 7 for å legge til flere leveringsmåter.
1. Når du er ferdig, velg **OK**.

> [!NOTE]
> - Når mer enn én leveringsmåte finnes på tvers av linjer i en salgsordre, blir standardmalen brukt. Standardmalen er malen som er tilordnet til varslingstypen på siden **Handelsprofil for e-postvarsling**.
> - Hvis en salgsordre har en leveringsmåte som ikke er konfigurert for en egendefinert e-postmal, brukes standard e-postmalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Opprette telefonsenterordrer](tasks/create-call-center-orders.md)

[Endre leveringsmodus i salgssted](pos-change-delivery-mode.md)
