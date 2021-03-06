---
title: Opprette en jobb i Attract
description: Dette emnet beskriver elementene i en jobb i Attract. Det forklarer også hvordan du oppretter en jobb.
author: hasrivas
manager: AnnBe
ms.date: 07/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 95bc75596f6f014b58160022f41ae86a825c5afc
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527272"
---
# <a name="create-a-job-in-attract"></a>Opprette en jobb i Attract

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver elementene i en jobb i Microsoft Dynamics 365 Talent: Attract. Det forklarer også hvordan du oppretter en jobb.

## <a name="job-creation"></a>Jobboppretting

Administratorer, rekrutteringspersoner og ansettelsesledere kan opprette jobber. Når du oppretter en jobb, blir du bedt om å velge din rolle i prosessen: ansettelsesansvarlig eller rekrutterer. Når du har valgt en rolle, blir du bedt om å velge en prosessmal. Hvis du velger **Hopp over**, brukes standardmalen. Hvis du vil ha mer informasjon om prosessmaler, se [Opprette en prosessmal i Attract](./process-templates-attract.md).

En jobb i Attract har jobbdetaljer, et ansettelsesteam, en ansettelsesprosess, ledige stillinger og analyse.

## <a name="job-details"></a>Stillingsdetaljer

Kategorien **Jobbdetaljer** inneholder detaljer om jobbens ansvarsområder og attributter. Felt for stillingstittel, jobbeskrivelse og jobbplassering er nødvendige. De andre feltene er valgfrie.

Som standard er feltet **Antall ledige stillinger** satt til **1**. Du kan imidlertid endre verdien. Når et tilbud er klargjort for en jobb, reduseres verdien i feltet **Antall ledige stillinger tilgjengelig**.

Hvis stillingsadministrasjon er aktivert i administrasjonssenteret, er **Oppdater stillinger**-oppslaget tilgjengelig. Dette oppslaget leser Jobbstilling-enheten i Common Data Service og returnerer en liste over stillinger som kan velges for jobben. Hvis antall stillinger du velger, overskrider antall ledige stillinger, får du en advarsel. Du kan også få en advarsel hvis en stilling brukes i flere jobber.

> [!NOTE]
> Stillingsadministrasjon er tilgjengelig med tillegget for omfattende ansettelse.

Avhengig av innstillingene i tilbudsaktiviteten for ansettelsesprosessen, kan et posisjonsnummer brukes to ganger i et tilbud. Hvis du vil ha mer informasjon, kan du se [Aktiviteter i ansettelsesprosesser](./activities-attract.md).

Attract inkluderer et standardsett med **Ferdigheter**. Disse ferdighetene vises som forslag mens du skriver. Du kan legge til flere ferdigheter ved å angi ny kompetansetekst i feltet og deretter trykke Enter.

Attract inkluderer et standardsett med **Jobbfunksjoner**. Du kan legge til opptil tre flere jobbfunksjoner ved å angi den nye jobbfunksjonen i feltet og trykke Enter.

Attract inkluderer et standardsett med **Selskapets bransje**. Du kan legge til opptil tre flere selskapsbranser ved å angi den nye selskapsbransjen i feltet og trykke Enter.

## <a name="hiring-team"></a>Ansettelsesteam

Kategorien **Ansettelsesteam** inneholder listen over personer som vil være involvert i jobben. Når brukere legges til i et ansettelsesteam, må de tilordnes en rolle i ansettelsesteamet. Rollen fastsetter dataene som brukerne har tilgang til, og varslingene de mottar. Rollene som kan velges, er **Rekrutterer**, **Ansettelsesansvarlig**, **Representant** og **Intervjuer**. Hvis du vil ha mer informasjon om rollerettigheter, kan du se dokumentet "Rollebehandling". Rekrutteringspersoner og ansettelsesansvarlige utnevne kan én eller flere representanter til å arbeide på deres vegne. Hvis du vil ha mer informasjon om representanter, kan du se [Administrasjon av sikkerhet og rolle i Attract](./security-attract.md).

Ansettelsesteamet kan oppdateres når jobben er aktivert.

## <a name="process"></a>Prosess

Standardinformasjon om ansettelsesprosessen er basert på prosessmalen for som ble valgt da jobben ble opprettet. Hvis en bestemt mal ikke var merket da, brukes standardmalen. Når du definerer ansettelsesprosessen, kan du legge til eller fjerne forskjellige stadier, bortsett fra stadiene kundeemne, søknad og tilbud. Selv om kundeemne-stadiet ikke kan fjernes, kan den deaktiveres. Du kan legge til eller fjerne en eller flere forhåndsdefinerte aktiviteter i hvert trinn.

Hvis du vil ha mer informasjon om aktiviteter som kan legges til ansettelsesprosessen, kan du se [Aktiviteter i ansettelsesprosesser](./activities-attract.md).

> [!NOTE]
> Ansettelsesprosessen kan ikke oppdateres når en jobb er aktivert.

## <a name="postings"></a>Posteringer

Når en jobb er aktivert, kan den posteres. Bare rekrutteringspersoner og administratorer kan postere jobber. Jobben kan posteres til Talent Careers (et karriereområde i Dynamics 365 Talent) eller LinkedIn. Attract-teamet jobber kontinuerlig for å samarbeide med jobbtavleaggregatorer. Denne listen utvides over tid. Når en jobb er postert som bare intern, må kandidater ha en AAD-konto for å vise og søke på jobben. Hvis jobben er oppført som offentlig, kan kandidsater vise og søke på jobber ved hjelp av alle godkjenningsalternativer. 

Hvis du vil ha mer informasjon om ledige stillinger, se [Konfigurere karriereområdet i Microsoft Dynamics 365 Talent - Attract](career-site.md).

> [!NOTE]
> Stillingsposteringsfunksjonaliteten er bare tilgjengelig med tilegget for omfattende ansettelse for Attract.

## <a name="activate"></a>Aktiver

Når en en jobb er aktivert, kan den posteres, og kundeemner og søkere kan legges til den. Alternativet for å legge til kundeemner i en jobb er angitt i kundeemneaktiviteten i ansettelsesprosessen.

> [!NOTE]
> Ansettelsesprosessen kan ikke oppdateres når en jobb er aktivert.

## <a name="prospects-and-applicants"></a>Kundeemner og søkere

Alternativet for å legge til kundeemner i en jobb er angitt i [Aktiviteter i ansettelsesprosesser](./activities-attract.md#prospect-activity) i ansettelsesprosessen. Dette alternativet må angis før du aktiverer jobben. Når en en jobb er aktivert, kan kundeemner og søkere legges til den.

## <a name="approvals"></a>Godkjenninger

Attract-jobber kan sendes til godkjenning. Ikke alle jobber krever godkjenning. Behovet er satt på malnivå. Godkjenninger er som standard deaktivert på malen. Hvis du vil definere godkjenninger, går du til en prosessmal og angir **Godkjenning**-feltet til standard. Velg deretter denne malen når du oppretter jobben.

Når en jobb er lagret, kan den sendes til godkjenning. Tabellen nedenfor viser statusene til et dokument som bruker godkjenninger.

| Status   | Fylke                                                               |
|----------|---------------------------------------------------------------------|
| Kladd    | Jobben er lagret, men den er ikke sendt til en arbeidsflyt. |
| Uavsluttet  | Jobben er sendt til godkjennere.                            |
| Godkjent | Jobben er godkjent, men er ikke aktivert.            |
| Avslått | Jobben er avvist, og kan ikke aktiveres.               |
| Aktive   | Jobben er godkjent og aktivert.                            |

I jobblisten kan du filtrere på jobbstatusene.

Godkjenninger kan sendes til en Microsoft Azure Active Directory (Azure AD)-bruker i firmaet. Godkjenningene sendes parallelt til alle personene som er oppført som godkjennere. Alle godkjennere må godkjenne jobben før den kan flyttes fremover. Hvis en enkelt godkjenner avviser jobben, vil jobben vise en **Avvist**-status. Når en jobb er godkjent, kan den aktiveres.

Hvis en bruker redigerer jobben etter at den er godkjent, men ikke aktivert, vil jobbstatusen tilbakestilles til **Utkast**, og prosjektet må sendes på nytt for godkjenning. Når en godkjent jobb er aktivert, kan du ikke redigere den.

Folk som er oppført som godkjennere, mottar en melding i Attract og en e-post for å informere dem om at de har et element å godkjenne.  I e-posten kan godkjennere klikke koblingen for å åpne jobben, gå gjennom detaljene, og enten godkjenne eller avvise. Etter at jobbstatusen er satt til **Godkjent** eller **Avvist**, får avsenderen beskjed i Attract, og de vil motta en e-post. Godkjennere vil også motta en påminnelsese-post hvis de ikke har svart på forespørselen om godkjenning innen 24 timer.

> [!NOTE]
> Du kan opprette egendefinerte e-postmaler for e-post for godkjenning. Hvis du vil ha mer informasjon, se [Opprette og administrere e-postmaler](https://docs.microsoft.com/dynamics365/unified-operations/talent/email-templates).

## <a name="create-a-job"></a>Opprette en jobb

Hvis du vil opprette en jobb, gjør du følgende:

1. Gå til **Jobber**.
2. Velg **Ny**.
3. I **Stillingsbetegnelse**-feltet angir du en stilling. I **Rolle**-feltet angir du rollen din.
4. Velg en mal i **Mal**-feltet. Et alternativ er å velge **Hopp over**. Hvis du velger **Hopp over**, brukes malen som er merket som standardmalen.

    Hvis dokumentet skal gå gjennom en godkjenningsprosess, velger du en mal der **Godkjenningsprosess**-feltet er satt til **Standard**.

5. Angi detaljene for jobben i **Detaljer**-kategorien. Felt for **tittel**, **jobbeskrivelse** og **plassering** er nødvendige.
6. Velg **Lagre**.
7. I **Ansettelsesteam**-kategorien legger du til en ansettelsesansvarlig, rekrutterer eller intervjuer.
8. Velg **Lagre**.
9. I **Prosess**-kategorien legger du til eller fjerner stadier etter behov:

    - Hvis du vil legge til et stadium, kan du velge **+ Nytt stadium**.
    - Hvis du vil fjerne et stadium, hold pekeren over det stadiet du skal fjerne, og velg deretter papirkurv-knappen som vises.

        > [!NOTE]
        > Stadiene kundemne, søknad og tilbud kan ikke fjernes.

10. Legge til eller fjerne aktiviteter etter behov:

    - Hvis du vil legge til en aktivitet, drar du den fra listen til høyre til det aktuelle stadiet. Du kan også dobbeltklikke aktiviteten, og deretter velge stadiet du vil legge den til.
    - Hvis du vil fjerne en aktivitet, utvider du aktiviteten, og velger deretter papirkurv-knappen på overskriften for aktiviteten.

11. Velg **Lagre**.
12. Hvis du har valgt å bruke en godkjenningsprosess, gjør du følgende:

    1. Velg **+ Legg til godkjenner**, og angi deretter en bruker som har en Azure AD-konto. Du kan legge til flere godkjennere.
    2. Velg **Send til godkjennere**.

    Feltet **Jobbstatus** for jobben er satt til **Venter**. Når verdien til **Jobbstatus**-feltet endres til **Godkjent**, kan jobben aktiveres.

13. Velg **Aktiver** for å aktivere jobben.
14. Hvis du vil postere jobben, kan du gå til **Posteringer** og deretter velge **Poster nå** under Talent Careers-området eller LinkedIn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]