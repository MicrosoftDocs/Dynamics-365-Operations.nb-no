---
title: Systemstyrt gruppeplukking
description: Dette emnet gir en oversikt over systemstyrt gruppeplukking i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 390e0a3379a6482e99a13f4f7835b5264e3747ac
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217247"
---
# <a name="system-directed-cluster-picking"></a>Systemstyrt gruppeplukking

[!include [banner](../includes/banner.md)]

Gruppeplukking er en stykkplukkingsprosess som lar deg plukke varer for flere ordrer samtidig ved å gruppere dem i plukkgrupper. Du må da gå til plukkstedet bare én gang. Denne funksjonaliteten brukes vanligvis med små ordreplukking eller antall som er mindre enn små kvanta.

Når systemstyrt gruppeplukking er definert, kan du gruppeplukke arbeidshoder, basert på en systemgenerert gruppe. Systemet gruppeplukker ordrer opp til antall stillinger som er angitt i gruppeprofilen. Derfor kan du plukke flere ordrer samtidig uten å måtte opprette en gruppe manuelt.

Systemstyrt gruppeplukking tilbyr et alternativ til manuell gruppebygging, der en gruppeprofil brukes til å opprette en gruppe. Flere oppsettsrelaterte linjer må defineres i gruppeprofilen før den brukes:

- **Antall stillinger** tilsvarer antall ordrer som skal plasseres i en gruppe. Derfor tilsvarer det antall seff.
- **Bryt gruppe** bestemmer når gruppen skal brytes.
- **Generer gruppe-ID** kontrollerer om gruppe-IDen skal genereres av systemet eller angis av brukeren.
- **Sorteringsbekreftelsestype** avgjør om posisjonsverifisering er nødvendig.

Et nytt menyelement for mobilenhet brukes til systemstyrt gruppeplukking. Gruppeprofil-IDen må angis for alternativet **Styrt av**. I tillegg kan den systemstyrte spørringsrekkefølgen gruppere ordrer, basert på firmaspesifikke kriterier. Derfor kan du ytterligere optimalisere tildelingen av arbeidsordrer ved å angi tilpassede sorteringskriterier i den systemstyrte spørringsrekkefølgen.

Når systemstyrt gruppeplukking utføres, presenteres lagerarbeidere med en gruppe der plukkordrer er forhåndstildelte til gruppestillinger. Arbeidere kan derfor begynne å plukke en vare for flere arbeidsordrer ved å gå til plukkstedet bare én gang. Plukkprosessen for systemstyrt gruppeplukking er den samme som prosessen for brukerstyrt gruppeplukking.

## <a name="set-up-system-directed-cluster-picking"></a>Konfigurere systemstyrt gruppeplukking

### <a name="create-cluster-profiles"></a>Opprette gruppeprofiler

Gruppeprofiler kontrollerer hvordan systemet oppretter hver gruppe. Hvis det kreves forskjellige grupper, bør det opprettes en annen gruppeprofil for hvert menyelement for mobilenhet.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.
2. Velg **Ny**.
3. Angi **2 posisjon** i **Gruppeprofil-ID**-feltet.
4. Angi **2 posisjon** i **Navn**-feltet.
5. Angi følgende felt i hurtigfanen **Generelt**:

    - **Generer gruppe-ID:** sett dette alternativet til **Ja**. Dette alternativet bestemmer om gruppe-IDen opprettes automatisk av systemet, eller om brukeren skal opprette den på begynnelsen av plukkingen.
    - **Aktiver stillinger:** sett dette alternativet til **Ja**. Dette alternativet bestemmer om stillingsnavnene genereres automatisk basert på oppsettet for stillingsnavnet. Hvis dette alternativet settes til **Nei**, brukes nummerskilt-ID-en for stillingen.
    - **Maksimalt antall stillinger:** Angi **2**. Dette feltet fastsetter det maksimale antallet stillinger som gruppen kan ha (det vil si maksimalt antall esker, seff og så videre).
    - **Stillingsnavn:** Velg **Numerisk**, slik at stillingene navngis ved hjelp av kontinuerlige tall. Hvis du velger **Alfabetisk**, navngis stillingene i alfabetisk rekkefølge.
    - **Pausegruppe ved:** Velg **Plasser**. Dette feltet bestemmer når gruppen brytes.
    - **Sorteringsbekreftelsestype:** Velg **Posisjonsskanning**. Dette feltet angir om plasser-til-stilling-trinnet er bekreftet.

6. På hurtigfanen **Gruppesortering** kan du definere sorteringskriterier ved å opprette en ny linje og angi følgende felt:

    - **Serienummer:** Dette feltet bestemmer sekvensen som systemet sorterer etter. En verdi angis automatisk, men du kan endre den etter behov.
    - **Feltnavn:** Velg **WMSLocationId**. Dette feltet bestemmer feltet som linjen bruker til sorteringskriterier.
    - **Sortering:** Velg **Stigende**. Dette feltet angir om sorteringen utføres i stigende eller synkende rekkefølge.

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

Hvis du vil opprette et nytt menyelement for mobilenhet for systemstyrt gruppeplukking og koble gruppeprofil-IDen til menyelementet for mobilenhet, følger du denne fremgangsmåten.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
2. Velg **Ny**.
3. I feltet **Menyelementnavn** angir du **SD-gruppe**.
4. Angi **SD-gruppe** i **Tittel**-feltet.
5. Velg **Arbeid** i feltet **Modus**.
6. Angi alternativet **Bruk eksisterende arbeid** til **Ja**.
7. Angi følgende felt i hurtigfanen **Generelt**:

    - **Styrt av:** Velg **Systemstyrt**.
    - **Generer nummerskilt:** Sett dette alternativet til **Ja**.
    - **Gruppeprofil-ID**: Velg **2 posisjon**.

8. I hurtigfanen **Arbeidsklasser** konfigurerer du den gyldige arbeidsklassen for dette menyelementet for mobilenhet ved å angi følgende felt:

    - **Arbeidsklasse-ID**: Sørg for at **Salg** er angitt.
    - **Arbeidsordretype**: Sørg for at **Salgsordrer** er angitt.

9. Følg denne fremgangsmåten for å angi en ny systemstyrt arbeidssekvensspørring:

    1. Velg **Ny**.
    2. Angi **1** i feltet **Serienummer**.
    3. I **Beskrivelse**-feltet velger du **Arbeidsprioritet – arbeids-ID**.

10. Velg **Rediger spørring** på menyen.
11. I kategorien **Sortering** angir du følgende felt:

    - **Tabell:** Velg **Arbeid**.
    - **Avledet tabell:** Velg **Arbeid**.
    - **Felt:** Velg **Arbeidsprioritet**.
    - **Søkeretning:** Velg **Stigende**.
    - **Tabell:** Velg **Arbeid**.
    - **Avledet tabell:** Velg **Arbeid**.
    - **Felt:** Velg **Arbeids-ID**.
    - **Søkeretning:** Velg **Stigende**.

Systemet vil nå sortere arbeids-IDer i gruppen, først etter arbeidsprioritet og deretter etter arbeids-ID.

### <a name="set-up-a-mobile-device-menu"></a>Definere en mobilenhetsmeny

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
2. Legg til menyelementet du nettopp opprettet, i ønsket meny.

## <a name="example"></a>Eksempel

### <a name="create-picking-work"></a>Opprett plukkarbeid

Før du kan definere systemstyrt gruppeplukking, må du opprette noe kvalifisert utgående arbeid. Gruppeprofilen du opprettet tidligere, angir to gruppestillinger. Derfor må du opprette minst to arbeids-IDer.

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
2. Velg **Ny** for å opprette en salgsordre.
3. Velg en kunde i **Kundekonto**-feltet.
4. På hurtigfanen **Generelt**, i **Lager**-feltet, velger du lageret **62**.
5. Velg **OK**.
6. I hurtigfanen **Salgsordrelinjer** velger du **Legg til linje**.
7. Velg **A0001** i feltet **Varenummer**.
8. I feltet **Antall** angi **1**.
9. Velg **Legg til linje** for å legge til en ny linje.
10. Velg **A0002** i feltet **Varenummer**.
11. I feltet **Antall** angi **3**.
12. Gjenta trinn 2 til 6.
13. Velg **A0001** i feltet **Varenummer**.
14. I feltet **Antall** angi **4**.
15. Velg **Legg til linje** for å legge til en ny linje.
16. Velg **A0002** i feltet **Varenummer**.
17. I feltet **Antall** angi **2**.

Reserver beholdningen, og frigi den til lageret. To forskjellige arbeids-IDer opprettes. Hver arbeids-ID har to plukklinjer.

### <a name="run-the-mobile-device-flow"></a>Kjør flyten for mobilenhet

1. På mobilenheten velger du menyen som inneholder det nye menyelementet for mobilenhet.
2. Velg **SD-gruppe**-menyelementet, og start plukkingen. Det opprettes en gruppe, og de to arbeids-IDene som du opprettet tidligere, er knyttet til den. Hvis du har opprettet mer enn to arbeids-IDer, legges bare de to første til i gruppen. Legg merke til at arbeids-IDene legges til gruppen i stigende rekkefølge, som du angav i spørringsoppsettet.

    > [!NOTE]
    > Den nye gruppen opprettes automatisk bare hvis nok ekstra arbeids-IDer ble opprettet tidligere. Ellers vises følgende melding: "Finner ikke nok arbeid for gruppen."

    Når du har valgt menyen, vises det første plukkskjermbildet. Systemet samler alle samsvarende plukklinjer fra de to arbeids-IDene, og dirigerer deg til å gå til plukkstedet én gang, slik at du kan oppfylle begge ordrene ved hjelp av én plukking. Denne prosessen utføres på samme måte som prosess for brukerstyrt gruppeplukking.

3. Bekreft den første plukkingen. Du må deretter angi stillingsnavnet for å bekrefte at varene ble plassert i riktig posisjon.
4. Gjenta denne prosessen til alle varene er plukket og satt til riktig posisjon.
5. Det siste trinnet på mobilenheten er å sette gruppen til den endelige plasseringen. Når denne plasseringsoperasjonen er bekreftet, lukkes og brytes gruppen, basert på verdien som du angir for **Pausegruppe ved** -feltet i gruppeprofilen. Arbeids-IDer lukkes også.
6. En "Gruppe fullført"-melding vises på mobilenheten.
