---
title: Bruke arbeidsflyter for godkjenning av leie
description: Dette emnet forklarer hvordan du bruker arbeidsflyter til å godkjenne leie av aktiva, og hvordan du sporer status og historikk for arbeidsflyter.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 33faf7aa6bc9e5df4b8b0f004692b2c1803c6994264c7b9a8e3eb404387f6800
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726092"
---
# <a name="use-lease-approval-workflows"></a>Bruke arbeidsflyter for godkjenning av leie

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker arbeidsflyter til å godkjenne leie av aktiva, og hvordan du sporer status og historikk for arbeidsflyter. Arbeidsflyter bidrar konsekvens i administrasjon av leiegodkjenninger ved å gi et standardsett med godkjenningstrinn og tilordne bestemte brukere som godkjenner hvert trinn i prosessen. En godkjenner kan godkjenne en leieavtale, avvise den, be om en endring eller tilordne den til en annen bruker for godkjenning. Arbeidsflyter kan også gi mer innsyn i godkjenningsprosessen ved å la deg spore status og logg. I tillegg kan du vise en sentralisert arbeidsliste som viser oppgaver og godkjenninger som er tilordnet bestemte godkjennere.

Før du bruker denne fremgangsmåten må du kontrollere at det er opprettet minst én arbeidsflyt for leiegodkjenning. Hvis det ikke finnes noen arbeidsflyt, oppretter du en. Hvis du vil ha informasjon om hvordan du konfigurerer en arbeidsflyt, kan du se [Konfigurere arbeidsflyter for godkjenning av leie](set-up-lease-wrkflw.md).

1. Send inn en leieavtale til godkjenning. På siden **Tablådetaljer** for leieavtalen velger du **Arbeidsflyt**, og deretter velger du **Send**.
2. I dialogboksen som vises, kan du legge til en kommentar. Den tilordnede godkjenneren vil se denne merknaden sammen med leieavtalen. Når du er ferdig med å legge inn kommentaren, velger du **Send**. Leieavtalen sendes til arbeidsflytsystemet, og godkjenneren mottar den for godkjenning.
3. Hvis du vil vise leieavtalene som er utpekt for godkjenning, kan du gå til **Moduler \> Felles \> Arbeidselementer \> Arbeidselementer som er tilordnet til meg**.
4. På siden **Arbeidselementer som er tilordnet til meg** velger du **leie-ID**-koblingen for leieavtalen du vil vise. Hvilken side som vises, er avhengig av hvilke leietablåer og leiedetaljer du har tilgang til.
5. Når du har fullført visningen av leieavtalen, velger du **Arbeidsflyt** og bestemmer hvilken handling som skal utføres. Alternativene omfatter **Godkjenn**, **Avvist**, **Be om endring**, **Deleger** og **Annullert**. Du kan også velge **Vis logg** for å vise godkjenningsloggen for den valgte leieavtalen.
6. Når du har valgt en handling, angir du en kommentar som beskriver handlingen. Når du er ferdig med å angi kommentaren, velger du **Godkjent**-handlingen fra listen.
7. Hvis du vil vise godkjenningshandlingene, går du tilbake til siden **Leiedetaljer** fra siden **Leiesammendrag**, og deretter velger du **Arbeidsflyt \> Vis logg**.

    Du kan vise arbeidsflytaktivitetene på siden **Arbeidsflytlogg**. Denne siden viser arbeidsflyttrinnene som er iverksatt på den bestemte leieavtalen. Du kan også bruke **Arbeidselementer**-feltet til å vise statusen for de tilordnede arbeidselementene.

8. Hvis du vil stoppe en arbeidsflyt, velger du **Tilbakekalling** på siden **Arbeidsflytlogg**. I dialogboksen som vises, angir du en kommentar, og deretter velger du **OK**.
9. Hvis du vil deaktivere en arbeidsflyt, eller aktivere en arbeidsflyt som er opprettet tidligere, kan du gå til **Aktivaleie \> Oppsett \> Leiearbeidsflyt**. Deretter, på siden **Leiearbeidsflyt**, velger du **Arbeidsflyt \> Versjoner**. Hvis du vil gjøre en gjeldende arbeidsflyt inaktiv, velger du den aktive leieavtalen i dialogboksen leieversjon, og deretter velger du **Aktiver**. Hvis du vil at en eksisterende arbeidsflyt skal være aktiv, velger du arbeidsflyten og deretter **Gjør aktiv**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
