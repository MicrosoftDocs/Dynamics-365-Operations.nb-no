---
title: Utsetting
description: Dette emnet hjelper deg med å bygge en gjennomgang av utsetting i produksjonen i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c4ef554406c727cc410f8dca5f41264be01060b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579358"
---
# <a name="subcontracting"></a>Utsetting

[!include [banner](../includes/banner.md)]

Dette emnet hjelper deg med å bygge en gjennomgang av utsetting i produksjonen i Microsoft Dynamics 365 Supply Chain Management. Den første delen av dette emnet beskriver oppsettet av dataene. Den andre delen leder deg gjennom trinnene i gjennomgangen.

## <a name="target-audience"></a>Målpublikum

I dette emnet lærer du hvordan du konfigurerer bruk av utsetting i produksjon. Du vil bruke eksisterende data i den juridiske enheten HQUS for å gjøre det grunnleggende oppsettet av en aktivitetsflyt for utsetting. Demodataene i den juridiske enheten HQUS inneholder oppsettsparametere som har blitt forhåndsdefinerte for å støtte trinnene i gjennomgangen. Selv om gjennomgangen håndterer viktige vanskelige punkt og utfordringer for forskjellige roller, kan den fullføres av systemadministratoren.

## <a name="demo-scenario"></a>Demoscenario

I den juridiske enheten HQUS produseres avanserte høyttalere. I løpet av produksjonsprosessen går høyttalerne gjennom følgende tre operasjoner.

- **Før montering** – Høytalerkabinettet monteres. Materialet for kabinettet plukkes på materialelageret før operasjonen startes.
- **Lakkering** – Når høyttalerkabinettet er montert, må det lakkeres. Denne operasjonen utføres av en leverandør (underleverandør). Det pre-monterte høyttalerkabinettet sendes til lakkeringsunderleverandøren sammen med to materialer.
- **Fullføring** – Etter et høyttalerkabinettet er blitt lakkert av underleverandøren, kommer det tilbake til den juridiske enheten HQUS, slik at monteringen av høyttaleren kan fullføres.

Illustrasjonen nedenfor viser de tre operasjonene og materialene som de bruker.

![Før-montering, lakkering og fullføring, og materialene de bruker.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Installasjon

Før du starter gjennomgangen, må du definere dataene.

### <a name="set-up-the-finished-product"></a>Definer det ferdige produktet

Denne prosedyren tar deg gjennom installasjonen av frigitt produkt D8100, "Lakkert kabinett".

1. Velg **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** for å åpne siden **Detaljer om frigitt produkt**.
2. Skriv inn **D8100** i hurtigfilterfeltet for å finne det eksisterende frigitte produktet.

    ![Filtrering for frigitt produkt D8100 på siden Detaljer om frigitt produkt.](./media/subcontract02_filtering-released-products.png)

3. I handlingsruten i fanen **Utvikling** velger du **Rute** for å åpne **Rute**-siden.

    **Rute**-siden viser de åtte ruteversjonene for det frigitte produktet D8100. De åtte ruteversjonene er fordelt mellom fire ruter på område 1 og område 5. Rute 000400 brukes for etterkalkulering, rute 00041 brukes når lakkeringsoperasjonen er en intern operasjon, og rute 00042 som brukes når lakkeringsoperasjonen er en ekstern operasjon.

    ![Åtte ruteversjoner på Rute-siden.](./media/subcontract03_route-page.png)

4. I den øvre ruten, i **Versjoner**-rutenettet, velger du ruteversjon **00042** for område **5**.
5. I den nedre ruten, i fanen **Oversikt**, velger du operasjon **20** (**Cbnt CtSc**) i rutenettet.

    ![Operasjon 20 ruteversjon 00042 for område 5 valgt.](./media/subcontract04_route-version-operation.png)

6. Velg fanen **Generelt**.

    Legg merke til at feltet **Rutetype** er satt til **Leverandør**. Denne verdien angir at operasjon 20 (Cbnt CtSc) er en utsatt operasjon.

    ![Rutetype-feltet satt til Leverandør i fanen Generelt.](./media/subcontract05_general-tab.png)

7. Velg fanen **Ressursbehov**.

    Funksjonene blir brukt til å finne en aktuell ressurs under produksjonsplanlegging. For operasjon 20 (Cbnt CtSc), legg merke til at en ressurs som har to egenskaper, **Lakkering** og **Lakkerte kabinetter**, kreves.

    ![Egenskapene Lakkering og Lakkerte kabinetter i fanen Ressurskrav.](./media/subcontract06_resource-requirements-tab.png)

8. Velg **Gjeldende ressurser** for å åpne dialogboksen **Gjeldende ressurser** .

    Det finnes tre ressurser som samsvarer med ressurskravene for operasjonen. Legg merke til at 8851 og 8852 er av **Leverandør**-typen.

    ![Tre aktuelle ressurser i dialogboksen Gjeldende ressurser.](./media/subcontract07_applicable-resources-dialog.png)

9. Velg **OK** for å lukke dialogboksen **Gjeldende ressurser** og gå tilbake til **Rute**-siden.
10. Lukk **Rute**-siden for å returnere til siden **Detaljer om frigitt produkt**.

    ![Siden Detaljer om frigitt produkt.](./media/subcontract08_released-product-details-page.png)

11. I handlingsruten i fanen **Utvikling** velger du **Stykklisteversjoner** for å åpne **Stykklisteversjoner**-siden.

    **Stykklisteversjoner**-siden viser fire stykklisteversjoner for det frigitte produktet D8100. 000040 brukes for etterkalkulering og planlegging, stykkliste 000041 brukes hvis lakkeringsoperasjonen gjøres internt, og stykkliste 000042 og 000043 brukes hvis lakkeringsoperasjonen er satt ut.

    Legg merke til at vare S8050 er et produkt av **Service**-varetypen. Denne varen representerer arbeidet som er satt ut.

    ![Fire stykklisteversjoner på siden Stykklisteversjoner.](./media/subcontract09_bom-versions-page.png)

12. På hurtigfanen **Stykklistelinjer**, velg **Rediger** for å åpne dialogboksen **Rediger stykklistelinje**.

    Når en produksjonsordre er opprettet og estimert for frigitt produkt D8100, blir en bestilling generert automatisk for vare S8050. Denne bestillingen knyttes til produksjonsordren. For at bestillinger skal genereres automatisk, må **Linjetype**-feltet være satt til **Leverandør**, og leverandørkontoen for underleverandøren må være valgt. I dette tilfellet er leverandørkontoen US-801.

    Legg merke til at stykklistelinjen er koblet til lakkeringsoperasjonen gjennom operasjonsnummeret (i dette tilfellet 20).

    ![Dialogboksen Rediger stykklistelinje.](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Opprett et passord for lagerarbeidere

Du må definere et passord for lagerarbeiderne som bruker den håndholdte enheten.

1. Velg **Lagerstyring \> Oppsett \> Arbeider** for å åpne siden **Arbeidsbrukere**.
2. På hurtigfanen **Brukere** merker du raden for bruker **51**.

    ![Siden Arbeidsbrukere.](./media/subcontract11_work-users-page.png)

3. Velg **Tilbakestill passord**.
4. I feltene **Passord** og **Bekreft passord**, angi **1**.
5. Velg **Angi passord**.

## <a name="step-by-step-walkthrough"></a>Trinnvis gjennomgang

**Scenario og bakgrunn**

En produksjonsordre på 10 deler opprettes for produkt D8100, "Lakkert kabinett". Lakkeringen av kabinetter er en operasjon som er satt ut, som utføres hos leverandør US-801, Perfect Coating Solutions. Produksjonsordren består av tre operasjoner. I den første operasjonen forhåndsmonteres kabinettet i en intern operasjon. Materialet for forhåndsmonteringen frigis for plukking i råvarelageret. Når forhåndsmonteringen er fullført, sendes kabinettet til Perfect Coating Solutions sammen med to materialer som kreves for lakkeringsoperasjonen. Når det lakkerte kabinettet er mottatt fra leverandøren, går det gjennom en siste intern monteringsoperasjon før det blir rapportert som fullført.

1. Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.
2. I handlingsruten velger du **Ny produksjonsordre** for å åpne dialogboksen **Opprett produksjonsordre**.

    ![Dialogboksen Opprett produksjonsordre.](./media/subcontract12_create-production-order-dialog.png)

3. Velg **D8100** i feltet **Varenummer**.
4. Feltene for lagerdimensjoner vises når du velger varenummeret. I **Farge**-feltet velger du **Krom**.

    Det vises en meldingsboks der du blir spurt om de aktive versjonene for stykklisten og ruten skal settes inn.

    ![Meldingsboks.](./media/subcontract13_message-box.png)

5. Velg **Ja**. 

    I dialogboksen **Opprett produksjonsordre** er de aktive versjonene av stykklisten og ruten for produkt D8100 valgt automatisk i feltene **Stykklistenummer** og **Rutenummer**. I dette tilfellet er stykkliste **000040** og rute **000040** valgt.
    
    > [!NOTE]
    > Både for stykklisten og ruten brukes versjon 000040 til etterkalkulering og planlegging.

6. I **Område**-feltet velger du **5**.
7. I **Lager**-feltet velger du **51**.
8. I feltene **Stykklistenummer** og **Rutenummer** endrer du verdien som ble valgt automatisk, til **000042**.

    > [!NOTE]
    > Både for stykklisten og ruten brukes versjon 000042 til å sette ut lakkeringen av kabinettet til leverandør US-801.

    ![Verdier angitt i dialogboksen Opprett produksjonsordre.](./media/subcontract14_create-production-order-dialog-set.png)

9. Velg **Opprett** for å opprette produksjonsordren og gå tilbake til siden **Alle produksjonsordrer**.

    ![Ny produksjonsordre på siden Alle produksjonsordrer.](./media/subcontract15_new-production-order.png)

10. i handlingsruten, i fanen **Produksjonsordre** velger du **Estimat** for å åpne dialogboksen **Estimat**.

    ![Dialogboksen Estimat.](./media/subcontract16_estimate-dialog.png)

11. Velg **OK** for å bekrefte estimatet og gå tilbake til siden **Alle produksjonsordrer**.

    > [!NOTE]
    > Når produksjonsordren er estimert, genereres bestillingen for servicevare S8050 for leverandør US-801.

12. I handlingsruten, i fanen **Produksjonsordre** velger du **Stykkliste** for å åpne **Stykkliste**-siden, der du kan vise stykklistelinjene for produksjonsordren.

    Legg merke til at det er en referanse til bestillingen som ble generert da produksjonsordren ble estimert for servicevare S8050.

    ![Stykklistelinjer i produksjonsordre på Stykkliste-siden.](./media/subcontract17_production-order-bom-lines.png)

13. Lukk **Stykkliste**-siden for å returnere til siden **Alle produksjonsordrer**.
14. i handlingsruten, i fanen **Planlegg** velger du **Planlegg jobber** for å åpne dialogboksen **Finplanlegging**.
15. Angi følgende verdier:

    - Velg **Fremover fra i morgen** i **Planleggingsretning**-feltet.
    - Sett **Begrenset kapasitet** til **Ja**.

    ![Dialogboksen Finplanlegging.](./media/subcontract18_job-scheduling-dialog.png)

16. Velg **OK** for å lukke dialogboksen **Finplanlegging** og gå tilbake til siden **Alle produksjonsordrer**.
17. I handlingsruten, i fanen **Planlegg** velger du **Gantt** for å åpne siden **Gantt-diagram - Ressursvisning**.

    Gantt-diagrammet gir en visuell oversikt over hvordan produksjonsjobbene er planlagt på ressursene. Legg merke til at den eksterne lakkeringen består av tre jobber: en prosessjobb, en transportjobb og en køtidjobb.

    ![Gantt-diagram på siden Gantt-diagram - Ressursvisning.](./media/subcontract19_gantt-chart.png)

18. Lukk siden **Gantt-diagram - Ressursvisning** for å returnere til siden **Alle produksjonsordrer**.
19. I handlingsruten, i fanen **Produksjonsordre** velger du **Frigi** for å åpne dialogboksen **Frigi**.

    ![Dialogboksen Frigi.](./media/subcontract20_release-dialog.png)

20. Velg **OK** for å lukke dialogboksen **Frigi**.
21. Velg **Produksjonskontroll \> Periodiske oppgaver \> Frigi til lager \> Automatisk frigivelse av stykkliste og formellinjer** for å åpne dialogboksen **Automatisk frigivelse av stykkliste og formellinjer**.

    ![Dialogboksen Automatisk frigivelse av stykkliste og formellinjer.](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Velg **OK** for å kjøre jobben Automatisk frigivelse av stykkliste og formellinjer.

    Denne jobben frigi plukkarbeid for råvarer til lageret.

23. Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.
24. Bruk hurtigfilterfeltet til å velge produksjonsordren du har arbeidet med.
25. I handlingsruten i fanen **Lager** velger du **Arbeidsdetaljer** for å åpne **Arbeid**-siden.

    Legg merke til at siden viser to sett med arbeid for råvareplukking. Det første arbeidet er for materialene M8100 og M8101. Disse materialene forbrukes av operasjonen 10. Det andre arbeidet er for materialene M8202 og M8250. Disse materialene forbrukes av operasjon 20, som er operasjonen som er satt ut.

    ![To sett med arbeid for råvareplukking på Arbeid-siden.](./media/subcontract22_work-page.png)

26. Start mobilappen Lagerstyring for å prosessere lagerarbeidet for operasjon 10.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Velg **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer** for å åpne siden **Alle produksjonsordrer**.
28. Bruk hurtigfilterfeltet til å velge produksjonsordren du har arbeidet med.
29. I handlingsruten, i fanen **Produksjonsordre** velger du **Start** for å åpne dialogboksen **Start**.
30. I fanen **Generelt** angir du følgende verdier:

    - I feltet **Fra oper.nr.** velg **10**.
    - I feltet **Til oper.nr.** velg **10**.

    ![Verdier angitt i fanen Generelt 1.](./media/subcontract23_start-dialog.png)

31. Velg **OK** for å lukke dialogboksen **Start** og gå tilbake til siden **Alle produksjonsordrer**.

    Legg merke til at statusen for produksjonsordren nå er **Startet**. Materialene for operasjon 10 forbrukes av en automatisk postering av plukklistejournalen. Tidsforbruket for operasjon 10 er gjort rede for av en automatisk bokføring av en rutekortjournal.

32. Start mobilappen Lagerstyring for å prosessere lagerarbeidet for operasjon 20.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. I handlingsruten, i fanen **Produksjonsordre** velger du **Start** for å åpne dialogboksen **Start**.
34. I fanen **Generelt** angir du følgende verdier:

    - I feltet **Fra oper.nr.** velg **20**.
    - I feltet **Til oper.nr.** velg **20**.
    - I feltet **Antall** angi **10**.
    - Sett alternativet **Poster plukkliste nå** til **Nei**.

    ![Verdier angitt i fanen Generelt 2.](./media/subcontract24_general-tab.png)

35. Velg **OK** for å lukke dialogboksen **Start** og gå tilbake til siden **Alle produksjonsordrer**.

    Det opprettes en plukkliste for materialene som skal brukes for lakkeringsoperasjonen, og for servicevaren. Servicevaren representerer kostnaden av operasjonen som er satt ut.

36. I handlingsruten, i fanen **Vis** velger du **Plukkliste** for å åpne siden **Plukkliste**.
37. Velg plukklisten som ikke er postert, og velg deretter journalnummeret for å vise journallinjene.

    ![Journallinjer på siden Plukkliste.](./media/subcontract25_picking-list.png)

38. I handlingsruten, velger du **Skriv ut** \> **Plukklisterapport** for å åpne dialogboksen **Plukklisterapport**.
39. Angi alternativet **Bruk følgeseddeloppsett** til **Ja**.

    ![Dialogboksen Plukklisterapport.](./media/subcontract26_picking-list-report-dialog.png)

40. Velg **OK** for å generere en **Plukkliste**-rapport.

    I dette tilfellet skrives en leverandørfølgeseddel ut fra produksjonsplukklistejournalen. Følgeseddelen angir materialene som sendes til leverandøren som skal utføre lakkeringsoperasjonen.

    ![Plukklisterapport.](./media/subcontract27_picking-list-report.png)

41. Lukk **Plukkliste**-rapporten for å gå tilbake til **Plukkliste**-siden.
42. I handlingsruten, velger du **Poster** for å åpne dialogboksen **Poster journal**.

    ![Dialogboksen Poster journal.](./media/subcontract28_post-journal-dialog.png)

43. Velg **OK** for å lukke dialogboksen **Poster journal**.
44. Åpne bestillingen.

    ![Bestilling-siden.](./media/subcontract29_purchase-order-page.png)

45. I handlingsruten, i fanen **Kjøp** velger du **Bekreft**.
46. Velg **Poster** for å åpne dialogboksen **Poster journal**.
47. Velg **OK** for å lukke dialogboksen **Poster journal** og gå tilbake til siden **Bestilling**.
48. Endre enhetsprisen fra **33** til **40**.

    ![Enhetspris endret på siden Bestilling.](./media/subcontract30_unit-price.png)

49. Bekreft bestillingen på nytt.
50. Mottaksseddel.

    ![Dialogboksen Poster mottaksseddel.](./media/subcontract31_posting-product-receipt-dialog.png)

51. Kjøpsfaktura.
52. Oppdater samsvarsstatusen.

    ![Siden Leverandørfaktura.](./media/subcontract32_vendor-invoice-page.png)

53. Ferdigmeld.

    ![Dialogboksen Ferdigmeld.](./media/subcontract33_report-as-finished-dialog.png)

54. Slutt.

    ![Dialogboks Slutt.](./media/subcontract34_end-dialog.png)

55. Kostnadssammenligning.

    ![Kostnadssammenligningsdiagrammer.](./media/subcontract35_cost-comparison-charts.png)

Manglende oppsett i data.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]