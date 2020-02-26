---
title: Opprett en fritekstfaktura
description: Dette emnet forklarer hvordan du oppretter fritekstfakturaer.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 909dd5bcaf1fa3b82adb44d265e312f9acc607d2
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000076"
---
# <a name="create-a-free-text-invoice"></a>Opprett en fritekstfaktura

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter fritekstfakturaer. For denne fremgangsmåten må du bruke demonstrasjonsfirmaet **USMF**.

## <a name="create-a-free-text-invoice"></a>Opprett en fritekstfaktura

1. Gå til **Kunder \> Fakturaer \> Alle fritekstfakturaer**.
2. Velg **Ny**.
3. Velg en verdi i **Kundekonto**-feltet.

    * Kontoen som velges som kundekonto, brukes som standard som fakturakontoen.
    * Regnskapsstatusen starter med **Pågår** hvis fakturaen ikke er postert.
    * Fakturanummeret tilordnes når fakturaen posteres.
    * Hvis du bruker mandater fra felles eurobetalingsområde (SEPA), fylles avtalegiromandatet automatisk ut når du velger kundekontoen.

4. Angi en verdi i feltet **Beskrivelse**.
5. Angi et kontonummer uten dimensjoner i **Hovedkonto**-feltet. Du setter inn dimensjoner senere i dette emnet.

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
    * Velg **Ja** for å skrive ut fakturaen.
    * Velg **Ja** for å postere fakturaen. Du kan skrive ut fakturaen uten å postere den.

19. Velg **OK**.

## <a name="copy-lines"></a>Kopier linjer
Hvis du vil kopiere linjer på en fritekstfaktura, velger du én eller flere linjer og velger deretter **Kopier valgte linjer**. Du kan angi hvor mange kopier du vil lage, og du kan også kopiere notater og vedlegg. Du kan kopiere distribusjonene eller la dem bli opprettet på nytt når du posterer.

Når du har kopiert linjene, kan du redigere informasjonen etter behov.

## <a name="create-a-free-text-invoice-from-a-template"></a>Opprette en fritekstfaktura fra en mal
Du kan opprette en fritekstfaktura fra en mal. Når du velger **Ny fra mal** i kategorien **Faktura**, kan du velge et malnavn og kundekontoen for den nye fritekstfakturaen. Standardverdier, for eksempel betalingsbetingelsene og betalingsmåten, kan fylles inn automatisk fra kunden, eller du kan bruke verdier som ble lagret i malen.

Det opprettes en ny fritekstfaktura, og du kan redigere verdiene etter behov.
