---
title: Angi og sammenligne tilbudsforespørsler og inngå kontrakter
description: Dette emnet forklarer hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir kontrakten til én av leverandørene.
author: RichardLuan
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable, PurchTablePart, PurchRFQCompareLinePrices, PurchRFQCompareRFQ
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f14b95a71397bf5879c97654620e1d4c22a1149
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016684"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Angi og sammenligne tilbudsforespørsler og inngå kontrakter

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du registrerer svar på en tilbudsforespørsel, poengsum og sammenligner bud, og deretter gir kontrakten til én av leverandørene. Du kan bruke prosedyren i **USMF**-demodatafirmaet.

Før du starter denne prosedyren, må du ha en tilbudsforespørsel som har to linjer og som er sendt til minst to leverandører. For å opprette denne tilbudsforespørselen må du fullføre prosedyren [Opprette en tilbudsforespørsel](create-request-quotation.md). Poengkriterier må også defineres før du kan fullføre denne prosedyren.

Du kan angi budet som en leverandør eller en innkjøpsansvarlig. Hvis du vil ha mer informasjon, se [Definere og vedlikeholde leverandørsamarbeid](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Angi et svar som en leverandør

1. Velg **Leverandørbud** på instrumentbordet.
2. I listen **Invitasjoner til nytt bud** finner du en tilbudsforespørsel som nettopp ble sendt. Velg tilbudsforespørselen for å gå gjennom forespørselen.
3. Velg **Vedlegg i tilbudsforespørsel** for å se gjennom vedlegg som er lagt til.
4. Velg **Bud** hvis du vil at feltene skal være redigerbare. Legg merke til at **Bud pågår**-feltet er satt til **Leverandør oppdaterer**.
5. I hodet og linjene angir du verdiene fra budsvaret.
6. Hvis det skal legges til vedlegg i budet, velger du **Vedlegg i bud**.
7. Velg hurtigfanen **Budveiledningselementer** for å vise om noen dokumenter er nødvendige.
8. Velg hurtigfanen **Endringer** for å vise om tilbudsforespørselen er endret.
9. Velg hurtigfanen **Spørreskjema**. Alle spørreskjemaer som vises her, må besvares.
10. Velg hurtigfanen **Linjedetaljer** for å vise utvidet informasjon om linjen.
11. Velg **Tilbakestill fra tilbudsforespørsel** bare hvis du må tilbakestille verdiene som er angitt i de opprinnelige tilbudsforespørselsverdiene.
12. Du kan når som helst lagre budet og utføre mer behandling senere, forutsatt at utløpsdatoen og -tidspunktet ikke er passert. I dette tilfellet kan du finne budet i listen **Bud som utføres** i arbeidsområdet **Leverandørbud**.
13. Når budet er klart til å sendes, velger du **Send**. Velg **Avslå** hvis du ikke vil by. Sendte bud er tilgjengelige i listen **Sendte bud** i arbeidsområdet **Leverandørbud**.  
14. Når budet er sendt, kan du tilbakekalle det når som helst før utløpsdatoen og -klokkeslettet. Legg merke til at når et bud blir tilbakekalt, behandles det ikke som sendt. Når budet godtas eller avvises av innkjøpsavdelingen, vises det i listen **Tildelte bud** eller **Tapte bud** i arbeidsområdet **Leverandørbud**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Angi et svar fra en leverandør som innkjøpsansvarlig

1. Kontroller at tillatelsen for å redigere leverandørbud er definert. Gå til **Innkjøp og leverandører** \> Oppsett \> Parametere for innkjøp og leverandører. I fanen **Tilbudsforespørsler** setter du **Innkjøper kan redigere bud fra leverandører** til **Ja**.
2. Gå til **Innkjøp og leverandører \> Tilbudsforespørsler \> Alle tilbudsforespørsler**.
3. Velg en tilbudsforespørsel som har statusen **Sendt**, og velg deretter koblingen i feltet **Tilfelle for tilbudsforespørsel**.
4. Velg **Behandle svar**. Siden som vises, viser en tilbudsforespørsel for hver leverandør som ble invitert til å by.
5. Velg en tilbudsforespørsel som ikke er besvart. (Feltet **Svarfremdrift** må settes til **Ikke startet**.)
6. Velg **Rediger \> Rediger svar på tilbudsforespørsel**. Siden **Forespørselssvar** vises. Som innkjøpsansvarlig kan du nå legge inn svaret på vegne av leverandøren. Legg merke til at **Bud pågår**-feltet er satt til **Innkjøper oppdaterer**.  
7. Angi buddataene. Når du er ferdig, velg **Send**.

## <a name="score-the-bids"></a>Gi bud poengsum

1. På siden **Alle tilbudsforespørsler** velger du tilbudsforespørselssaken som du vil gi poeng for svar for.
2. Velg **Behandle svar**.
3. Velg svaret som skal gis poeng for.
4. Velg **Hode**, slik at du kan vise poengsummen for budet.
5. I hurtigfanen **Budresultat** angir du et tall i feltet **Poengsum** for ett av poengkriteriene. Hvis du holder musepekeren over et poengkriterium, viser et verktøytips området som poengsummen må være innenfor. Du kan angi et tall mellom 1 og 5 for poengkriterier i denne demoen.  
6. Gjenta trinn 5 for et annet poengkriterium.
7. Hvis saken for tilbudsforespørsel har et spørreskjema som ble sendt til leverandørene, kan du skrive inn leverandørsvarene i hurtigfanen **Spørreskjemaer**.
8. Lukk siden.
9. Gjenta trinn 1 til 8 for alle de andre budene.

## <a name="compare-the-replies"></a>Sammenligne svarene

1. Velg **Sammenlign svar** i fanen **Generelt** i handlingsruten.
2. Angi et tall i **rangeringsfeltet**.  
    - Denne siden viser bud sammen med overskrifts- og linjeinformasjon, og også den samlede poengsummen på overskriftsnivå. Du kan sammenligne linjene ved å sortere rutenettet, slik at tilsvarende linjer er ved siden av hverandre. Følgende informasjon er også inkludert:
    - **Antall** – Tilbudt antall fra leverandøren. Dette antallet kan være ulikt antallet som er angitt i tilbudsforespørselen.
    - **Nettobeløp** – Prisen som leverandøren tilbyr for varene på linjen, minus rabatter.
    - **Avvik** – Antall dager som leveringsdatoen i budhodet eller -linjen avviker fra den ønskede leveringsdatoen i tilbudsforespørselshodet eller -linjen. Du kan angi en rangering for hvert bud.  
3. Velg overskriftslinjen for det andre budet du vil rangere.
4. Angi et tall i **rangeringsfeltet**.
5. Velg **Lagre**.

## <a name="reject-a-bid"></a>Avvise et bud

1. Velg overskriftslinjen for budet du vil avvise. Du kan godta, avvise eller returnere bare ett bud eller linjene i bare ett bud om gangen.
2. Merk av for **Merk**.  
    - Hvis du merker av for **Merk** i overskriften til budet, vil alle linjene også merkes av. Hvis du bare vil avvise eller godta noen av linjene i budet, kan du merke bare disse linjene. Du kan også godta én leverandørs bud for noen linjer i en tilbudsforespørsel, og deretter gi andre linjer i tilbudsforespørselen til en annen leverandør. Du må imidlertid utføre ett bud om gangen.  
    - Hvis det finnes alternative linjer, kan du godta enten den opprinnelige budlinjen eller den alternative, men ikke begge.  
3. Velg **Avvis**.
4. Velg **Parametere**, og skriv deretter inn eller velg en årsak for avslag av budet i **Avvisningsårsak**-feltet. Årsaken lagres i svaret.  
5. Velg **OK**.
6. Velg **OK**.

## <a name="accept-a-bid"></a>Godta et bud

1. Velg budet du vil godta, og velg deretter koblingen i **Tilbudsforespørsel**-feltet. Hvis du er på siden **Sammenlign svar på tilbudsforespørsel**, er det merkede budet som har fokus, budet som systemet vil vurdere under godkjenningshandlingen. Du kan bare godta linjer fra ett bud om gangen.  
2. Velg **Svar** i handlingsruten.
3. Velg **Godta**. Hvis du har merket bare bestemte linjer, vil Godta-handlingen bare ta med disse linjene. Hvis du vil godta alle linjene i budet, trenger du ikke merke linjene.  
4. Velg **Parametere**, og skriv deretter inn eller velg en årsak for å godta budet i **Årsak til aksept**-feltet. Årsaken lagres i budet.  
5. Velg **OK**.
6. Velg **OK**. Når du velger **OK**, genereres en bestilling basert på linjene som er inkludert i godkjenningen av tilbudsforespørselen. Hvis det finnes andre bud som ikke er behandlet (godkjent, avvist eller returnert), vil systemet be deg om å avvise dem.  

## <a name="view-the-purchase-order-that-is-generated"></a>Vise bestillingen som er generert

Velg **Bestilling** i fanen **Generelt** i handlingsruten. Siden som vises, angir bestillingen som ble generert da du godtok budet.
