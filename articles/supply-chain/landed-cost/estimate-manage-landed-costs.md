---
title: Estimere og behandle netto innkjøpspris
description: Systemet bruker det automatiske kostnadsoppsettet til å fastslå et estimat for netto innkjøpspris. Dette emnet beskriver hvordan du kan definere ulike scenarioer for å gi et mer nøyaktig estimat.
author: sherry-zheng
ms.date: 01/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostTemplateTable, ITM CostEstimateDialog, ITMCostEstimateTable, SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-26
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 510f5fc4910dde2f91fe2d666abb23a9bd7381f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823439"
---
# <a name="estimate-and-manage-landed-costs"></a>Estimere og behandle netto innkjøpspris

[!include [banner](../../includes/banner.md)]

Systemet bruker det [automatiske kostnadsoppsettet](auto-cost-setup.md) til å fastslå et estimat for netto innkjøpspris. I tillegg kan du definere ulike scenarioer for å gi et mer nøyaktig estimat. Disse scenarioene blir lagret. Du kan derfor gå gjennom dem senere og sammenligne dem med faktiske data i en rapport. Du kan også oppdatere vareprisen.

## <a name="set-up-cost-estimates"></a>Konfigurere kostnadsestimater

### <a name="set-up-cost-templates"></a>Definer kostnadsmaler

Kostnadsmaler oppretter standardinnstillinger som brukere som får estimatet, ikke nødvendigvis vet. Maler kan bidra til å redusere kompleksiteten i estimeringsprosessen ved å minimere valgene brukerne må angi for å få et nøyaktig estimat. Hvis du bruker standard kostnadsmodellen, kan du bruke kostnadsmaler mens du definerer varekostnaden.

Hvis du vil konfigurere kostnadsmalene dine, kan du gå til **Netto innkjøpspris \> Kostnadsoppsett \> Kostnadsmaler**. På siden **Kostnadsmaler** viser listen til venstre alle gjeldende kostnadsmaler. Du kan bruke knappene i handlingsruten til å opprette, slette og redigere maler.

Følgende tabell beskriver feltene som er tilgjengelige for hver mal.

| Felt | beskrivelse |
|---|---|
| Kostnadsmal | Angi et unikt navn for kostnadsmalen. Navnet beskriver vanligvis faktoren eller kostnadsmultiplikatoren for malen. |
| beskrivelse | Angi en beskrivelse av kostnadsmalen. |
| Forsendelsesfirma | Velg forsendelsesfirmaet som skal brukes når malen brukes. |
| Leveringsmiddel | Velg leveringsmåten, for eksempel sjø- eller lufttransport, som skal brukes når malen brukes. Dette feltet bidrar til å bestemme de automatiske kostnadene som er knyttet til varene i et kostnadsestimat. |
| Fraktcontainertype | Velg typen forsendelsescontainer som skal brukes når malen brukes. Dette feltet bidrar til å bestemme de automatiske kostnadene som er knyttet til varene i et kostnadsestimat. |
| Tollmegler | Tollmekleren (leverandøren) som skal brukes når malen brukes. Dette feltet bidrar til å bestemme de automatiske kostnadene som er knyttet til kostnadsestimatet. |
| Omregningsfaktor | Angi multiplikatoren (i prosent) som automatisk skal brukes på kostnadsestimatet når malen brukes. Hvis du for eksempel vil legge til 10 prosent i det beregnede kostnadsestimatet, skriver du inn *1,10*. |

### <a name="create-a-cost-estimate"></a>Opprette et kostnadsestimat

Bruk dialogboksen **Kostnadsestimat** til å generere et nytt kostnadsestimat som er basert på en valgt kostnadsmal, et valgt sett med varer og andre detaljer om et utvalg av varer. Disse innstillingene brukes deretter til å fastslå den estimerte netto innkjøpsprisen for varer. Disse kostnadsestimatene brukes primært til å arbeide med varer med standard kostpris. Ved å legge til den anslåtte netto innkjøpsprisen i standard kostpris for varer på lager, bør du oppleve mindre avvikstransaksjoner når varene legges til i en sjøreise, fordi standardkostnaden vil gjenspeile estimatene for den netto innkjøpsprisen.

Hvis du vil åpne dialogboksen **Kostnadsestimat**, går du til **Netto innkjøpspris \> Periodiske oppgaver \> Kostnadsestimat**. Deretter angir du verdier for feltene som er beskrevet i følgende underdeler. Til slutt velger du **OK** for å opprette estimatet. Siden **Kostnadsestimat** (**Netto innkjøpspris \> Forespørsler \> Kostnadsestimater**) vises deretter med det nye estimatet, som beskrives senere i dette emnet.

### <a name="settings-on-the-parameters-tab"></a>Innstillinger i fanen Parametere

Følgende tabell beskriver feltene som er tilgjengelige i fanen **Parametere** i dialogboksen **Kostnadsestimat**.


| Felt | beskrivelse |
|---|---|
| Kostnadsmal | Velg en kostnadsmal. Innstillingene som er knyttet til den valgte malen, vil bli brukt til å bestemme hvilke automatiske kostnader som skal brukes. |
| Estimert dato | Som standard er dette feltet satt til dagens dato, men du kan endre verdien. Den angitte datoen vil bli brukt til å velge riktige salgspriser, innkjøpspriser, automatiske kostnader og valutakursen hvis det brukes en forsendelsessats. |
| Mål | Kostnadene kan avhenge av et mål. Når det for eksempel brukes flyfrakt, kan det hende prissetting av volum brukes. Hvis kostnaden avhenger av et mål, angir du verdien for målet. Ellers anbefales det at du setter dette feltet til *1*, med mindre du er sikker på at det ikke forekommer noen tildeling ved bruk av mål. Angi en desimalverdi. Enheten er den som er definert i den aktuelle automatiske kostnadsposten. |
| Reisemal | Velg en [reisemal](multi-leg-journey-setup.md). Dette feltet brukes til å fastsette riktige automatiske kostpriser som skal brukes. |
| Fra-havn | Havnen som varene skal sendes fra. Dette feltet er definert på grunnlag av den valgte malen for videre opprettede tjenester. |
| Til-havn | Havnen som varene skal sendes til. Dette feltet er definert på grunnlag av den valgte malen for videre opprettede tjenester. |
| Valuta. | Velg valutaen som varene skal kjøpes i. |
| Containere | Hvis flere containere vanligvis brukes, angir du antall containere. Systemet vil deretter bruke kostnader for flere containere når kostnadene beregnes. |
| Folioer | Hvis det vanligvis brukes flere folioer, angir du antallet. (Antallet er vanligvis *1*.) |
| Site | Angi stedet der varene skal leveres. |

### <a name="settings-on-the-items-tab"></a>Innstillinger i fanen Varer

I fanen **Varer** kan du legge til så mange varer i estimatet som du trenger. Bruk verktøylinjen til å legge til elementer i rutenettet eller fjerne elementer. Velg **Lager \> Visningsdimensjoner** på verktøylinjen for å åpne en dialogboks der du kan legge til dimensjonskolonner i rutenettet eller fjerne kolonner.

Følgende tabell beskriver feltene som er tilgjengelige for hver vare.

| Felt | beskrivelse |
|---|---|
| Varenummer | Velg varen du vil bestemme prisen for. (Hvis varen ennå ikke finnes i systemet, oppretter du en testvare, knytter den eventuelt til en varekostgruppe for sjøreise, og lar deretter prisen stå tom eller opprett eller endre prisen.) |
| Leverandørnummer | Velg leverandøren som skal brukes til estimatet for denne varen. Hvis en standardleverandør er tilordnet varen, angis dette feltet automatisk. |
| Antall | Velg antallet du vil kjøpe inn. |
| Kostpris | Systemet bruker prissettingsreglene til å finne en opprinnelig pris, men du kan overstyre denne prisen hvis det er nødvendig. |
| Salgspris | Angi forventet salgspris for varene. |
| Mål | Angi en desimalverdi for målet av varene. Enheten er den som er definert for det gjeldende frigitte produktet. |
| Oppdater varens vekt/volum | Merk av i denne avmerkingsboksen for å oppdatere vekten eller volummålet for det frigitte produktet, slik at det stemmer overens med verdien for **Mål** som er angitt for denne raden. |
| (Andre dimensjoner) | Det kan hende at du ser flere kolonner med informasjon om hver vare, avhengig av dimensjonene du har valgt å vise. |

Hvis du vil vise eller justere volum- og/eller vektdetaljene for en vare, velger du varen i rutenettet og bruker deretter feltene nederst på siden.

## <a name="manage-estimated-costs"></a>Administrere estimerte kostnader

Hvis du vil vise og redigere kostnadsestimatene du har opprettet, går du til **Netto innkjøpspris \> Forespørsler \> Kostnadsestimater**. På siden **Kostnadsestimater** viser listen til venstre alle gjeldende kostnadsestimater. Du kan bruke knappene i handlingsruten til å arbeide med et valgt estimat. Vær oppmerksom på at du ikke kan opprette et nytt kostnadsestimat fra siden **Kostnadsestimater**. I stedet bruker du dialogboksen **Kostnadsestimat** (**Netto innkjøpspris \> Periodiske oppgaver \> Kostnadsestimat**), som beskrevet tidligere i dette emnet.

Siden **Kostnadsestimater** viser hvordan hver estimerte kostnad ble avledet. Den viser også den estimerte, innlagte kostnaden for hver vare. Du kan endre et kostnadsestimat ved å endre kostprisen og/eller valutaen som er knyttet til de forskjellige varene. Du kan også endre de tilknyttede sjøreisekostnadene både på sjøreise- og containernivå. Når du bruker denne siden til å endre kostnadene, blir du bedt om å beregne de estimerte kostnadene for varene i kostnadsestimatet på nytt. Når du er klar, kan du bruke estimatene til å oppdatere kostprisen for varene i kostnadsmalen.

### <a name="information-on-the-header"></a>Informasjon i hodet

Toppen av siden **Kostnadsestimater** viser innstillingene som ble brukt til å generere det valgte kostnadsestimatet, som beskrevet i den forrige delen. 

### <a name="settings-and-buttons-on-the-lines-fasttab"></a>Innstillinger og knapper i hurtigfanen Linjer

Hurtigfanen **Linjer** viser hver vare som er inkludert i det gjeldende estimatet. Følgende tabell beskriver feltet som er tilgjengelige for hver rad.

| Felt | beskrivelse |
|---|---|
| Leverandørnummer | Leverandørkontoen som er knyttet til varen. |
| Varenummer | Varenummeret. |
| Antall | Antall varer som brukes til å bestemme kostnaden. |
| Kostpris | Kostprisen i henhold til forretningsavtalen. Denne verdien vises i den lokale valutaen. |
| Mål | Det individuelle målet. Enheten er den som er definert for det gjeldende frigitte produktet. |
| Estimert godskostnad | Den estimerte netto innkjøpsprisen for det totale antallet. |
| Per enhet | Den estimerte netto innkjøpsprisen delt på antallet. |
| (Andre dimensjoner) | Det kan hende at du ser flere kolonner med informasjon om hver vare, avhengig av dimensjonene du har valgt å vise. |

Følgende tabell beskriver knappene som er tilgjengelige på verktøylnijen i hurtigfanen **Linjer**.

| Knapp | beskrivelse |
|---|---|
| Legg til | Legg til varer i kostnadsestimatet. Når du har lagt til varer, må du velge **Omberegn** i handlingsruten. |
| Fjern | Fjern varer fra kostnadsestimatet. Når du har fjernet varer, må du velge **Omberegn** i handlingsruten. |
| Sjøreisekostnader | Åpne en side der du kan vise og redigere ulike typer sjøreisekostnader for varen. |
| Lager \> Visningsdimensjoner | Åpne en dialogboks der du kan legge til dimensjonskolonner i rutenettet eller fjerne kolonner. |

### <a name="settings-on-the-general-fasttab"></a>Innstillinger i hurtigfanen Generelt

Hurtigfanen **Generelt** viser detaljer om varen som for øyeblikket er valgt i hurtigfanen **Linjer**. Mye av denne informasjonen gjentas fra hurtigfanen **Linjer**, og den kan redigeres uansett. Tilleggsdetaljer er imidlertid også tilgjengelig her. Verdiene til ekstrafeltene er basert på oppsettet til det gjeldende frigitte produktet.

### <a name="settings-on-the-dimension-fasttab"></a>Innstillinger i hurtigfanen Dimensjon

Hurtigfanen **Dimensjon** viser verdier for alle tilgjengelige lagerdimensjoner for varen som er valgt i hurtigfanen **Linjer**, uansett hvilke dimensjoner du har valgt å vise der. Eventuelle verdier som vises her, kommer fra den aktuelle kostnadsestimatmalen. De er valgfrie i malen for kostnadsestimat.

### <a name="buttons-on-the-action-pane"></a>Knapper i handlingsruten

Du kan bruke knappene i handlingsruten på siden **Kostnadsestimater** til å arbeide med det valgte kostnadsestimatet. Følgende tabell beskriver knappene som er tilgjengelige.

| Handling | beskrivelse |
|---|---|
| Kostnadsforespørsel | Vis alle kostnadene for sjøreisen. Du kan vise kostnader på nivå med den enkelte varen etter behov. |
| Oppdater standardkostnad | <p>Oppdater standardkostnaden ved å bruke standard kostnadsversjon som er definert på siden **Parametere for netto innkjøpspris**. Du kan overstyre denne versjonen.</p><p>**Merk:** Hvis en vare har flere varedimensjoner (for eksempel ulike størrelser, farger og konfigurasjoner), men disse dimensjonene ikke er valgt for estimatet, vil systemet opprette en uavsluttet pris for hver kombinasjon.</p><p>**Viktig:** Prisoppdelingen opprettes og brukes til å fastslå avvik i standard kostpris per netto innkjøpspris.</p> |
| Sjøreisekostnader | Vis og rediger sjøreisekostnader for alle varer i forsendelsen. |
| Omberegn | Oppdater den estimerte netto innkjøpsprisen etter at sjøreisekostnadene er oppdatert, lagt til eller fjernet. |
| Lås | Lås kostnadsestimatposten slik at det ikke kan gjøres flere endringer. |

## <a name="item-cost-price-update"></a>Oppdatering av varekostnadspris

Den periodiske oppgaven **Oppdatering av varekostpris** oppdaterer alle kostnadsestimater som samsvarer med filtrene du angir når du kjører oppgaven. Effekten er lik virkningen av å velge **Oppdater standardkost** i handlingsruten for ett estimat. I dette tilfellet gjelder imidlertid oppdateringen for alle samsvarende estimater.

Gjør følgende for å kjøre den periodiske oppgaven.

1. Gå til **Netto innkjøpspris \> Periodiske oppgaver \> Oppdatering av varekostpris**.
1. I dialogboksen **Oppdater kostpris fra estimat** definerer du følgende felt som nødvendige for å begrense oppdateringsområdet:

    - **Versjon** – Oppdater bare estimater som bruker den angitte kostnadsversjonen.
    - **Sted** – Oppdater bare estimater som bruker det angitte stedet.
    - **Kostnadsmal** – Oppdater bare estimater som bruker den angitte malen.
    - **Til-havn** – Oppdater bare estimater som bruker den angitte til-havnen.
    - **Estimatdato** – Oppdater bare estimater som har den angitte datoen.

1. Angi alternativene i hurtigfanen **Poster som skal inkluderes** og **Kjør i bakgrunnen** som vanlig for periodiske oppgaver.
1. Velg **OK** for å kjøre oppgaven.

> [!NOTE]
> Denne periodiske oppgaven vil bare utføres såfremt følgende informasjon er tilgjengelig:
>
> - Hvert relevante produkt må ha definert **Bruttodybde**, **Bruttobredde** og **Bruttohøyde**.
> - Hver relevante leverandør må ha definert en **Fra-havn**.
