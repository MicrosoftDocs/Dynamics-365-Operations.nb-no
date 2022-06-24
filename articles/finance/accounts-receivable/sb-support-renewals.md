---
title: Støtte og fornyelser
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker støtte- og fornyelsesprosessen på salgsordrer til å opprette en faktureringsplan for fornyelse av varer.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: b40e0136883d909755480a3ce101627297bd9ffb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896528"
---
# <a name="support-and-renewals"></a>Støtte og fornyelser 

Denne artikkelen beskriver hvordan du angir støttevarer eller fornyelsesvarer når du registrerer salgsordrer. Disse varene brukes til å beregne tilleggsbeløpet for den opprinnelige støttekontrakten og/eller fornyelsesbeløpet som brukes når det opprettes en faktureringsplan i abonnementsfakturering. Firmaet ditt selger for eksempel en server til en kunde, og du tilbyr et sikkerhetskopiabonnement for data det første året, og alternativet for å fornye abonnementet hvert år. *Støttevaren* er abonnementet for det første året, og *fornyelsesvaren* er fornyelsen for hvert etterfølgende år.

Du kan angi informasjon for støttekontrakten, fornyelseskontrakten eller begge deler. Når du angir støttekontraktinformasjon, blir bare støttevaren lagt til i salgsordren. Når du angir informasjon om fornyelse av kontrakt, brukes fornyelsesvaren til å opprette en faktureringsplan.

## <a name="support-and-renewal-setup"></a>Oppsett av støtte og fornyelse

På siden **Støtte- og fornyingsnivåer** kan du konfigurere ulike støttenivåer for støtte og fornyelse av varer. Støtten eller fornyelsen kan være en prosent av det opprinnelige varebeløpet, eller det kan være et standardbeløp.

Du kan velge standard støttenivåer på siden **Faktureringsparametere for regelmessig kontrakt**.

Et firma kan for eksempel tilby følgende støtte- og fornyelsesnivåer.

| Støttenivå | Støtteprosent | Fornyingsprosent |
|---|---|---|
| Ubegrenset | 40 % | 30 % |
| Gull | 25 % | 18 % |
| Sølv | 20 % | 14 % |
| Bronse | 15 % | 10 % |

Hvis du vil opprette et støtte- eller fornyelsesnivå, gjør du følgende.

1. På siden **Støtte- og fornyingsnivåer** velger du **Ny**.
2. Angi et unikt navn i feltet **Støttenivå**.
3. Angi en beskrivelse i **Beskrivelse**-feltet.
4. I feltet **Beregningsmåte for støtte** velger du beregningsmåten for støtte. Hvis du velger **Prosent**, angir du en støtteprosent i feltet **Støtteprosent**.
5. I feltet **Beregningsmåte for fornying** velger du beregningsmåten for fornying. Hvis du velger **Prosent**, angir du en fornyingsprosent i feltet **Fornyingsprosent**.
6. Velg **Lagre**.

### <a name="fields"></a>Felt

Siden **Støtte- og fornyingsnivåer** inneholder følgende felter.

| Felt | Beskrivelse |
|---|---|
| Støttenivå | En unik identifikator for støtte- eller fornyingsnivået (for eksempel **Gull** eller **Sølv**). |
| Beskrivelse | En beskrivelse av støtte- eller fornyelsesnivået. |
| Beregningsmåte for støtte | Velg støtteberegningsmetoden for nivået: **Prosent** eller **Standardbeløp**. |
| Støtteprosent | Hvis du valgte **Prosent** som støtteberegningsmetode, angir du prosenten som brukes til å beregne prisen på støttevaren. Hvis du valgte **Standardbeløp** som beregningsmetode, angis beløpet når transaksjonen opprettes. |
| Beregningsmåte for fornying | Velg fornyingsberegningsmetoden for nivået: **Prosent** eller **Standardbeløp**. |
| Fornyingsprosent | Hvis du valgte **Prosent** som fornyingssberegningsmetode, angir du prosenten som brukes til å beregne prisen på fornyingsvaren. Hvis du valgte **Standardbeløp** som beregningsmetode, angis beløpet når transaksjonen opprettes. |

## <a name="support-and-renewal-process"></a>Støtte- og fornyingsprosess

Funksjonaliteten for støtte og fornying kan bruke ulike støttenivåer på varer og oppdatere fornyingsinformasjon i abonnementsfakturering.

Før du bruker funksjonaliteten for støtte og fornying, må følgende oppgaver fullføres.

1. På siden **Støtte- og fornyingsnivåer** oppretter du minst ett støtte- eller fornyingsnivå.
2. På siden **Vareoppsett** knytter du til en vare med støtte- og fornyelsesvarer. Denne oppgaven er bare nødvendig hvis du vil definere standardverdier for støtte- og/eller fornyelsesvarer.
3. På siden **Faktureringsparametere for regelmessig kontrakt** angir du standardinnstillingene for støtte og fornying for nye faktureringsplaner.

Følg denne fremgangsmåten for å bruke forskjellige støttenivåer for varer og oppdatere fornyelsesinformasjon.

1. Opprett en salgsordre på siden **Alle salgsordrer**.
2. Legg til en vare på hurtigfanen **Salgsordrelinjer**.
3. På **Faktura**-fanen velger du **Støtte og fornying \> Legg til støtte og fornying**.
4. På siden **Støtte- og fornyingsprosess** blir hodedelen oppdatert med innstillingene fra siden **Faktureringsparametere for regelmessig kontrakt**. Disse verdiene gjelder for alle støtte- og fornyelsesvarer. (Hvis for eksempel faktureringsfrekvensen er satt til **Årlig**, har alle salgslinjer som opprettes med en fornyelsesvare, en årlig frekvens.) Hvis du vil knytte salgsordren til en eksisterende faktureringsplan, velger du en verdi i feltet **Faktureringsplannummer**.
5. Hvis du vil endre startdatoen for støtte eller fornyelse, setter du alternativet **Overstyr startdato** til **Ja**.
6. Hvis du vil legge til eller redigere støttevaren, merker du av for **Støtte**, og deretter angir du en støttevare i feltet **Støttevare**. Varen legges til i salgsordren.
7. Hvis du vil legge til eller redigere fornyingsvaren, merker du av for **Fornying**, og deretter angir du en fornyingsvare i feltet **Fornyingsvare**. Når salgsordren er fakturert, opprettes det en faktureringsplan som inkluderer varen.
8. Velg **OK**.
9. På **Generer**-fanen velger du **Faktura**. Når salgsordren er postert, blir faktureringsplanen opprettet. Et varsel med informasjon om faktureringsplanen vises i meldingsdetaljene.
10. På listesiden **Alle/Aktive faktureringsplaner** velger du faktureringsplannummeret for å se gjennom detaljene om faktureringsplanen på siden **Faktureringsplaner**.
11. På hurtigfanen **Faktureringsplanlinjer** velger du **Støtte og fornying** for å se gjennom detaljene til linjene som ble opprettet.

> [!NOTE]
> Hvis startdatoen for fornying av en faktureringsplanlinje må endres, kan du redigere **Startdato**-verdien for linjen på siden **Faktureringsplaner**. Når du åpner siden **Vis faktureringsdetaljer** for linjen, oppdateres feltet **Startdato for fakturering** med den nye datoen. Verdien **Sluttdato for fakturering** omberegnes på grunnlag av faktureringsfrekvensen. Startdatoen for fornying kan bare oppdateres hvis den første fakturaen for faktureringsplanen for fornyingen ikke er opprettet og postert. Etter at den første fakturaen er opprettet og postert, kan du ikke redigere startdatoen.

Støtte- og fornyingsprosessen er bare tilgjengelig for salgsordren. Når du legger til støtte og fornying av varer i en salgsordre, kan du opprette en ny faktureringsplan eller legge til fornyingsvaren i en eksisterende faktureringsplan.

## <a name="support-and-renewal-audit"></a>Støtte- og fornyingsrevisjon

På siden **Støtte - og fornyingsrevisjon** kan du se gjennom detaljene i faktureringsplanlinjene som er opprettet fra fornyingsvaren i en salgsordre. Dette alternativet er tilgjengelig når varen på faktureringsplanlinjen er en fornyingsvare.

Følg denne fremgangsmåten for å redigere informasjon om støtte og fornying for en faktureringsplanlinje.

1. På siden **Alle faktureringsplaner** velger du faktureringsplannummeret.
2. Velg en linje i delen **Faktureringsplanlinjer**, og velg deretter **Støtte og fornying**.
3. Gå gjennom all informasjon for støtte- eller fornyingsvaren.
4. Foreta eventuelle endringer som kreves for støttenivået, fornyingsprosenten eller beløpet, og angi deretter en verdi i feltet **Årsak til endring**.
5. Velg **Prosess**.

### <a name="fields"></a>Felt

Siden **Støtte- og fornyingsrevisjon** inneholder følgende felter.

| Felt | Beskrivelse |
|-------|-------------|
| Varenummer | Varenummeret for faktureringsplanlinjen. |
| Produktnavn | Produktnavnet. |
| Støtteplannivå | Vis eller endre støttenivået for fornyingsvaren. |
| Fornyingsprosent | Angi fornyingsprosenten som brukes når enhetsprisen beregnes for en fornyingsvare i en faktureringsplan. |
| Fornyingsbeløp | Angi fornyingsbeløpet som brukes når enhetsprisen beregnes for en fornyingsvare i en faktureringsplan. |
| Årsak til endringen | Angi årsaken til endringen av støtte- og fornyingsinformasjonen. Du må angi en årsak når du endrer verdien for **Fornyingsprosent**, **Fornyingsbeløp** eller **Støtteplannivå**. |
| Opprinnelig salgsvare | Det opprinnelige salgsvarenummeret fra salgsordren. |
| Opprinnelig nettobeløp | Det opprinnelige nettobeløpet for varen. |
| Opprinnelig støttenivå | Det opprinnelige støttenivået for varen. |
| Opprinnelig fornyingsprosent | Den opprinnelige fornyingsprosenten for varen. |
| Opprinnelig fornyingsbeløp | Det opprinnelige fornyingsbeløpet for varen. |
| **Rutenett** | |
| Opprinnelig støttenivå | Det forrige støttenivået. |
| Opprinnelig fornyingsprosent | Den forrige fornyingsprosenten. |
| Opprinnelig fornyingsbeløp | Det forrige fornyingsbeløpet. |
| Endret av | Brukernavnet til brukeren som foretok endringen. |
| Endringsdato og -klokkeslett | Datoen da endringen inntraff. |
| Årsak | Årsaken til endringen. |
