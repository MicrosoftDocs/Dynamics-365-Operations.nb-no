---
title: Føre utsatt inntekt
description: Dette emnet inneholder informasjon om hvordan du fører inntekt ved hjelp av funksjonen Inntektsføring.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 244321e1eb246c46260326a8892924d9d9da75d3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176041"
---
# <a name="recognize-deferred-revenue"></a>Føre utsatt inntekt

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling ennå. For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.

Dette emnet beskriver prosessen med å føre inntekt i inntektsføringsplanen. Etter at en faktura er postert for en salgsordre, blir det opprettet en inntektsføringsplan for hver salgsordrelinje som har en inntektsplan. Inntektsplanen på en linje brukes til å bestemme om linjens inntekt skal utsettes.

## <a name="view-revenue-recognition-schedule-details"></a>Vis detaljer om inntektsføringsplan

Det finnes to måter å få tilgang til detaljene i inntektsføringsplanen på.

- Du kan åpne inntektsføringsplanen direkte fra en fakturert salgsordre. I dette tilfellet filtreres informasjonen i inntektsplanen for å vise detaljene bare for den valgte salgsordren. Denne fremgangsmåten er nyttig når du skal validere tidsplandetaljene for en salgsordre.
- Du kan åpne tidsplanen for inntektsføring fra siden **Inntektsføring \>Periodiske oppgaver**. Denne fremgangsmåten brukes ofte når inntekt føres på slutten av en periode. Når siden åpnes for første gang, vises ingen informasjon. Bruk filtrene over rutenettet til å definere kriterier for tidsplandetaljene som skal vises. Du kan filtrere etter fakturadatoene ved å angi et datointervall, en salgsordre, en kunde, en prosjekt-ID eller en status.

[![Side for inntektsplaner](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

Hurtigfanen **Finansdimensjon** under rutenettet viser finansdimensjonene til salgsordrelinjen. Disse dimensjonene ble vurdert under postering til utsatt inntekt. De tas også hensyn til når inntekten føres. Dimensjonsverdiene som brukes, er avhengig av kontostrukturen som er tilordnet til inntekten og de utsatt inntektshovedkontoene.

## <a name="recognize-revenue"></a>Føre inntekt

Du fører inntekt ved å kjøre prosessen **Opprett journal** fra siden **Føre inntekt**. Du kan åpne denne siden fra salgsordren eller **Periodiske oppgaver**. Hvis prosessen kjøres fra salgsordren, fører den bare inntekt for den valgte salgsordren. Vanligvis kjøres prosessen i stedet fra **Periodiske oppgaver**, slik at den fører inntekt for alle posterte salgsordrefakturaer.

Hvis du vil definere kriteriene for valg og postering av inntekt, velger du **Opprett journal** for å åpne dialogboksen **Opprett journal**.

[![Opprette alternativer for journalparametere](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

I dialogboksen bruker du alternativene i feltgruppen **Behandlingsdato** til å definere posteringsdatoen som brukes når inntekten føres. Hvis du velger **Valgt dato**, kan du angi en posteringsdato i feltet **Transaksjonsdato**. Hvis du velger **Inntektsplandato**, brukes ikke transaksjonsdatoen. I stedet brukes verdien i feltet **Føringsdato** på hver linje i planen som posteringsdatoen.

Deretter angir du datoen for inntektsføring i feltet **Per dato**. Alle linjer i planen der føringsdatoen er på eller før datoen for som kommer, forutsatt at de ikke er på vent.

Når du er ferdig med å definere datoene, velger du **OK** i dialogboksen for å opprette journalen. Du mottar en informasjonsmelding som viser hvor mange transaksjoner som er opprettet, og hvilken journal de ble opprettet i. Journalen posteres ikke automatisk. Derfor har den ansvarlige for inntektsføringen tid til å validere hvilke linjer i planen som føres.

Når prosessen er kjørt, merkes linjene i planen som ble overført til journalen, som **Behandlet**. Flagget **Behandlet** angir at linjene er overført til journalen, men de kan være posterte eller uposterte. Når journalen for inntektsføringen er postert, blir flagget **Behandlet** værende. Hvis journalen for inntektsføring er slettet, eller hvis en linje slettes, fjernes flagget **Behandlet**. På den måten kan linjen føres når prosessen **Opprett journal** kjøres på nytt.

[![Side for inntektsføringsplaner](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Åpne **Linjer** på siden **Journal for inntektsføring** (**Inntektsføring \> Journaloppføringer \> Journal for inntektsføring**) for å vise detaljene for hva som blir ført. En egen transaksjon opprettes alltid for hver linje i planen som blir ført, selv om alle linjene posteres på samme dato ved hjelp av de samme finanskontoene.

[![Siden Journalbilag](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

Kolonnen **Konto** viser den utsatte finanskontoen for inntekt. Denne finanskontoen kan ikke redigeres. Denne begrensningen bidrar til å garantere at den riktige utsatte inntektsfinanskontoen frigis. Denne finanskontoen valideres ikke mot kontostrukturen, fordi den kan ha blitt endret siden postering til den refererte inntektsfinanskontoen sist oppstod.

Kolonnen **Motkonto** viser den finanskontoen for inntekt. Som standard hentes inntektsfinanskontoen fra lager posteringsprofiler, og finansdimensjonene hentes fra salgsordrelinjen. Denne finanskontoen valideres mot den gjeldende kontostrukturen. Den kan imidlertid redigeres hvis kontostrukturen er endret og krever flere finansdimensjoner.

Standardbeløpet er fra den tilsvarende linjen for tidsplanen, og det kan ikke endres.

Hvis salgsordren er en salgsordre med samtidig valuta, blir valutakursen som standard satt til valutakursen fra fakturaen. Denne virkemåten bidrar til å sikre at regnskapsvaluta- og rapporteringsvalutabeløpene er helt frigitt. På grunn avrunding kan det hende at valutakursen for den siste linjen i tidsplanen avviker litt fra kursen på fakturaen.

Når journalen for inntektsføring er postert, angis bilaget i tidsplanen. Hvis det er mer enn ett bilag for samme linje i tidsplanen, vises det en stjerne (\*) på linjen. Hvis du vil vise bilagene som ble postert for denne linjen, velger du **Bilagstransaksjoner**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Endre detaljene om tidsplan for inntektsføring

De fleste dataene i inntektsplandetaljene kan ikke redigeres. Du kan ikke legge til nye linjer i planen, og eksisterende linjer kan ikke slettes. Inntektsplandetaljene for hver salgsordrelinje må vedlikeholdes for å hjelpe til med å garantere at en organisasjon fører samme beløp som ble utsatt, over tid.

### <a name="edit-schedule-lines"></a>Redigere tidsplanlinjer

Noen redigeringer er tillatt på linjene i tidsplanen. Følgende felt kan endres på linjene:

- **På vent** – dette flagget kan angis eller fjernes før linjen behandles. Hvis du vil fjerne flagget, merker du raden og velger **Fjern sperre**. Inntekt kan ikke føres på linjer som er på vent. Linjer kan settes på vent hvis inntektsplanen er satt opp for automatiske sperringer.

    [![Inntektsplaner – redigere tidsplanlinjer](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Føringsdato** – føringsdatoen kan endres før linjen behandles. Når prosessen som oppretter journalen for å føre inntekten, kjøres, angis det en dato i feltet **Før inntekt per dato**. Datoen sammenlignes med datoen i feltet **Føringsdato** for å bestemme hvilke linjer som skal føres.
- **Beløp som skal frigis** – beløpet som blir frigitt, kan endres før linjen behandles. Du kan redusere inntektsbeløpet som føres, men du kan ikke øke det. Dette feltet gjør det mulig for en organisasjon å føre deler av inntekten på føringsdatoen. Hvis beløpet endres, viser beløpet i feltet **Restbeløp** hvor mye inntekt som fortsatt må føres.
- **Antall som skal frigis** – hvis inntektsplanen er satt opp for én forekomst eller én måned, viser feltet **Antall som skal frigis** antallet for salgsordrelinjen. Dette feltet kan også redigeres og er en annen måte å føre deler av inntekten på. Hvis antallet på linjen for eksempel er 5, kan du overstyre antallet slik at det er mindre enn 5. Beløpet i feltet **Beløp som skal frigis** oppdateres proporsjonalt.

### <a name="update-contract-terms"></a>Oppdatere kontraktsbetingelser

Detaljene for inntektsplanen blir opprettet basert på inntektsplanen som er tilordnet salgsordrelinjen når fakturaen posteres. Hvis inntektsplanen på salgsordrelinjen er feil, kan den ikke endres på salgsordren etter at salgsordren er fakturert. I stedet må du bruke knappen **Oppdater kontraktsbetingelser** til å endre inntektsplanen. Inntektsplanen kan endres enten før eller etter at inntekten er ført.

Hvis du vil endre tidsplanen, velger du en hvilken som helst tidsplanlinje for varen du vil endre. I illustrasjonen nedenfor er linjen for vare S0008, som ble postert ved hjelp av en inntektsplan på 12 måneder, valgt. Når du velger **Oppdater kontraktsbetingelser**, viser en dialogboks kontraktens start- og sluttdatoer og inntektsplanen.

[![Start- og sluttdatoer for kontrakt](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Endre start- og sluttdatoene for kontrakten slik at de gjenspeiler riktig datointervall. Når du endrer datointervallet, må verdien i feltet **Antall forekomster** samsvare med en inntektsplan som er definert i systemet. I dette eksemplet må det defineres en tidsplan for en 24-måneders inntekt, fordi kontrakten er endret til en 24-måneders kontrakt. Ettersom det finnes en inntektsplan på 24 måneder, angis den som standard, og kontrakten kan endres. Hvis en inntektsplan som har et tilsvarende antall forekomster, ikke finnes, kan ikke kontrakten endres. Når du er ferdig med å oppdatere kontraktsvilkårene og inntektsplanen etter behov, velger du **OK** i dialogboksen for å lagre endringene.

[![Oppdatert datointervall for kontrakt](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

Kontraktsendringene har følgende innvirkning på detaljene for inntektsplanen:

- Hvis det ikke er noen inntekt for produktet, fjernes alle de forrige planleggingsdetaljene og de erstattes med de nye tidsplandetaljene for inntekt. Vare S0008 hadde for eksempel opprinnelig 12 linjer i tidsplandetaljene. Disse 12 linjene fjernes og erstattes med 24 linjer, basert på den nye inntektsplanen.
- Hvis det er ført inntekt for produktet, ble deler av inntekten feilaktig ført fordi føringen var basert på feil inntektsplan. Disse linjene må tilbakeføres og føres på nytt basert på den nye planen. I dette scenariet opprettes det nye inntektsplanlinjer som har negative beløp på den opprinnelige føringsdatoen. Nye linjer opprettes deretter for å føre beløpene basert på den nye inntektsplanen. 8. august 2019 førte du for eksempel en inntekt på USD 10,53. Den 8. september 2019 førte du en inntekt på USD 13,16. Derfor opprettes det to nye linjer på samme dato. En linje gjelder for USD 10,53, og den andre linjen gjelder for USD 13,16. Tjuefire nye linjer opprettes, og den totale utsatte inntekten på USD 160,61 tildeles på tvers av dem. Du kan postere tilbakeføringslinjene ved å kjøre prosessen **Opprett journal**.

[![Inntektsføringsplan](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)
