---
title: Containerbruk
description: Dette emnet beskriver hvordan du automatiserer containerbruken av laster. Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9293beba6a251a670b918fecbb2315a5e94660b9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572271"
---
# <a name="containerization"></a>Containerbruk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du automatiserer containerbruken av laster. Automatisert containerbruk oppretter containere og plukkarbeidet for forsendelser når en bølge behandles.

Hvis du vil konfigurere containerbruk, må du opprette følgende:

- **Containertype** – Definer fysiske egenskaper for containerne. Bruk containertyper for å pakke lagervarer i en bestemt pakke- og størrelsestype, for eksempel hyller eller paller.
- **Containergrupper** – Opprett grupper med containertyper som ligner. En containergruppe kan for eksempel inkludere containertyper som har lignende størrelsesdimensjoner. En containergruppe angir rekkefølgen containere pakkes i, og fyllprosenten for hver container.
- **Mal for build for container** – Opprett maler somdefinerer regler for containerbruk. For eksempel regler for blanding av lager og andre pakkestrategier.
- **Bølgemaler** – Angi én eller flere bølgemaler til å opprette en plukkarbeidet for containerbruk.

## <a name="create-wave-templates-for-containerization"></a>Opprett bølgemalr for containerbruk

Du må angi én eller flere bølgemaler for forsendelse for containerbruk. Bølgemaler inneholder kriterier som bestemmer følgende:

- Hvordan behandle bølger. Denne kan være manuell eller automatisk.
- Opprette plukkarbeid. Dette bestemmes av bølgemetodene. Bølgemalen må inneholde **containerbruk**-metoden.
- Hvordan samsvare varer og fordelingslinjer med en bølge.

Hvis du vil ha mer informasjon, kan du se [Bølgemaler](wave-templates.md).

## <a name="create-container-types"></a>Opprett containertyper

Bruk containertyper for å opprette beskrivelser for containere, herunder maksimumsverdiene for fysiske dimensjoner og vektkapasitet. Når en bølge for containerbruk behandles, opprettes containere basert på informasjonen om containertype.

Hvis du vil konfigurere en containertype, gjør du følgende:

1. Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containertype**.
1. Velg **Ny** for å opprette en ny containertype.
1. Angi en unik ID og beskrivelse for containertypen.
1. I **Taravekt**-feltet angir du den faktiske eller beregnede vekten til containeren.
1. I **Maksimumsvekt**-feltet angir du den maksimale vekten som containeren tåler.
1. I feltene **Maksimumsvolum for containerbruk**, **Maksimumslengde for containerbruk**, **Maksimumsbredde for containerbruk** og **Maksimumshøyde for containerbruk** angir du de fysiske dimensjonene til containeren.

    > [!NOTE]
    > Verdiene for lengde og bredde kan skiftes ut. Dette betyr at du kan rotere varer sidelengs eller på x-aksen, om nødvendig. Hvis lengden er 2 meter, og bredden 1 meter, kan du for eksempel endre lengden til 1 meter og bredden til 2 meter. Vær oppmerksom på at dette ikke gjelder for høydedimensjonen. Du kan ikke endre høydeverdien for å rotere et element loddrett.

1. Velg egendefinerte attributtverdier for containeren i attributtfeltene. Attributter er egendefinerte verdier som brukes til å filtrere eller sortere elementer basert på en verdi som ellers ikke er tilgjengelig. Hvis du vil pakke varer for en bestemt kunde, kan du for eksempel opprette et attributt for navnet på kunden. Du oppretter attributter på siden **Containerattributter**.

## <a name="create-container-groups"></a>Opprett containergrupper

Du kan definere logiske grupper med containertyper. For hver gruppe kan du angi rekkefølgen containere pakkes i og fyllprosenten for hver container. Størrelsesdimensjoner for varen bestemmer om den passer inn i en container. Containeren som er nærmest størrelsesdimensjonen for varen, brukes. Hvis du har flere containertyper i en gruppe, anbefaler vi at du ordner rekkefølgen etter størrelse, slik at den største containeren kommer først, som nummer 1 i rekkefølgen, og den minste containeren kommer sist.

Hvis du vil konfigurere en containergruppe, gjør du følgende:

1. Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**.
1. Velg **Ny** for å opprette en containergruppe.
1. Angi en unik ID og beskrivelse for containergruppen.
1. På **Detaljer**-hurtigfanen velger du **Ny** for å legge til en containertype i gruppen.
1. Velg en containertype i feltet **Containertype**.
1. Velg **Flytt opp** eller **Flytt ned** for å angi rekkefølgen containertypene skal pakkes i.

## <a name="create-container-build-templates"></a>Opprett malr for containerversjoner

Du kan definere regler for containerbruksprosessen, for eksempel kombinasjonsregler for beholdning og andre pakkestrategier. Du kan for eksempel definere en regel slik at arbeidere ikke kan pakke tildelingslinjer som representerer salgsordrer fra andre kunder i den samme containeren.

Hvis du vil konfigurere en mal for containerversjon, følger du fremgangsmåten nedenfor.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Containere** \> **Mal for build for container**.
1. Opprett en ny mal for containerversjon.
1. I feltene **Navn på containerbruk** og **Sekvensnummer** angir du navnet på malen for containerbruk og ordren som matches mot tildelingslinjer.

    > [!NOTE]
    > Systemet bruker den første malen som tildelingslinjen oppfyller spørringsvilkårene for. Flytt derfor malen med de mest spesifikke kriteriene øverst i listen. Jo bredere kriterier, desto mer sannsynlig at en fordelingslinje oppfyller kriteriene. Dette kan føre til at linjer tilordnes til feil container. Om nødvendig kan du velge **Flytt opp** eller **Flytt ned** for å endre rekkefølgen på malene.

1. I feltet **Containergruppe-ID** velger du containergruppen å opprette containere fra.
1. I feltet **Grunnleggende spørringstyper** velger du spørringstypen som bestemmer hva som skal pakkes og hva filterspørringen skal baseres på. Følgende alternativer er tilgjengelige:

      - **Salgstildelingslinje** – Pakketildelingslinjer som er opprettet for salgsordrer.
      - **Overføringstildelingslinje** – Pakketildelingslinjer som er opprettet for overføringsordrer.
      - **Container** – Pakk en container som allerede er opprettet av containerbruk-prosessen. Dette brukes for eksempel til å neste containere.

        > [!NOTE]
        > Hvis du vil bruke nestede containere, må du gjøre slik at containerbrukmetoden kan gjentas. Hvis du vil ha mer informasjon, kan du se [Bølgemaler](wave-templates.md).

1. På **Generelt**-hurtigfanen i feltet **Bølgetrinnkode** angir du den unike ID-en for bølgeprosessmetoden som kobler containerbyggemalen til trinnene i en bølgemal.
1. Merk av for **Tillat oppdeling av plukking** for å tillate arbeidere å pakke varer fra en arbeidsordre i separate containere. Dette krever at hele antallet passer i containeren. Den største måleenheten i tildelingslinjen brukes alltid.
1. I feltet **Pakk etter enhet** velger du måleenheten som representerer containeren. Du kan for eksempel angi at en sak er en container. Hvis du pakker etter måleenheten, kan du ikke også angi en containergruppe, fordi måleenheten er containeren.
1. I feltet **Pakkestrategi for container** velger du pakkestrategien som skal brukes. Følgende alternativer er tilgjengelige:

    > [!NOTE]
    > Strategien gjelder bare for salgstildelingslinjer og overføringstildelingslinjer.

      - **Pakk i alle åpne containere**– Systemet vurderer om tildelingslinjen får plass i en container som ble opprettet i løpet av containerbruk-syklusen.
      - **Pakk bare i gjeldende container** – Systemet vurderer bare om tildelingslinjen får plass i containeren som ble opprettet sist.

    Hvis du vil ha mer informasjon og eksempler som viser hvordan du arbeider med containerpakkestrategier, kan du se [Strategier for containerpakking](container-packing-strategy-overview.md).

1. Hvis du vil definere regler for pakketildelingslinjer i containere, velger du **Blanding av brudd i kombinasjonslogikk**. Du kan for eksempel opprette en regel som tillater ansatte å pakke tildelingslinjer for to ulike varer, i den samme containeren. Hvis du vil definere en kombinasjonsregel, gjør du følgende:

    1. På siden **Blanding av brudd i kombinasjonslogikk** velger du **Ny**.
    1. I **Tabell**-feltet velger du tabellen som inneholder feltet som skal brukes som et kriterium for brudd i kombinasjonslogikken.
    1. I feltet **Velg felt** velger du feltet som skal brukes som et kriterium for brudd i kombinasjonslogikken.
    1. Gjenta disse trinnene til du har lagt til alle kriteriene for brudd i kombinasjonslogikk.

    > [!NOTE]
    > Hvis du bruker kombinasjonslogikk, anbefaler vi at du sorterer etter de samme feltene i filterkriteriespørringen. Dette reduserer antall containere som opprettes.
