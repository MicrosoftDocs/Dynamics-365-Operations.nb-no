---
title: Opprett en fritekstfaktura
description: Denne artikkelen forklarer hvordan du oppretter fritekstfakturaer.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 87dc6334baa83ace23b77d94da4d1e464cb0b574
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878167"
---
# <a name="create-a-free-text-invoice"></a>Opprett en fritekstfaktura

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du oppretter fritekstfakturaer. For denne fremgangsmåten må du bruke demonstrasjonsfirmaet **USMF**.

## <a name="create-a-free-text-invoice"></a>Opprett en fritekstfaktura

1. Gå til **Kunder (eller salgsfinanskonto) \> Fakturaer \> Alle fritekstfakturaer**.
2. Velg **Ny**.
3. Velg en verdi i **Kundekonto**-feltet.

    * Kontoen som velges som kundekonto, brukes som standard som fakturakontoen.
    * Regnskapsstatusen starter med **Pågår** hvis fakturaen ikke er postert.
    * Fakturanummeret tilordnes når fakturaen posteres.
    * Hvis du bruker mandater fra felles eurobetalingsområde (SEPA), fylles avtalegiromandatet automatisk ut når du velger kundekontoen.

4. Angi en verdi i feltet **Beskrivelse**.
5. Angi et kontonummer uten dimensjoner i **Hovedkonto**-feltet. Du setter inn dimensjoner senere i denne artikkelen.

    Du kan også angi ett eller flere tegn for hovedkontoen og bruke oppslaget til å finne kontoen.

6. Velg hurtigfanen **Linjedetaljer** for å legge til dimensjoner i hovedkontoen.
7. Velg kategorien **Finansdimensjonslinje**.

    * Dimensjonene gjelder bare for den valgte linjen.
    * Mva-gruppen fylles ut av kunden. Hvis kunden ikke har en mva-gruppe, brukes mva-gruppen fra hovedkontoen.
    * Mva-gruppen for varer fylles ut fra hovedkontoen. Hvis hovedkontoen ikke har en mva-gruppe for varer, brukes mva-gruppen for varer som er angitt i mva-parameterne i Økonomimodul.

8. Du kan også angi et tall i feltet **Antall**.
9. Valgfritt: Angi et tall i feltet **Enhetspris**.

    Beløpet beregnes som antallet ganger enhetsprisen. Du kan imidlertid overstyre dette ved å angi et beløp.

10. Hvis du vil vise merverdiavgiften som er beregnet for fakturaen, velger du **Merverdiavgift**.

    Du kan vise mva-beløpene på denne siden, eller du kan overstyre beløpene i kategorien **Justering**.

11. Velg **OK**.
12. Klikk **Tillegg** for å legge til et tillegg på fakturaen.
13. Skriv inn en verdi i **Tilleggskode**-feltet.
14. Angi et tall i **Gebyrverdi**-feltet.
15. Lukk siden.
16. Velg **Totaler** for å vise et sammendrag av fakturadetaljene og totaler.
17. Velg **Lukk**.
18. Velg **Poster** for å postere fakturaen. Du vil fortsatt ha mulighet til å avbryte før du faktisk bokfører.

    * Du kan endre tidspunktet for fakturautskrifter. Velg **Gjeldende** for å skrive ut hver faktura når den oppdateres. Velg **Etter** for å skrive ut når alle fakturaene er oppdatert.
    * Hvis du vil endre hvordan kundens kredittgrense kontrolleres før fakturaen er postert, kan du endre verdien i **Kredittmaks.type**-feltet.
    * Du kan velge å stoppe postering av fritekstfaktura når det oppstår en feil på fanen **Oppdateringer** på siden **Kundeparametere** (**Kunder > Oppsett > Kundeparametere**). Velg **Ja** for parameteren **Stopp postering av fritekstfakturaer ved første feil** for å stoppe posteringen av fritekstfakturaer når det oppstår en feil. Hvis du posterer i en bunke, vil en feil stoppe posteringsprosessen og bunkestatusen settes til **Feil**. Hvis du ikke velger dette alternativet, hopper posteringsprosessen over en faktura med en posteringsfeil, og vil fortsette å postere flere fakturaer. Hvis du posterer i en bunke, vil ikke en posteringsfeil hindre at andre fakturaer posteres. Bunkestatusen vil være **Avsluttet**. En detaljert posteringsprosessrapport vil være tilgjengelig for gjennomgang i loggen for bunkejobber.
    * Velg **Ja** for å skrive ut fakturaen.
    * Velg **Ja** for å postere fakturaen. Du kan skrive ut fakturaen uten å postere den.

19. Velg **OK**.

## <a name="copy-lines"></a>Kopier linjer
Hvis du vil kopiere linjer på en fritekstfaktura, velger du én eller flere linjer og velger deretter **Kopier valgte linjer**. Du kan angi hvor mange kopier du vil lage, og du kan også kopiere notater og vedlegg. Du kan kopiere distribusjonene eller la dem bli opprettet på nytt når du posterer.

Når du har kopiert linjene, kan du redigere informasjonen etter behov.

## <a name="create-a-free-text-invoice-from-a-template"></a>Opprette en fritekstfaktura fra en mal
Du kan opprette en fritekstfaktura fra en mal. Når du velger **Ny fra mal** i kategorien **Faktura**, kan du velge et malnavn og kundekontoen for den nye fritekstfakturaen. Standardverdier, for eksempel betalingsbetingelsene og betalingsmåten, kan fylles inn automatisk fra kunden, eller du kan bruke verdier som ble lagret i malen.

Det opprettes en ny fritekstfaktura, og du kan redigere verdiene etter behov.

## <a name="resetting-the-workflow-status-for-free-text-invoices-from-unrecoverable-to-draft"></a>Tilbakestiller arbeidsflytstatusen for fritekstfakturaer fra Uopprettelig til Utkast
En arbeidsflytforekomst som er stoppet på grunn av en uopprettelig feil, vil ha arbeidsflytstatusen **Uopprettelig**. Når statusen til en arbeidsflyt for en fritekstfaktura for en kunde er **Uopprettelig**, kan du tilbakestille den til **Utkast** ved å velge **Tilbakekall**. Du kan deretter redigere fritekstfakturaen for kunden. Denne funksjonen er tilgjengelig hvis parameteren **Tilbakestiller arbeidsflytstatusen for fritekstfakturaer fra Uopprettelig til Utkast** på siden **Funksjonsbehandling** er slått på.

Du kan bruke siden **Arbeidsflytlogg** for å tilbakestille arbeidsflytstatusen til **Utkast**. Du kan åpne denne siden fra **Fritekstfaktura** eller fra **Felles > Forespørsler > Arbeidsflyt**. Hvis du vil tilbakestille arbeidsflytstatusen til **Utkast**, velger du **Tilbakekall**. Du kan også tilbakestille arbeidsflytstatusen til **Utkast** ved å velge handlingen **Tilbakekall** på siden **Fritekstfaktura** eller **Alle fritekstfakturaer**. Når arbeidsflytstatusen er tilbakestilt til **Utkast**, blir den tilgjengelig for redigering på siden **Fritekstfaktura**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
