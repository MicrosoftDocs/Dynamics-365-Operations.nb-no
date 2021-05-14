---
title: Opprette og behandle avvik
description: Dette emnet beskriver hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956212"
---
# <a name="create-and-process-nonconformances"></a>Opprette og behandle avvik

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan du utfører behandling av avvik, basert på en eksisterende kvalitetsordre. Avviksbehandling utføres vanligvis av en kvalitetsassistent. Det er en forutsetning at du har en tilgjengelig kvalitetsordre. (Hvis du vil ha informasjon om hvordan du oppretter en kvalitetsordre, kan du se [Inspisere kvaliteten på varer](inspect-quality-goods.md).)

Før en bruker kan behandle godkjenningen av et avvik, må en arbeider tilordnes dem i **Person**-feltet på **Brukere**-siden. Før brukeren kan bruke dokumentnotatene, må alternativet **Aktiver dokumentoversikt** være satt til *Ja* i brukeralternativene.

## <a name="create-a-nonconformance"></a>Opprette et avvik

Hvis du vil opprette et avvik, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. I handlingsruten velger du **Ny**.
1. Velg problemtypen som ble funnet under inspeksjonsprosessen, i **Problemtype**-feltet i dialogboksen **Opprett avvik**.
1. Velg **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Godkjenne eller avvise et avvik

Hvis du vil godkjenne eller avvise et avvik, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til en rettelse i avvik som er godkjent.

1. Velg **Funksjoner \> Godkjenn avvik** i handlingsruten for å godkjenne avviket, eller **Funksjoner \> Avvis avvik** for å avvise det. Du kan knytte godkjente avvik til [relaterte operasjoner](../quality-operations.md). På denne måten kan du registrere arbeid som er utført som en del av avvikshåndteringen og behandlingen av rettelsesbehandling.
1. Du blir bedt om å bekrefte valget. Klikk på **Ja** for å fortsette.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Legge til operasjoner og andre detaljer i avvik

Når du har opprettet et avvik, kan du begynne å legge til tilknyttede operasjoner og angi tilleggsinformasjon om disse operasjonene. Du kan bare legge til relaterte operasjoner i avvik som er godkjent.

I tillegg til den grunnleggende informasjonen kan du legge til følgende detaljer i en operasjon:

- **Varer** – Du kan opprette en liste over varer som forbrukes for å utføre rettelsen. Varene kan for eksempel være produkter som kreves for å reparere utstyr eller ingredienser som kreves for å omarbeide et ferdig produkt.
- **Kvalitetsstyringstillegg** – Du kan opprette en liste over tillegg som påløper eller faktureres eksterne kilder.
- **Timeregistrering** – Du kan opprette en logg over tiden som hver arbeider bruker på operasjonen.

De gjenværende innstillingene er valgfrie. Kostnaden for hver vare, kvalitetsgebyr og timeregistreringen summeres og vises på operasjonen. Du kan ikke redigere **Kostnad**-feltet direkte på operasjonen.

### <a name="create-an-operation-for-a-nonconformance"></a>Opprette en operasjon for et avvik

Hvis du vil opprette en operasjon for et avvik, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.

1. I handlingsruten velger du **Relaterte operasjoner**.
1. Velg **Ny** i handlingsruten på siden **Relaterte operasjoner** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Operasjon** – Velg koden for operasjonen som skal utføres for avviket.
    - **Årsak** – Angi en detaljert beskrivelse som forklarer hvorfor operasjonen er nødvendig.
    - **Salgsordre** – Hvis den valgte operasjonskoden er knyttet til salgsordretypen, velger du salgsordren du kobler operasjonen til.
    - **Bestilling** – Hvis den valgte operasjonskoden er knyttet til bestillingstypen, velger du bestillingen du kobler operasjonen til.

1. Lukk sidene.

### <a name="add-items-to-an-operation"></a>Legge til varer i en operasjon

Følg denne fremgangsmåten for å legge til varer i en operasjon.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.

1. I handlingsruten velger du **Relaterte operasjoner**.
1. På siden **Relaterte operasjoner** velger du operasjonen du vil legge til varer i.
1. Velg **Varer** i handlingsruten.
1. Velg **Ny** i handlingsruten på siden **Relaterte operasjoner** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Varenummer** – Velg produktet som skal forbrukes som del av den valgte operasjonen.
    - **Antall** – Angi antall varer som skal forbrukes.

    > [!NOTE]
    > Du kan vise kostnaden for varen i feltet **Kostnad** i kategorien **Generelt**. Kostnaden som vises der, kommer fra kostnaden som er definert på **Frigitt produkt**-siden. Kostnaden kan ikke oppdateres direkte på siden **Relatert operasjonsvare**. Kostnadene for alle varer som legges til på siden **Relaterte operasjonsvarer**, legges automatisk til i **Kostnad**-feltet på **Relaterte operasjoner**-siden.

1. Gjenta det forrige trinnet for hver tilleggsvare du må legge til.
1. Lukk sidene.

### <a name="add-quality-charges-to-an-operation"></a>Legge til kvalitetsgebyrer i en operasjon

Følg denne fremgangsmåten for å legge til kvalitetsstyringstillegg i en operasjon.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.

1. I handlingsruten velger du **Relaterte operasjoner**.
1. På siden **Relaterte operasjoner** velger du operasjonen du vil legge til kvalitetsstyringstillegg i.
1. I handlingsruten velger du **Kvalitetsstyringstillegg**.
1. Velg **Ny** i handlingsruten på siden **Relaterte operasjonstillegg** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Tilleggskode** – Velg kvalitetstillegget du vil legge til.
    - **Beskrivelse** – Angi en detaljert beskrivelse av tillegget.
    - **Gebyrverdi** – Angi gebyrbeløpet.

1. Gjenta det forrige trinnet for hvert tilleggsgebyr du må legge til.
1. Lukk sidene.

> [!NOTE]
> Beløpet i feltet **Gebyrverdi** summeres automatisk for alle kvalitetstillegg, og legges til andre beløp i **Kostnad**-feltet på siden **Relaterte operasjoner**.

### <a name="create-a-timesheet-on-an-operation"></a>Opprette en timeregistrering for en operasjon

Følg denne fremgangsmåten for å legge til en timeregistrering i en operasjon.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til eller opprette operasjoner i avvik som er godkjent.

1. I handlingsruten velger du **Relaterte operasjoner**.
1. På siden **Relaterte operasjoner** velger du operasjonen du vil legge til en timeregistrering i.
1. Velg **Timeregistrering** i handlingsruten.
1. Velg **Ny** i handlingsruten på siden **Relaterte operasjonstimeregistreringer** for å legge til en rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Dato** – Angi datoen da arbeidet ble utført. Som standard settes feltet til gjeldende dato.
    - **Arbeider** – Velg arbeideren som utførte arbeidet. Som standard er dette feltet satt til den arbeideren som er tilordnet den gjeldende brukeren.
    - **Operasjonstimer** – Angi antall timer som ble arbeidet på den valgte operasjonen.
    - **Fakturert** – Merk av i denne avmerkingsboksen hvis tiden er belastet en kunde eller leverandør på en faktura.

    > [!NOTE]
    > Du kan vise kostnaden i **Kostnad**-feltet i kategorien **Generelt**. Kostnaden beregnes ved å bruke satsen du definerer på siden **Lagerstyringsparametere**.

1. Gjenta det forrige trinnet for hver timeregistreringslinje du må legge til.
1. Lukk sidene.

> [!NOTE]
> Beløpet i feltet **Kostnad** summeres for alle timeregistreringslinjer og legges til andre beløp i **Kostnad**-feltet på siden **Relaterte operasjoner**.

## <a name="add-a-correction-to-a-nonconformance"></a>Legge til en rettelse i et avvik

Hvis du vil legge til en rettelse i et avvik, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til en rettelse i avvik som er godkjent.

1. I handlingsruten velger du **Korreksjoner**.
1. I handlingsruten velger du **Ny** for å legge til en rad i rutenettet på siden **Rettelser**. Angi deretter følgende felter for den nye raden:

    - **Diagnose** – Velg diagnosetypen som identifiserer rettelsestypen du oppretter.
    - **Arbeider** – Velg personen som er økonomisk ansvarlig for rettelsen.
    - **Rettelsesprioritet** – Velg et alternativ for å angi hvordan rettelsen skal prioriteres (*Lav*, *Normal* eller *Høy*).
    - **Ønsket dato** – Angi datoen da den korrigerende handlingen ble forespurt.
    - **Planlagt dato** – Angi datoen da rettelsen forventes å være fullført.
    - **Kortsiktig løsning** – Merk av i denne avmerkingsboksen hvis den korrigerende handlingen retter avviket bare i en kort tidsperiode.

1. Lukk sidene.

## <a name="mark-a-correction-as-completed"></a>Merke en rettelse som fullført

Hvis du vil merke en avviksrettelse som fullført, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.

    > [!NOTE]
    > Du kan bare legge til en rettelse i avvik som er godkjent.

1. I handlingsruten velger du **Korreksjoner**.
1. Velg **Rettelser**-siden i rutenettet, og velg rettelsen du vil merke som fullført.
1. Velg **Merk som fullført** i handlingsruten.
1. Du blir bedt om å bekrefte valget. Velg **OK** for å fortsette. **Fullføringsdato- og -klokkeslett**-feltet settes til gjeldende dato og klokkeslett, og det merkes av i avmerkingsboksen **Fullført**.
1. Lukk siden.

## <a name="reopen-a-completed-correction"></a>Åpne en fullført rettelse på nytt

Hvis du vil åpne er fullført rettelse på nytt, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Avvik**.
1. Velg avviket du vil oppdatere, i listen.
1. I handlingsruten velger du **Korreksjoner**.
1. På **Rettelser**-siden i rutenettet velger du rettelsen du vil åpne på nytt.
1. I handlingsruten velger du **Åpne på nytt**.
1. Du blir bedt om å bekrefte valget. Velg **OK** for å fortsette. Verdien tømmes fra **Fullføringsdato- og -klokkeslettfeltet**, og det er ikke merket av for **Fullført**.
1. Lukk siden.

Du kan nå foreta flere endringer eller oppdateringer i rettelsen. Når du er ferdig, kan du merke rettelsen som fullført på nytt.

## <a name="close-a-nonconformance"></a>Lukke et avvik

Hvis du vil lukke et avvik, følger du disse trinnene.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Kvalitetsstyring \> Kvalitetsordrer**.
1. Velg en kvalitetsordre i rutenettet.
1. Velg **Forespørsler \> Avvik** i handlingsruten.
1. På **Avvik**-siden velger du målavviket i rutenettet.
1. Velg **Funksjoner \> Lukk avvik** i handlingsruten.
1. Du blir bedt om å bekrefte valget. Klikk på **Ja** for å fortsette.
1. Lukk sidene.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over kvalitetsstyring](../quality-management-processes.md)
- [Aktivere kvalitets- og avviksstyring](../enable-quality-management.md)
- [Arbeidere som er ansvarlige for å godkjenne avvik](../quality-responsible-workers.md)
- [Karantenesoner for avvik](../quality-quarantine-zones.md)
- [Diagnosetyper for avvik](../quality-diagnostic-types.md)
- [Kvalitetsendringer for avvik](../quality-charges.md)
- [Operasjoner for avvik](../quality-operations.md)
- [Kvalitetsstyring for lagerprosesser](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
