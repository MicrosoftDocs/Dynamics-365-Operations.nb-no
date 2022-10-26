---
title: Konfigurasjonsgrupper for Invoice Capture-løsning
description: Denne artikkelen gir generell informasjon om konfigurasjonsgrupper i Invoice capture-løsningen.
author: sunfzam
ms.date: 09/28/2022
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
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691218"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Konfigurasjonsgrupper for Invoice Capture-løsning

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Brukere kan styre listen over fakturafelt og den manuelle kontrollinnstillingen for juridiske enheter ved hjelp av konfigurasjonsgrupper. Brukere kan definere fakturakonfigurasjoner for forskjellige juridiske enheter i grupper. Alle juridiske enheter i samme konfigurasjonsgruppe bruker de samme fakturafeltene og innstillingen for manuell kontroll.

## <a name="manage-configuration-groups"></a>Oppretthold konfigurasjonsgrupper

Hvis du vil administrere konfigurasjonsgrupper ved å bruke appen, går du til **Oppsett** og velger deretter **Systemoppsett \> Definer konfigurasjonsgruppekomponent**.

På siden **Definer konfigurasjonsgrupper** viser hovedkategorien listen over konfigurasjonsgrupper som er definert. Det viser også en standard konfigurasjonsgruppe. For hver konfigurasjonsgruppe følger du handlinger som er tilgjengelige.

- **Kopier en konfigurasjonsgruppe** – Du kan opprette en ny konfigurasjonsgruppe ved å duplisere en eksisterende gruppe. Den nye gruppen har de samme verdiene som den opprinnelige gruppen for alle feltene unntatt **Gruppenavn** og **Gruppebeskrivelse**. Velg **OK** når konfigurasjonsgruppen er duplisert .
- **Slett konfigurasjonsgrupper** – Hvis du vil slette en konfigurasjonsgruppe, velger du den og velger deretter **Slett**.

    > [!NOTE]
    > Standardkonfigurasjonsgruppen kan ikke slettes.

- **Rediger en konfigurasjonsgruppe-ID** – Hvis du vil redigere IDen til en konfigurasjonsgruppe, velger du feltet **Gruppe-ID** og oppdaterer verdien. Gruppe-IDen må ikke inneholde mellomrom eller spesialtegn, og den må ikke overskride 20 tegn.

    > [!NOTE]
    > Verdien i feltet **Gruppe-ID** kan bare oppdateres én gang.

- **Rediger en konfigurasjonsgruppebeskrivelse** – Hvis du vil redigere beskrivelsen til en konfigurasjonsgruppe, velger du feltet **Beskrivelse** og oppdaterer verdien.
- **Endre innstillingen for manuell gjennomgang** – Brukere kan bestemme om en faktura må gjennomgås manuelt. Hvis du vil endre innstillingen for manuell gjennomgang, velger du alternativet **Trenger manuell gjennomgang**. Følgende alternativer er tilgjengelige:

    - **Alltid manuell gjennomgang** – Velg dette alternativet hvis fakturaer i konfigurasjonsgruppen alltid krever manuell gjennomgang.
    - **For feil og advarsler** – Velg dette alternativet hvis fakturaer som inneholder feilmeldinger eller advarselsmeldinger, må gjennomgås manuelt.
    - **For feil** – Velg dette alternativet hvis fakturaer som inneholder feilmeldinger, må gjennomgås manuelt.

- **Endre innstillingen for konfidensresultat** – Konfidensresultatet er metadata som Invoice Capture-løsningen gir for å rapportere nøyaktigheten til gjenkjennede fakturadata. Jo høyere poengsum er, desto mer nøyaktig kan de gjenkjennede dataene være. Ved hjelp av konfigurasjonen kan brukere definere når det kreves manuell gjennomgang basert på den ønskede poengsummen. Brukere kan endre konfidensresultatet for fakturaer. Hvis du vil oppdatere innstillingen for konfidensresultat, velger du feltet for **konfidensresultat** og oppdaterer verdien.

    Det finnes to varslingstyper for konfidensresultater:

    - **Advarsel** – Fakturafelt som har riktige konfidensresultater over advarselsterskelen, anses som riktige. Advarselsterskelen må være større enn feilterskelen og mindre enn 100.
    - **Feil** – Fakturafelt som har riktige konfidensresultater under feilterskelen, anses som mislykket. Feilmeldinger vises for brukeren. Feilterskelen må være større enn 0 (null) og mindre enn varselsterskelen. Det vises advarselsmeldinger for fakturafelt som har konfidensresultat mellom advarselsterskelen og feilterskelen.

- **Administrere fakturafelt** – Brukere kan styre listen over fakturafelt som vises i visningsprogrammet for side-ved-side. I fanen **Administrasjon av fakturafelt** velger du tannhjulsymbolet, og velg fakturafeltene som skal legges til, og velg deretter **Lagre**. De valgte feltene blir lagt til i listen. Hvis du vil fjerne et fakturafelt fra listen, velger du **Fjern** i feltet.

### <a name="manage-file-filters-optional"></a>Administrere filfiltre (valgfritt)

Ved hjelp av filfiltre kan brukere definere flere filtre for innkommende fakturafiler. Filer som ikke oppfyller filterkriteriene, mottas og vises i listen **Mottatte filer**, men de vil vise filvalideringsfeil. Denne virkemåten er forskjellig fra virkemåten for filtre som er definert i kanalen. For de filtrene blir filer som ikke oppfyller kriteriene, ikke mottatt i det hele tatt. Brukere kan gå gjennom de innkommende filene og avgjøre om hver fil er en ikke-gyldig faktura, og de kan forelde filen eller inkludere den manuelt for gjenkjenning og inkludering i oppfangede fakturaer.

Når Invoice capture-løsningen er installert, defineres et standard filfilter. Dette filfilteret er globalt. Hvis du vil ha ulike filterinnstillinger, kan du oppdatere standardfilteret. Hvis et felt er obligatorisk, velger du **Nødvendig**. 

### <a name="accepted-file-size"></a>Godkjent filstørrelse

Du kan velge den godtatte filstørrelsen.

> [!NOTE]
> Filer som er større enn 20 480 kilobyte (kB), støttes ikke.

### <a name="supported-file-types"></a>Støttede filtyper

Følgende filtyper støttes for øyeblikket:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF
