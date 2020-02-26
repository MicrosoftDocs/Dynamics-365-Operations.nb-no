---
title: Kostnadskonfigurasjon for behandling av distribuert ordre (DOM)
description: Dette emnet beskriver kostnadskonfigurasjon for DOM-funksjonaliteten i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004234"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Kostnadskonfigurasjon for behandling av distribuert ordre (DOM)

[!include [banner](../includes/banner.md)]

Organisasjoner vurderer flere kostnadskomponenter for å fastslå hvilken lokasjon som er best å oppfylle ordrer fra. Noen av disse kostnadskomponentene er knyttet til frakt, håndtering og emballasje. En kombinasjon av disse kostnadene beregnes for å bestemme oppfyllingslokasjonen.

Da den første gjentakelsen av behandling av distribuert ordre (DOM) i Dynamics 365 Commerce optimaliserte tilordningen av ordrer til oppfyllingslokasjoner, ble det bare tatt hensyn til avstand. Selv om avstand kan korreleres med kostnad, er det ikke det samme som kostnad. En leveranse til neste dag koster for eksempel mer enn tredagers leveranse eller sjudagers leveranse med samme avstand.

Med funksjonen for kostnadskonfigurasjon kan forhandlere definere og konfigurere ytterligere kostnadskomponenter som skal beregnes og tas hensyn til når den beste lokasjonen for oppfylling av ordrelinjer fastsettes.

Når kostnadskomponenter er konfigurert, bruker DOM-problemløseren bare disse kostnadsdefinisjonene for å fastslå den beste lokasjonen for ordreoppfyllelse. Den tar ikke hensyn til avstandskomponenten som kostnad. Men hvis ingen kostnadskomponenter er konfigurert, bruker DOM-problemløseren avstandskomponenten som kostnad for å fastslå den beste lokasjonen for ordreoppfyllelse.

## <a name="set-up-cost-components"></a>Konfigurere kostnadskomponenter

Du kan definere to hovedtyper av kostnadskomponenter i systemet: **Forsendelse** og **Annet**.

Begge kostnadskomponenttypene støtter flere beregningsgrunnlag, som vist i tabellen nedenfor.

<table>
<thead>
<tr>
<th>Type kostnadskomponent</th>
<th>Beregningsgrunnlag</th>
</tr>
</thead>
<tbody>
<tr>
<td>Forsendelse</td>
<td>
<ul>
<li>Enkel</li>
<li>Trinnvis</li>
</ul>
</td>
</tr>
<tr>
<td>Annet</td>
<td>
<ul>
<li>Salgsordre</li>
<li>Salgslinje</li>
<li>Lokasjon</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Kostnadskomponenttypen Forsendelse

Denne delen forklarer hvordan du definerer hver kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget for forsendelseskostnader. Den inneholder også informasjon om hvordan DOM-problemløseren bruker ulike kombinasjoner.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Type kostnadskomponent = Forsendelse og beregningsgrunnlag = Enkel

Hvis en kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget **Enkel** brukes, er forsendelseskostnaden for en leveringsmåte basert på enten en fast kostnad eller avstand.

Du må definere følgende felt for denne kombinasjonen:

- **Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.
- **Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.
- **Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall. Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.
- **Aktiv** – Angi om kostnadsfaktoren er aktiv. DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.
- **Firma** – Angi den juridiske enheten som kostnadsfaktoren er konfigurert for. Alle linjer i beregningskriteriene må være for samme juridiske enhet.
- **Leveringsmåter** – Angir leveringsmåtene som kostnaden er konfigurert for.
- **Beregningstype** – Angi hvordan kostnaden skal beregnes for en bestemt leveringsmåte. To beregningstyper støttes:

    - **Fast** – En fast kostnad brukes for leveringsmåten. Hvis du velger denne beregningstypen, definerer **Kostnad**-feltet den faste kostnaden.
    - **Per avstandsenhet** – Kostnaden for leveringsmåten beregnes som kostverdien som angis i **Kostnad**-feltet, multiplisert med avstanden mellom leveringsadressen og lokasjonene.

- **Kostnad** – Angi kostverdien som brukes sammen med **Beregningstype**-feltet, for å beregne kostnaden for en leveringsmåte.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Type kostnadskomponent = Forsendelse og beregningsgrunnlag = Trinnvis

Hvis en kombinasjon av kostnadskomponenttypen **Forsendelse** og beregningsgrunnlaget **Trinnvis** brukes, er forsendelseskostnaden for en leveringsmåte basert på enten en fast kostnad eller avstand. I denne kombinasjonen er avstanden imidlertid basert på et trinnvist avstandsområde.

Du må definere følgende felt for denne kombinasjonen:

- **Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.
- **Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.
- **Standardkostnad** – Angi kostnaden som skal brukes for en leveringsmåte hvis avstanden mellom leveringsadressen og lokasjonen ikke er innenfor noen av de trinnvise avstandene for leveringsmåten.
- **Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall. Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.
- **Aktiv** – Angi om kostnadsfaktoren er aktiv. DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.
- **Firma** – Angi den juridiske enheten som kostnadsfaktoren er konfigurert for. Alle linjer i beregningskriteriene må være for samme juridiske enhet.
- **Leveringsmåter** – Angir leveringsmåtene som kostnaden er konfigurert for.
- **Avstandstype** – Angi om definisjonen av trinnvis avstand er luftavstand eller veiavstand.
- **Avstandsenheter** – Angi enheten som den trinnvise avstanden måles i.
- **Avstand fra** – Angi startområdet for den trinnvise avstanden.
- **Avstand til** – Angi sluttområdet for den trinnvise avstanden.
- **Beregningstype** – Angi hvordan kostnaden skal beregnes for en bestemt leveringsmåte og trinnvis avstand. To beregningstyper støttes:

    - **Fast** – En fast kostnad brukes for leveringsmåten. Hvis du velger denne beregningstypen, definerer **Kostnad**-feltet den faste kostnaden.
    - **Per avstandsenhet** – Kostnaden for leveringsmåten og trinnvis avstand beregnes som kostverdien som angis i **Kostnad**-feltet, multiplisert med avstanden mellom leveringsadressen og lokasjonene.

- **Kostnad** – Angi kostverdien som brukes sammen med **Beregningstype**-feltet, for å beregne kostnaden for en leveringsmåte.

> [!NOTE]
> - Når du definerer trinnvise avstander, validerer systemet at det ikke er noen avstander som mangler eller overlapper.
> - Avstandstypen som brukes for en leveringsmåte, må være den samme for alle trinnvise avstander.

### <a name="other-cost-component-type"></a>Kostnadskomponenttypen Annet

Denne delen forklarer hvordan du definerer hver kombinasjon av kostnadskomponenttypen **Annet** og en annen kostnadstype for kostnader som ikke er forsendelseskostnader. Den inneholder også informasjon om hvordan DOM-problemløseren bruker ulike kombinasjoner.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Kostnadskomponenttype = Annet og andre kostnadstyper = Salgsordre

En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Salgsordre** brukes til å definere kostnader på salgsordrenivå som ikke er forsendelseskostnader.

Du må definere følgende felt for denne kombinasjonen:

- **Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.
- **Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.
- **Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall. Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.
- **Aktiv** – Angi om kostnadsfaktoren er aktiv. DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.
- **Kostnad** – Angi kostverdien for en kostnad på salgsordrenivå som ikke er forsendelseskostnad.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Kostnadskomponenttype = Annet og andre kostnadstyper = Salgslinje

En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Salgslinje** brukes til å definere kostnader på salgsordrelinjenivå som ikke er forsendelseskostnader.

Du må definere følgende felt for denne kombinasjonen:

- **Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.
- **Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.
- **Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall. Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.
- **Aktiv** – Angi om kostnadsfaktoren er aktiv. DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.
- **Kostnad** – Angi kostverdien for en kostnad på salgsordrelinjenivå som ikke er forsendelseskostnad.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Kostnadskomponenttype = Annet og andre kostnadstyper = Lokasjon

En kombinasjon av kostnadskomponenttypen **Annet** og den andre kostnadstypen **Lokasjon** brukes til å definere kostnader for en gruppe lokasjoner eller en enkelt lokasjon som ikke er forsendelseskostnader.

Du må definere følgende felt for denne kombinasjonen:

- **Kostnadsfaktor** – Angi en unik identifikator for kostnadsfaktoren.
- **Beskrivelse** – Angi navn og beskrivelse på kostnadsfaktoren.
- **Startdato** og **Sluttdato** – Du kan bruke disse feltene til å begrense kostnadsfaktoren til et bestemt datointervall. Hvis du lar disse feltene stå tomme, er kostnadsfaktoren gyldig på ubestemt tid.
- **Aktiv** – Angi om kostnadsfaktoren er aktiv. DOM tar bare hensyn til aktive kostnadsfaktorer som er knyttet til oppfyllingsprofilen.
- **Oppfyllelsesgruppe** – Angi gruppen med lokasjoner som kostnadene som ikke er forsendelseskostnader, defineres for.
- **Oppfyllelseslokasjon** – Angi lokasjonen som kostnadene som ikke er forsendelseskostnader, defineres for.

    > [!NOTE]
    > Du kan ikke angi en oppfyllelsesgruppe og en oppfyllelseslokasjon på samme linje for lokasjonsbaserte beregningskriterier.

- **Kostnad** – Angi kostverdien for en kostnad som ikke er forsendelseskostnad, på oppfyllelsesgruppenivå eller oppfyllelseslokasjonsnivå.

> [!IMPORTANT]
> Hvis DOM skal ta hensyn til disse kostnadene under kjøring, må du legge til kostnadsfaktoren i den relevante oppfyllelsesprofilen.
