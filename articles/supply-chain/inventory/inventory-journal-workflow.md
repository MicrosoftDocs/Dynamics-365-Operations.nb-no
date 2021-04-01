---
title: Godkjenningsarbeidsflyter for lagerjournal
description: Dette emnet beskriver hvordan du kan sette opp og bruke godkjenningsarbeidsflyter for lagerjournal for ulike typer transaksjoner for aktuell beholdning. Lagerjournalarbeidsflyter bidrar til å sikre at bare godkjente lagerjournaler kan posteres til transaksjoner.
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247916"
---
# <a name="inventory-journal-approval-workflows"></a>Godkjenningsarbeidsflyter for lagerjournal

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du setter opp og bruker godkjenningsarbeidsflyter for lagerjournal for ulike typer fysiske lagertransaksjoner, for eksempel postering av avganger og mottak, lagerbevegelser, stykklister og avstemmingen av fysisk lager. Lagerjournalarbeidsflyter bidrar til å sikre at bare godkjente lagerjournaler kan posteres til transaksjoner.

> [!NOTE]
> Godkjenningsarbeidsflyter for lagerjurnal gjelder bare for transaksjoner som er registrert ved hjelp av Lagerstyring-modulen. De fungerer ikke med lagerjournaler utløst fra Lagerstyring-modulen.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Aktivere funksjonen for godkjenningsarbeidsflyter for lagerjournal

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Godkjenningsarbeidsflyt for lagerjournal*

## <a name="create-your-inventory-journal-approval-workflows"></a>Opprette godkjenningsarbeidsflyter for lagerjournal

Hvis du vil sette opp denne funksjonen, må du opprette en arbeidsflyt for hver av lagerjournaltypene du vil kontrollere. Siden forskjellige lagerjournaltyper kan ha forskjellige godkjenningshierarkier og arbeidsflyttrinn, kan du konfigurere enkeltarbeidsflyter for hver lagerjournaltype.

Arbeidsflyter støtter versjonskontroll, og hver har en arbeidsflyt-ID og en aktiv versjon. Du kan velge å aktivere hver nye arbeidsflytversjon umiddelbart ved oppretting eller beholde den inaktiv. Hvis du trenger forskjellige arbeidsflyter for samme journaltype, kan du opprette flere arbeidsflyter for denne journaltypen og deretter tilordne hver av disse til et annet journalnavn som bruker denne typen.

Slik oppretter du godkjenningsarbeidsflyter for lagerjournal:

1. Gå til **Lagerstyring \> Oppsett\> Arbeidsflyter for lagerstyring**.
1. Velg **Ny** i handlingsruten.
1. Velg lagerjournaltypen du vil definere en arbeidsflyt for:
    - **Lagerbrikkeopptellingsjournal**
    - **Endringsjournal for lagereierskap**
    - **Beholdningsbevegelsesjournal**
    - **Lageroverføringsjournal**
    - **Lageropptellingsjournal**
    - **Lagerstykklistejournal**
    - **Lagerjusteringsjournal**

    ![Dialogboksen Opprett arbeidsflyt](media/journal-workflow-create-workflow.png "Dialogboksen Opprett arbeidsflyt")

1. Appen for arbeidsflytredigering starter på maskinen din. (Du kan bli bedt om å godkjenne denne handlingen.) Bruk den til å utforme arbeidsflyten etter behov. Hvis du vil ha mer informasjon om hvordan du bruker arbeidsflytredigering, se [Oversikt over arbeidsflytsystem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Når du har lagret og lukket appen for arbeidsflytredigering, må du velge om du vil aktivere denne arbeidsflytversjonen eller beholde den som inaktiv.

> [!NOTE]
> Arbeidsflyter gir versjonskontroll, som betyr at du kan vise en liste over versjoner du har opprettet, og velge hvilken som er aktiv. Hvis du vil vise listen over tilgjengelige versjoner og velge hvilken du vil aktivere, velger du en arbeidsflyt som er oppført på siden **Arbeidsflyter for lagerstyring**. I handlingsruten åpner du fanen **Arbeidsflyt** og velger **Versjoner**. Bare én versjon kan være aktiv om gangen for hver arbeidsflyt-ID.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Tilordne godkjenningsarbeidsflyter til lagerjournalnavn

Det neste trinnet er å tilordne en lagerjournalarbeidsflyt til hvert lagerjournalnavn. For hver lagerjournaltype kan du definere flere lagerjournalnavn.

Slik knytter du en lagerjournalarbeidsflyt til et lagerjournalnavn:

1. Gå til **Lagerstyring \> Oppsett \> Journalnavn \> Beholdning**.
1. Velg et journalnavn fra listekolonnen for å åpne innstillingssiden.
1. På **Generelt**-hurtigfanen angir du **Arbeidsflyt for godkjenning** til **Ja**. Hvis du blir bedt om å godkjenne handlingen, velger du **Ja**.

    ![Tilordne en arbeidsflyt til et journalnavn](media/journal-workflow-journal-name.png "Tilordne en arbeidsflyt til et journalnavn")

1. Åpne rullegardinlisten **Arbeidsflyt**, og velg den aktuelle arbeidsflyten. Listen viser hver aktive arbeidsflyt du har opprettet ved hjelp av appen for arbeidsflytredigering.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Opprette en lagerjournal og sende den til godkjenning

Når du har tilknyttet et lagerjournalnavn med den samsvarende godkjenningsarbeids flyten for lagerjournal, kan du opprette nye lagerjournaler som bruker dette navnet, og deretter sende disse journalene til godkjenning ved hjelp av den arbeidsflyten. Du vil ikke kunne postere lagerjournalen før den er godkjent av godkjennerne som er konfigurert i arbeidsflyten.

1. I navigasjonsruten utvider du **Lagerstyring \> Journaloppføringer \> Varer** og velger deretter en lagerjournaltype.
1. Velg **Ny** for å opprette en ny journal av den valgte typen.
1. Dialogboksen **Opprett lagerjournal** åpnes. Fyll ut skjemaet etter behov, og velg deretter **OK** for å lagre journalen.
1. Fullfør journalen etter behov.
1. Når du oppretter eller åpner en lagerjournal med en godkjenningsarbeidsflyt knyttet til den, er knappen **Arbeidsflyt** aktiv i handlingsruten. Når du er klar til å sende journalen til godkjenning, velger du **Arbeidsflyt**-knappen for å åpne en dialogboks, og deretter velger du **Send inn**. Godkjenningsforespørselen vil deretter rute til den aktuelle godkjenneren, som blir varslet ved hjelp av varslingsmetoden som er konfigurert for arbeidsflyten.

    ![Sende inn en journal til godkjenning](media/journal-workflow-inventory-journal.png "Sende inn en journal til godkjenning")

Hvis du vil tilbakekalle en godkjenningsforespørsel, åpner du den relevante journalen, velger **Arbeidsflyt**-knappen og velger deretter **Tilbakekall**. Dette vil tilbakestille arbeidsflyten.

Når journalen er godkjent, kan du postere den. Hvis du vil postere journalen, velger du **Poster** fra handlingsruten. Hvis **Poster**-knappen ikke er aktiv, er ikke journalen godkjent enda.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Svare på en forespørsel om godkjenning av lagerjournal

Hvis du er en godkjenner, bør du motta en melding hver gang din godkjenning er nødvendig (som konfigurert i den aktuelle arbeidsflyten). Deretter kan du godkjenne eller avvise en forespørsel om journalgodkjenning ved å gjøre følgende:

1. I navigasjonsruten utvider du **Lagerstyring \> Journaloppføringer \> Varer** og velger deretter en lagerjournaltype.
1. Åpne den aktuelle journalen og se gjennom den.
1. Velg **Arbeidsflyt**-knappen i handlingsruten for å åpne en dialogboks med en rullegardinliste. Velg ett av følgende:
    - **Godkjenn** – for å godkjenne forespørselen.
    - **Avvis** – for å avvise forespørselen.
    - **Mer \> Be om endring** – for å sende en melding til bestilleren og be vedkommende om å endre noe spesifikt og deretter sende på nytt.
    - **Mer \> Deleger** – for å delegere godkjenningen til en annen bruker.
    - **Mer \> Tilbakekall** – for å tilbakekalle godkjenningsforespørselen (tilbakestiller arbeidsflyten).
    - **Flere \> Arbeidsflytlogg** – viser loggen til denne godkjenningsarbeidsflyten så langt.

## <a name="review-the-approval-history"></a>Se gjennom godkjenningsloggen

Som med andre arbeidsflyttyper kan du bruke siden **Arbeidsflytlogg** til å vise godkjenningsarbeidsflytloggen for en hvilken som helst journal.

Slik kontrollerer du arbeidsflytloggen for en journal:

1. I navigasjonsruten utvider du **Lagerstyring \> Journaloppføringer \> Varer** og velger deretter en lagerjournaltype.
1. Åpne den relevante journalen.
1. Velg **Arbeidsflyt**-knappen i handlingsruten for å åpne en dialogboks med en rullegardinliste. Velg **Arbeidsflytlogg**. Hvis du vil ha mer informasjon, kan du se [Vise arbeidsflytlogg](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]