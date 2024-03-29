---
title: Konfigurere arbeidsflyter for godkjenning av leie
description: Artikkelen beskriver hvordan du definerer en godkjenningsarbeidsflyt som skal kjøres når en ny leieavtale opprettes.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0162e559f8aaec248cfb9042b0152788536c9fc9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870285"
---
# <a name="set-up-lease-approval-workflows"></a>Konfigurere arbeidsflyter for godkjenning av leie

[!include [banner](../includes/banner.md)]

Artikkelen beskriver hvordan du definerer en godkjenningsarbeidsflyt som skal kjøres når en ny leieavtale opprettes. Hvis du vil ha informasjon om hvordan du bruker arbeidsflyten, kan du se [Bruke arbeidsflyter for godkjenning av leie](use-create-lease-wrkflw.md). 

1. Gå til **Aktivaleie \> Oppsett \> Leiearbeidsflyt**.
2. Velg **Ny** på siden **Leiearbeidsflyt**.
3. I dialogboksen som vises, under **Arbeidsflyttype**, velger du koblingen **Leiearbeidsflyt**.

    Programmet åpnes. Når den har kjørt, må du logge på Azure Active Directory (Azure AD) for å omadressert til arbeidsflytprogrammet.

4. Dra elementet for **Godkjenningsarbeidsflyt for leie** til arbeidsflyten.
5. Koble én node fra **Start** til **Godkjenningsarbeidsflyt for leie**. Deretter kobler du **Godkjenningsarbeidsflyt for leie** til **Slutt**.
6. Dobbeltklikk på **Godkjenningsarbeidsflyt for leie**.
7. Velg **Egenskaper** og deretter, under **Grunnleggende innstillinger**, angir du navnet på arbeidsflyten.

    På denne siden kan du også angi flere parametere for arbeidsflyten. Hvis du har aktivert **Automatiske handlinger**, vil systemet automatisk utføre en bestemt handling. Du kan sende varslinger hvis de er angitt i kategorien **Varslinger**. I kategorien **Avanserte innstillinger** kan du angi en endelig godkjenner, angi en tidsgrense og angi bestemte handlinger som må fullføres.

8. Når du er ferdig med å angi arbeidsflytparametere, velger du **Lukk**.
9. Velg **Trinn 1**, og velg deretter **Egenskaper**.
10. Under **Grunnleggende innstillinger** skriver du inn et navn på trinnet, oppretter en emnelinje for godkjenningen og angir instruksjoner for godkjenningen.
11. På siden **Tilordning** velger du tilordningstypen.
12. Hvis du vil tilordne bestemte brukere til godkjenningen, velger **Bruker**, velger brukerne som godkjenner leieavtaler, og deretter velger du **Lukk**.
13. Velg **Lagre og Lukk** for å opprette arbeidsflyten. Deretter velger du **OK** når du blir bedt om det.
14. Velg **Lukk** på siden **Opprett arbeidsflyt**.
14. Velg den nye arbeidsflyten, og velg deretter **Versjoner**. Velg deretter **Gjør aktiv** for å sikre at arbeidsflyten er aktiv.
15. Velg **Lukk**. Den nye aktive versjonen vises.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
