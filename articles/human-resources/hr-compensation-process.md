---
title: Behandle kompensasjon
description: Med kompensasjonsbehandling kan du beregne nye kompensasjonsbeløp for de ansatte basert på justeringer av egenkapitalen, mål for personlig tilleggsøkning og ytelse.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 228c891e8c29cf4309856b90139d0b88805a9812
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886167"
---
# <a name="process-compensation"></a>Behandle kompensasjon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Med kompensasjonsbehandling kan du beregne nye kompensasjonsbeløp for de ansatte basert på justeringer av egenkapitalen, mål for personlig tilleggsøkning og ytelse. Denne artikkelen dekker den grunnleggende flyten i faste kompensasjonsplaner uten faktorisering av ytelsen til en ansatt.

## <a name="plan-the-new-compensation-amounts-and-budgets"></a>Planlegg nye kompensasjonsbeløp og budsjetter
Hvis du vil gi ansatte en personlig tilleggsøkning, må du definere et budsjett med fast økning for hver av avdelingene: **Kompensasjonsstyring** > **Koblinger** > **Mål for personlig tilleggsøkning**. (Du kan også åpne denne siden gjennom avdelingen: **Organisasjon** > **Avdelinger**.) Du kan angi om ansatte i en bestemt fagforening eller plassering trenger en annen økningsprosent. Feltene **Budsjett** og **Valuta** inneholder informasjon og kan brukes til å registrere et valutabeløp for budsjettet.

## <a name="set-up-the-compensation-process"></a>Definer kompensasjonsprosessen
På siden **Kompensasjonsprosesser** kan du angi parameterne for kompensasjonsbehandlingen. Dette inkluderer datoperioden som skal evalueres for å fastslå kompensasjonsbeløpene, og datoen da de nye kompensasjonsbeløpene skal tre i kraft.

Du kan også inkludere en **Fast lønn for klassifisert ansettelsesdato** hvis noen av de faste kompensasjonsplanene bruker en ansettelsesregel med prosent. For disse planene får alle som ble ansatt etter **Syklusstart**-dato og før **Fast lønn for klassifisert ansettelsesdato** motta 100 % av beregnet personlig tillegg eller generelt tillegg. Alle som ble ansatt etter **Fast lønn for klassifisert ansettelsesdato** og før **Syklusens sluttdato**, mottar en del av den beregnede økningen basert på hvor mange dager blant totale syklusdager de var ansatt. Hvis for eksempel syklusen går fra 1. til 31. desember, og 1. april er dato for proporsjonalt fordelt fast lønn etter ansettelsesdato, får en ansatt som er ansatt i mars, hele den beregnede økningen, mens en arbeider som er ansatt den 1. juli, mottar omtrent halvparten av den beregnede økningen.

**Tidspunkt**-dato for prosesshendelsen brukes bare for behandling av bestemte variable kompensasjonsplaner og vil ikke bli dekket her. **Tidsfrist for gjennomgang** er tidsfristen for å gjøre alle anbefalingene slik at de nye kompensasjonsbeløpene kan lastes inn i den ansattes post. Datoen for gjennomgang er kun til informasjon.

Når du har lagret parameterne for prosesshendelsen, kan du klikke **Oppsett** for å velge planene som skal tas med når prosessen kjøres, og hvilke handlinger for fast kompensasjon som skal utføres for hver plan.

Klikk **Legg til**-knappen i **Planer**-kategorien for å legge til en kompensasjonsplan i prosesshendelsen. Kolonnene **Bruk annen utnyttelse**, **Utnyttelsesfaktor**, og **Utnyttelsesbeskrivelse** brukes bare i variable kompensasjonsplaner og dekkes ikke i denne artikkelen.

Lagre posten, og klikk deretter **Legg til**-knappen i kategorien **Handlinger** for å legge til handlinger for fast kompensasjon for den valgte planen. Bruk alternativet **Aktiver anbefaling** til å angi et annet beløp enn den beregnede retningslinjeøkningen for handlingen. Hvis du vil beregne en handling som er basert på resultatet fra den forrige handlingen for å koble flere kompensasjonshandlinger, merker du av for **Bruk forrige resultat**-alternativet. Handlinger for fast kompensasjon er typer kompensasjonslogikk som du kan gi beskrivende navn til. For planene **Klasse** og **Segment** kan du bare legge til handlinger for fast kompensasjon som er av følgende typer:

| Type handling for fast kompensasjon | Funksjonalitet                  |
|-------------------------------|-------------------------------------------------------------------------|
| Egenkapital                        | Egenkapitalhandlinger sammenligner den ansattes betalingssats per syklusens sluttdato med det laveste referansepunktet for nivået som er angitt på den ansattes jobb. Hvis den ansattes lønnssats er mindre enn det minste referansepunktet, beregnes tillegget som er nødvendig for å få den ansatte til det minste punktet i området.                                                                                |
| Personlig tillegg                         | Personlige handlinger vil beregne en økning som er basert på den ansattes lønnssats per syklusens sluttdato og økningsprosenten funnet i budsjettet med fast økning for den ansattes avdeling, fagforening og plassering.                                                                                                                                                                                         |
| Generelt                       | Generell handlinger vil beregne en økning som er basert på enten en prosent eller gi ansatte et flatt beløp. Dette bestemmes basert på innstillingene under **Fast kompensasjon** i kategorien **Generelt**.                                                                                                                                                                                                                        |
| Forfremmelse                     | Kampanjehandlinger gir deg et navngitt sted der du kan tildele økninger. Merk av for **Aktiver anbefaling** for å angi en anbefaling for ansatte som skal motta kampanjer.  Ansatte uten en anbefalt økning, får ikke **Kampanje**-handlingen lagt til i poster for fast kompensasjon.                                                                       |
| Annen nivåendring            | I eksemplet ovenfor er **Degradering** navnet på **Fast kompensasjon**-handlingen med typen **Annen nivåendring**. Dette genererer en 0 (null-endring) retningslinjeøkning slik at du kan angi et anbefalingsbeløp for å justere den ansattes lønnssats. (Velg alternativet **Aktiver anbefaling**.) Ansatte uten en anbefaling får ikke denne handlingen lagt til i poster for fast kompensasjon. |

Du kan bare legge til **Fast kompensasjon**-handlinger av typen trinnvis plan.

| Type handling for fast kompensasjon | Funksjonalitet                |
|--------------------------------|------------------------------|
| Trinn                           | I kategorien **Generelt** angir du om denne trinnhandlingen skal flytte de ansatte fremover 0 trinn 1 trinn eller to trinn.                                                                                  |
|                                | **0 trinn** - De ansatte vil motta lønnssatsen for det aktuelle trinnet de er på.                                                                                                                      |
|                                | **1 trinn** - Systemet kontrollerer om den ansatte allerede er på siste referansepunkt for nivået.                                                                                             |
|                                | **2 trinn** – Den ansatte flyttes fremover to trinn på det gjeldende nivået. Den ansatte kan bare flyttes ett eller ingen trinn når de har nådd det siste referansepunktet for nivået. |

## <a name="run-the-compensation-process"></a>Kjøre kompensasjonsprosessen
Når prosesshendelsen er definert med nødvendige datofelt, planer og handlinger, kan du klikke **Kjør prosess** på siden **Prosesshendelse**, som åpner dialogboksen **Kjør prosesshendelser for kompensasjon**. Klikk dialogboksen **Vis resultater for hendelsesbehandling** for å se hvordan kompensasjonsbeløp ble beregnet for hver ansatt. Hvis du velger **OK**, kjøres kompensasjonsprosessen for alle ansatte i de valgte kompensasjonsplanene per syklusens sluttdato.

## <a name="view-the-process-results"></a>Vis prosessresultater
Hvis du vil vise prosessresultatene, kan du åpne **Prosessresultater**-siden. En ny kompensasjonshendelse opprettes hver gang prosesshendelsen kjøres. Dette tillater prøvekjøringer, utførelse av justeringer og kjøring av kompensasjonshendelsen flere ganger for å se hvordan ulike endringer påvirker ansattkompensasjon.

**Prosessresultat**-siden inneholder informasjon om prosesskjøringen, inkludert når utførelsen fant sted, brukeren som kjørte prosessen, og om det oppstod noen feil da prosessen ble kjørt. Velg **Låst** for å deaktivere knappen **Last inn kompensasjon** og hindre at noen laster inn kompensasjonshendelser til ansattpostene. Hvis du velger knappen **Resultatene for ansatte**, vises listen over ansatte som er inkludert i utførelsen.

Alternativet **Ansattresultater** viser informasjon om selve prosessen, samt noen kompensasjonshandlinger som utføres i prosessen. Delen **Fast kompensasjon** inneholder en post for hver handling som er inkludert i prosesshendelsen for kompensasjonsplanen. Kolonnene **Gjeldende retningslinje** og **Anbefaling** viser mer informasjon om handlingen som er valgt i delen **Fast kompensasjon**. Hvis **Aktiver anbefalinger** var merket av for handlingen, kan **Anbefaling**-feltene redigeres. Dette gjør at du kan justere beløpene for ansatt manuelt. Merk at hvis du merket av for **Bruk forrige resultat** for handlingen på prosesshendelsen, må du manuelt oppdatere beløpene for alle avhengige handlinger.

Når du har kontrollert kompensasjonsbeløpene for en ansatt og gjort eventuelle justeringer i de anbefalte verdiene, kan du endre **Status** på **Ansatthendelse**-linjen for å angi om hendelsen er godkjent eller skal ignoreres. Hvis du vil, kan du slette eventuelle endringer i den ansattes anbefaling ved å klikke **Omberegn** knappen. Dette merker den eksisterende ansatthendelsen med statusen Ignorer og oppretter en ny ansatthendelse med omberegnede verdier.

## <a name="loading-approved-compensation-changes"></a>Laste inn godkjente kompensasjonsendringer
Når en eller flere ansatthendelser får statusen oppdatert til **Godkjent**, kan de lastes til de ansattes faste kompensasjonsposter. Dette kan gjøres ved å velge hver ansatthendelse én om gangen og klikke **Last inn ansattkompensasjon** på siden **Ansattresultater**, eller ved å klikke **Last inn kompensasjon** på siden **Prosessresultater** for å laste inn alle godkjente ansatthendelser samtidig.

Hvis du velger **OK** i dialogboksen **Last inn kompensasjon**, legges kompensasjonshandlingslinjer som ikke er null, til på siden **Fast kompensasjon for ansatt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
