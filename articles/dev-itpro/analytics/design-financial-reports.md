---
title: Vise og utforme finansrapporter
description: "Denne artikkelen inneholder øvelser som forklarer hvordan du viser og opprette finansrapporter for Microsoft Dynamics 365 for Finance and Operations."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86597a81b4dcfb14cbc88667fbb1db214133c6e5
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-design-financial-reports"></a>Vise og utforme finansrapporter

[!INCLUDE [banner](../includes/banner.md)]

Denne artikkelen inneholder øvelser som forklarer hvordan du viser og opprette finansrapporter for Microsoft Dynamics 365 for Finance and Operations. Finansrapportering består av en visningsopplevelse i Finance and Operations og en ettklikks rapportutforming som lar deg opprette og redigere økonomiske rapporter.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Øvelse 1: Generere og utforske en standard finansrapport
-----------------------------------------------------------

I denne øvelsen skal du generere og utforske en eksisterende standardrapport. Denne rapporten inneholder alle kontoene og også kontoegenskaper (attributter) for kontoene. Du skal drille ned i transaksjonsdetalj, bruke dimensjonsfiltre og endre valutaen i rapporten. Først skal vi oppdatere visningsrekkefølgen til dimensjoner for finansrapportering. Dermed kan du velge hvordan dimensjonene skal vises, og ikke bare når du utformer og viser finansrapporter.

1.  Gå til **Konfigurasjon av finansdimensjoner for programintegrering** under **Dimensjoner for kontoplan** i økonomimodulen.
2.  Flytt dimensjonene slik at de er i følgende rekkefølge:
    1.  Hovedkonto
    2.  Forretningsenhet
    3.  Kostsenter
    4.  Avdeling

    Obs!  De andre dimensjonene kan forbli i rekkefølgen de er i.
3.  Lagre dimensjonskonfigurasjonen. Deretter skal vi generere en rapport og utforske dataene i rapporten.
4.  Gå til **Finansrapporter** under **Forespørsler og rapporter** i økonomimodulen.
5.  Velg raden for rapporten kalt **FIN-detalj – standard**.
6.  Velg **Rediger**. Obs!  Du blir bedt om å laste ned ettklikks rapportutforming og om å logge på. Bruk legitimasjonen til å logge på.
7.  Endre basisåret til 2012, og velg **Generer**. Når en rapport genereres fra rapportdesigneren, åpnes den i en ny nettleserfane. Du kan enten utforske rapporten i den nye nettleserfanen, eller gå til den opprinnelige nettleserfanen din og åpne rapporten derfra ved å velge den fra listen over **Finansrapporter**.
8.  I den åpnede rapporten velger du ett av beløpene for å drille ned i kontodetaljen for rapporten.
9.  Når du er i kontodetalj, velger du en konto med data og **driller ned til transaksjonsnivå i rapporten**. På transaksjonsnivået i rapporten kan du se egenskapene (attributtene) som er inkludert i rapportutformingen. Avhengig av transaksjonen og kontoen kan noen eller alle attributtene vises.
10. Lukk transaksjonsnivået i rapporten.
11. Velg samme eller en annen konto, og **åpne bilagstransaksjoner**. Bilagstransaksjoner filtreres etter kombinasjonen av periode, år og konto + dimensjon for den valgte kontoen. Fra bilagstransaksjoner kan du utforske tilleggsinformasjon om transaksjonen.
12. Lukk bilagstransaksjoner. I en finansrapport kan du vise dataene enten for en annen periode og et annet år eller med andre attributter og dimensjoner brukt på dem. Du kan gjøre dette ved hjelp av **Rapportalternativer**.
13. Velg **Rapportalternativer**.
14. Velg **Legg til et dimensjonsfilter**, og velg **Forretningsenhet**.
15. Skriv inn 001 i feltet, og velg **OK**. Rapporten viser nå bare dataene for forretningsenhet 001. Dette er en tilpasset visning av rapporten, og visningen er ikke tilgjengelig for andre.
16. Lukk den filtrerte rapporten. Finansrapporter kan vises i en hvilken som helst valuta som er lagt til i Finance and Operations.
17. Velg **Valuta**, og velg deretter **EUR**. Rapporten vises nå i euro. Valutakoder eller valutasymboler som er inkludert i rapportutformingen, vises nå i valutaen som er brukt. Hvis ingen valutasymbol er definert for en valuta, vises ikke valutasymbolet.
18. Lukk rapporten **FIN-detalj**.
19. Lukk **Rapportutforming**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Øvelse 2: Legge til ytterligere kontoegenskaper i en rapportutforming
I denne øvelsen skal du endre en eksisterende standardrapport. Du skal oppdatere begge raddefinisjonene slik at de omfatter alle kontoene, og du skal oppdatere kolonnedefinisjonen slik at den inneholder kontoattributter. Når oppdateringene er fullført, skal du generere den nyopprettede rapporten og utforske den. Vi begynner i Finansrapporter-listen.

1.  Gå til **Finansrapporter** under Forespørsler og rapporter i økonomimodulen.
2.  Velg raden for rapporten kalt **Råbalansesammendrag – standard**.
3.  Velg **Rediger**. **Råbalansesammendrag – standard** åpnes i Rapportutforming.
4.  Velg **Fil**, **Lagre som**, og gi rapporten navnet Detaljert råbalanse med attributter. Obs!  Hver gang det opprettes en ny rapport i Rapportutforming, oppdateres Finansrapporter-listen i Finance and Operations.
5.  Fra rapportdefinisjonen velger du ikonet for raddefinisjon for å åpne **Råbalanse – standard raddefinisjon**.
6.  Lagre raddefinisjonen som **Detaljert råbalanse med attributter**
7.  Plasser markøren i rad 50, velg **Rediger** og deretter **Sett inn rader fra dimensjoner**. Du kan bruke Sett inn rader fra dimensjoner til å velge hvilke dimensjoner du vil ha i raddefinisjonen. I denne øvelsen skal vi bygge raddefinisjonen ved hjelp av Hovedkonto.
8.  Kontroller at **Hovedkonto** inneholder alle &-tegn, og velg **OK**. Raddefinisjonen inneholder nå alle hovedkontoene for den juridiske enheten USMF.
9.  Bla ned til rad 11110, og slett den.
10. Velg **--- (Understrek beløp)** i rad 11080.
11. Skriv inn **Totalt for alle kontoer** i kolonne B i rad 11140.
12. I kolonne C velger du **TOT** fra rullegardinlisten.
13. Skriv inn **50:11080** i kolonne D.
14. **Lagre** raddefinisjonen. Raddefinisjonen inneholder nå alle kontoene pluss en totalrad for å legge sammen alle kontoene. Nå skal vi oppdatere kolonnedefinisjonen for å ta med ytterligere kontoattributter.
15. Fra rapportdefinisjonen **Detaljert råbalanse med attributter** velger du ikonet for kolonnedefinisjon for å åpne kolonnedefinisjonen **Råbalansesammendrag – standard**.
16. Lagre kolonnedefinisjonen som **Detaljert råbalanse med attributter**. Kolonnedefinisjonen inneholder finansdatakolonner, en beskrivelseskolonne og beregningskolonner. Vi skal legge til attributtkolonner i kolonnedefinisjonen for å gi mer detaljert informasjon om kontoene.
17. Følgende attributter skal legges til i kolonnedefinisjonen:
    -   Journalnummer
    -   Journalbeskrivelse
    -   Transaksjonsdato
    -   Opprettet av
    -   Sist endret av

18. I kolonne I velger du **ATTR** som kolonnetype. Velg deretter **Journalnummer** som attributtkategorien.
19. Fortsett å legge til kolonner for de gjenstående attributtene.
20. I raden **Topptekst 2** legger du til beskrivelser for hver av de nye kolonnene som er lagt til.
21. Lagre kolonnedefinisjonen. Nå som raddefinisjonen og kolonnedefinisjonen er oppdatert, skal vi du legge dem til i rapportdefinisjonen.
22. Fra rapportdefinisjonen **Detaljert råbalanse med attributter** velger du Detaljert råbalanse med attributter for både raddefinisjonen og kolonnedefinisjonen.
23. Endre basisåret til **2012**.
24. **Lagre** rapportdefinisjonen, og **generer**. Når rapporten er generert og åpnes, kan du utforske den slik du gjorde i den første øvelsen. Drill ned i andre kontoer for å se hvordan de ytterligere attributtene vises.
25. Lukk rapporten **Detaljert råbalanse med attributter**.
26. Lukk **Rapportutforming**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Øvelse 3: Opprette en flerdimensjonal rapport ved hjelp av et rapporteringstre
I denne øvelsen skal du endre en eksisterende standardrapport. Du skal opprette et rapporteringstre og legge til en rapportdefinisjon for å produsere et resultatregnskap for kostsenter/avdeling. Når oppdateringene er fullført, skal du generere resultatregnskapet for kostsenter/avdeling og utforske rapporten ved å bruke rapporteringstreet. Vi begynner i Finansrapporter-listen.

1.  Gå til **Finansrapporter** under Forespørsler og rapporter i økonomimodulen.
2.  Velg raden for rapporten kalt **Resultatregnskap – standard**.
3.  Velg **Rediger**. **Resultatregnskap – standard** åpnes i Rapportutforming.
4.  På **Fil**-menyen velger du **Ny** og klikker deretter **Definisjon av rapporteringstre**
5.  På **Rediger**-menyen klikker du **Sett inn rapportenheter fra dimensjoner**...
6.  Fjern merket for alle dimensjoner unntatt **Kostsenter**.
7.  Klikk **Fra dimensjon**-feltet for kostsenterdimensjonen, skriv inn **007**, og trykk deretter Tab. I **Til dimensjon**-feltet skriver du inn **018**.
8.  **Lagre** det resulterende treet med navnet **Kostsentre etter avdeling**. Nå som rapporteringstreet er opprettet, skal du endre rapporteringstreet slik at det inneholder tre nye opprullede enheter: Markedsføring, Operasjoner og Detaljhandel.
9.  På **Vindu**-menyen klikker du **Kostsentre etter avdeling**. (Hvis rapporteringstreet er lukket, velger du det fra Definisjoner av rapporteringstre i navigasjonsruten.)
10. Velg enhet nummer to, **Varemesser**, og klikk ikonet **Sett inn rapportenhet**.
11. Dobbeltklikk enhetskolonnen i den tomme raden, og velg **USMF**.
12. Skriv inn **Markedsføring** i kolonne B og C.
13. Klikk enhet nummer fem, **Serviceoperasjoner**, og høyreklikk. Velg **Sett inn rapportenhet**.
14. Gjenta trinn 11.
15. Skriv inn **Operasjoner** i kolonne B og C.
16. Klikk enhet nummer tolv, **Utsalgssted**, og høyreklikk. Velg **Sett inn rapportenhet**.
17. Gjenta trinn 11.
18. Skriv inn **Detaljhandel** i kolonne B og C. Legg merke til at enhetene Markedsføring, Operasjoner og Detaljhandel viser samme nivå som de gjeldende opprullede enhetene. Nå skal de nye enhetene organiseres. Rapportenheter organiseres via høyreklikksalternativene for heving og senking eller ved å dra og slippe.
19. Kontroller at enhet tre, **Varemesser**, er aktiv, og høyreklikk.
20. Velg **Senk rapportenhet**. Legg merke til at enheten nå vises som underordnet **Markedsføring**.
21. Klikk enhet fire, **Markedsførings****kampanje**, og høyreklikk.
22. Velg **Senk rapportenhet**.
23. Klikk **Serviceoperasjoner** i den grafiske visningen. Trykk og hold nede venstre museknapp mens du drar enheten opp til **Operasjoner**. Slipp venstre museknapp for å slippe enheten i operasjonens opprulling. Gjenta dette for **Produksjon, Kvalitetskontroll, Logistikk, Innkjøp og Administrasjon**.
24. Gjør **Utsalgssted**, **Super**, **Kjøpesenter** og **Nett** til underordnede for **Detaljhandel** ved å senke dem eller dra og slippe dem.
25. Lagre den resulterende omorganiseringen. Nå som vi har rapporteringstreet opprettet og organisert, kan det legges til i rapportdefinisjonen.
26. På **Vindu**-menyen velger du **Resultatregnskap – standard** for å åpne rapportdefinisjonen.
27. Klikk rullegardinlisten **Tretype**, og velg **Rapporteringstre**.
28. Klikk rullegardinlisten Tre, og velg **Kostsentre etter avdeling**.
29. Endre basisåret til **2012**, **lagre** endringene, og **generer** rapporten. Når rapporten er generert og åpnes, kan du utforske den.
30. Velg rullegardinlisten **Rapporteringstre** for å vise rapporteringsenhetene. Du kan også drille ned i en rad i rapporten for å se alle saldoene for alle enheter i rapporteringstreet.
31. Lukk **Resultatregnskap – standard**.
32. Lukk **Rapportutforming**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Øvelse 4: Opprette en konsolidert rapport ved hjelp av et organisasjonshierarki
I denne øvelsen skal du endre en eksisterende standardrapport. Du skal legge til et organisasjonshierarki i rapportdefinisjonen for å produsere et konsolidert resultatregnskap og balanse. Når oppdateringene er fullført, skal du generere den konsoliderte rapporten og utforske den ved å bruke rapporteringstreet. Vi begynner i Finansrapporter-listen.

1.  Gå til **Finansrapporter** under Forespørsler og rapporter i økonomimodulen.
2.  Velg raden for rapporten kalt **Balanse og resultatregnskap side ved side – standard**
3.  Velg **Rediger**. **Balanse og resultatregnskap side ved side – standard** åpnes i Rapportutforming.
4.  Velg **Fil** &gt; **Lagre som**, og gi rapporten navnet **Konsolidert balanse og resultatregnskap side ved side**.
5.  Endre basisåret til 2012.
6.  Klikk rullegardinlisten Tretype, og velg **Organisasjonshierarkier**.
7.  Klikk rullegardinlisten Tre, og velg **Contoso Holdings**.
8.  Lagre endringene, og generer rapporten. Velg alle rapportenheter hvis du blir spurt. Når rapporten er generert og åpnes, kan du utforske den.
9.  Velg **Rapportalternativer**.
10. Velg **Legg til et dimensjonsfilter**, og velg **Avdeling**.
11. Skriv inn **022** i feltet, og velg **OK**.
12. Lukk den filtrerte rapporten.
13. Velg rullegardinlisten **Rapporteringstre** for å vise rapporteringsenhetene. Du kan også drille ned i en rad i rapporten for å se alle saldoene for alle enheter i rapporteringstreet.
14. Lukk **Konsolidert balanse og resultatregnskap side ved side**.
15. Lukk **Rapportutforming**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>Øvelse 5: Opprette en side-ved-side-rapport for avdeling
I denne øvelsen skal du opprette en ny rapport. Rapporten er en side-ved-side-rapport med resultatregnskap for avdeling. Du skal bruke en eksisterende raddefinisjon, men opprette en ny rapportdefinisjon og en ny kolonnedefinisjon som bruker dimensjonsfiltre. Vi begynner i Finansrapporter-listen.

1.  Gå til **Finansrapporter** under Forespørsler og rapporter i økonomimodulen.
2.  Velg **Ny**. Rapportutforming åpnes med en tom rapportdefinisjon åpen. Først skal du opprette kolonnedefinisjonen.
3.  Opprett en ny kolonnedefinisjon ved å klikke **Fil**, **Ny** og deretter **Kolonnedefinisjon**.
4.  I **Kolonne A** velger du **DESC** for kolonnetypen.
5.  I **Kolonne B** velger du **FD** for kolonnetypen.
6.  Dobbeltklikk i **Dimensjonsfilter**-feltet.
7.  I **Dimensjon**-vinduet dobbeltklikker du **Avdeling**-kolonnen.
8.  I delen for enkeltvis eller område i dialogboksen klikker du **ellipsen** for **Fra**-feltet for å vise en liste over avdelinger.
9.  Velg avdeling **022**, **Salg og markedsføring**, og klikk deretter **OK**.
10. Gjenta trinn 5 til 8 for avdeling 23–25.
11. I raden **Topptekst 2** for hver FD-kolonne skriver du inn følgende avdelingsbeskrivelser:
    -   Kolonne B – Salg og markedsføring
    -   Kolonne C – Operasjoner
    -   Kolonne D – Finans
    -   Kolonne E – IT

12. Lagre kolonnedefinisjonen som Avdelinger side ved side. Siden vi bruker en eksisterende raddefinisjon, kan rapportdefinisjonen nå endres slik at den bruker den nylig opprettede kolonnedefinisjonen og den eksisterende raddefinisjonen.
13. På **Vindu**-menyen velger du **Ny rapportdefinisjon** for å åpne rapportdefinisjonen.
14. Velg **Resultatregnskap – standard** som raddefinisjonen og **Avdelinger side ved side** som kolonnedefinisjonen.
15. Lagre rapportdefinisjonen som **Resultatregnskap for avdeling side ved side**.
16. Endre basisåret til **2012**.
17. Endre detaljnivået til **Økonomisk, Konto og Transaksjon**.
18. **Lagre** endringene, og **generer**. Når rapporten er generert og åpnes, kan du utforske den.

## <a name="additional-resources"></a>Tilleggsressurser
[Finansrapportering](../../financials/general-ledger/financial-reporting-getting-started.md) 
[Vise finansrapporter](../../financials/general-ledger/view-financial-reports.md) 
[Blogg for Dynamics-finansrapportering](http://blogs.msdn.com/b/dynamics_financial_reporting/)




