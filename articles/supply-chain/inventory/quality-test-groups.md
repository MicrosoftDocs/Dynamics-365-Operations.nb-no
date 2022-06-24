---
title: Testgrupper for kvalitetsstyring
description: Denne artikkelen beskriver hvordan du oppretter testgrupper, slik at flere tester kan brukes med kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7722bc92d8c2bf52d6a798a93f07af44037d4e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857713"
---
# <a name="quality-management-test-groups"></a>Testgrupper for kvalitetsstyring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter testgrupper, slik at flere tester kan brukes med kvalitetsordrer i Microsoft Dynamics 365 Supply Chain Management.

Du kan bruke **Testgrupper**-siden til å definere, redigere og vise testgrupper og de individuelle testene som er tilordnet til dem. Den øvre delen på siden viser testgrupper, og den nedre delen viser testene som er tilordnet til en valgt testgruppe.

Du tilordner flere policyer til en testgruppe, for eksempel en prøveplan, et akseptabelt kvalitetsnivå og kravet for destruktiv testing. Deretter når du tilordner en individuell test til en testgruppe, definerer du tilleggsinformasjon, for eksempel sekvensen, dokumenter og gyldighetsdatoer. For en kvantitativ test inkluderer informasjonen du definerer, også de akseptable målingsverdiene. For en kvalitativ test inkluderer informasjonen testvariabelen og standardresultatet.

Testgruppen som er tilordnet en kvalitetsordre, definerer standardsettet med tester som må utføres for den bestemte varen. Du kan imidlertid legge til, slette eller endre tester for kvalitetsordren. Testresultater rapporteres for hver test på en kvalitetsordre.

Når du definerer en testgruppe, kan du velge å angi en prøve for en vare. Vareprøver brukes til å definere beløpet for produktet som må testes. Hvis du vil ha mer informasjon, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md). Du kan også angi om testene i en testgruppe er destruktive. I en destruktiv test ødelegges vareprøven, og antallet fjernes fra lagerbeholdningen.

## <a name="example-of-a-test-group"></a>Eksempel på en testgruppe

Et produksjonsfirma definerer en testgruppe for hver variasjon av retningslinjene for kvalitet. De ulike testgruppene gjenspeiler forskjeller i prøveplanene, settet med tester som må utføres sammen, det akseptable kvalitetsnivået og andre faktorer. For kvantitative tester er det også forskjeller i de akseptable målingsverdiene. Hvis firmaet vil fremtvinge sine retningslinjer for kvalitet, tilordner firmaet en testgruppe til hver regel som brukes til å generere kvalitetsordrer automatisk på siden **Kvalitetstilknytninger**. Det tilordner også en testgruppe til kvalitetsordrer som opprettes manuelt.

## <a name="create-a-test-group"></a>Opprette en testgruppe

Hvis du vil opprette en testgruppe, følger du disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testgrupper**.
1. Velg **Ny** i handlingsruten for å legge til en rad i rutenettet i øvre del av siden. Angi deretter følgende felter for den nye raden:

    - **Testgruppe** – Angi en unik ID eller et unikt navn for testgruppen.
    - **Beskrivelse** – Angi en detaljert beskrivelse av testgruppen.
    - **Akseptabelt kvalitetsnivå** – Angi den totale prosentsatsen av testresultater som må bestå for at gruppen med tester skal vurderes som bestått.
    - **Vareprøve** – Velg en prøve for en vare. Hvis du vil ha mer informasjon, kan du se [Vareprøve for kvalitetsstyring](quality-item-sampling.md).
    - **Destruktiv** – Merk av i denne avmerkingsboksen for å angi at testgruppen skal undersøke varene som er testet.

1. Mens den nye raden fremdeles er merket, velger du kategorien **Generelt** i den øvre delen av siden. Noen av innstillingene for testgruppen som er valgt i kategorien **Oversikt**, gjentas her. I tillegg kan du angi følgende felt for gruppen:

    - **Oppdater lagerpartiattributt** – Når du setter dette alternativet til *Ja* her, blir det automatisk satt til *Ja* for alle nye tester som legges til testgruppen i den nedre delen av siden.
    - **Oppdater partidisposisjon** – Når du setter dette alternativet til *Ja*, og hvis varen som blir testet, er partikontrollert, blir partidisposisjonen automatisk oppdatert med verdien som er valgt i feltet **Mislykket disposisjon for kvalitetsordrepart** eller **Sendt disposisjon for kvalitetsordreparti**.
    - **Mislykket disposisjon for kvalitetsordreparti** – Velg partidisposisjonskoden som skal tilordnes når en kvalitetsordre som inkluderte denne testgruppen, mislykkes fordi den ikke oppfyller det akseptable kvalitetsnivået.
    - **Sendt disposisjon for kvalitetsordreparti** – Velg partidisposisjonskoden som skal tilordnes når en kvalitetsordre som inkluderte denne testgruppen, lykkes fordi den oppfyller det akseptable kvalitetsnivået.
    - **Oppdater lagerstatus** – Når du setter dette alternativet til *Ja* og **Lagerstatus** er aktivert for lagringsdimensjonsgruppen for varen som blir testet, oppdateres statusen automatisk med statusen som er valgt i feltet **Mislykket kvalitetsordrestatus** eller **Bestått kvalitetsordrestatus**.
    - **Mislykket kvalitetsordrestatus** – Velg lagerstatusen som skal tilordnes til varen når en kvalitetsordre som inkluderte denne testgruppen, mislykkes fordi den ikke oppfyller det akseptable kvalitetsnivået.
    - **Bestått kvalitetsordrestatus** – Velg lagerstatusen som skal tilordnes til varen når en kvalitetsordre som inkluderte denne testgruppen, lykkes fordi den oppfyller det akseptable kvalitetsnivået.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Legge til en kvalitativ test i en testgruppe

Følg denne fremgangsmåten for å legge til en kvalitativ test i en testgruppe.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testgrupper**.
1. I kategorien **Oversikt** i den øvre delen av siden velger du testgruppen du vil legge til en test i.
1. I den nedre delen av siden, i kategorien **Oversikt**, velger du **Legg til** på verktøylinjen for å legge til en ny rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Sekvensnummer** – Angi et heltall for å angi rekkefølgen testene skal utføres i. Tester som har mindre sekvensnumre, kjøres før tester som har større serienumre.

        > [!NOTE]
        > Vi anbefaler at du lar det være en tidsforskjell mellom sekvensnumrene. Du kan for eksempel sette **Sekvensnummer**-feltet til *10* for den første testen, og deretter øke verdien med 10 for hver tilleggstest. På denne måten kan du legge til nye tester senere uten å måtte slette og opprette linjene på nytt for å plassere dem i ønsket rekkefølge.

    - **Test** – Velg testen du vil utføre. For en kvalitativ test velger du en test der **Type**-feltet er satt til *Alternativ*.
    - **Gjelder** – Velg den første datoen da testen er gyldig. Hvis du lar du dette feltet stå tomt, er det ingen grense.
    - **Utløp** – Velg den siste datoen da testen er gyldig. Hvis du lar dette feltet stå tomt eller setter det til *Aldri*, finnes det ingen grense.
    - **Fastsettelse av testverdi**– Velg hvordan et godtatt kvalitetstegn skal fastsettes når flere resultater registreres for den samme testen. For en kvalitativ test kan bare *Manuell* velges. Hvis du velger en av de andre verdiene (*Gjennomsnitt*, *Minimum* eller *Maksimum*), får du en feilmelding når du lagrer testgruppen.
    - **Attributt** – Hvis du vil registrere testresultater på et partiattributt, velger du attributtet her og merker av for **Oppdater lagerpartiattributt**.
    - **Oppdater lagerpartiattributt** – Merk av her hvis du vil registrere testresultater for partiattributtet som er valgt i **Attributt**-feltet.

1. I den nedre delen av siden velger du kategorien **Generelt**. Noen av innstillingene for testen som er valgt i kategorien **Oversikt**, gjentas her. I tillegg kan du angi følgende felt for testen:

    - **Analysesertifikatrapport** – Sett dette alternativet til *Ja* for å angi at testresultatene skal skrives ut på analysesertifikatet. Denne rapporten kan genereres fra kvalitetsordren.
    - **Handling ved feil** – Velg enten *Godta* eller *Mislykket* for å angi om testen skal bestå eller mislykkes hvis det akseptable kvalitetsnivået ikke er oppfylt.
    - **Akseptabelt kvalitetsnivå** – Angi den totale prosentsatsen av testresultater som må bestås for at testen skal vurderes som bestått.

1. I den nedre delen av siden i kategorien **Test** angir du følgende felt:

    - **Variabel** – Velg testvariabelen som de kvalitative testresultatene skal registreres for.
    - **Standardresultat** – Velg standardresultatet som skal registreres for testresultatene.
    - **Testinstrument** – Velg enheten som skal brukes for testen. Hvis et testinstrument er definert, angis det automatisk for testen i testgruppen.

1. Lukk siden.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Legge til en kvantitativ test i en testgruppe

Følg denne fremgangsmåten for å legge til en kvantitativ test i en testgruppe.

1. Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Testgrupper**.
1. I kategorien **Oversikt** i den øvre delen av siden velger du testgruppen du vil legge til en test i.
1. I den nedre delen av siden, i kategorien **Oversikt**, velger du **Legg til** på verktøylinjen for å legge til en ny rad i rutenettet. Angi deretter følgende felter for den nye raden:

    - **Sekvensnummer** – Angi et heltall for å angi rekkefølgen testene skal utføres i. Tester som har mindre sekvensnumre, kjøres før tester som har større serienumre.

        > [!NOTE]
        > Vi anbefaler at du lar det være en tidsforskjell mellom sekvensnumrene. Du kan for eksempel sette **Sekvensnummer**-feltet til *10* for den første testen, og deretter øke verdien med 10 for hver tilleggstest. På denne måten kan du legge til nye tester senere uten å måtte slette og opprette linjene på nytt for å plassere dem i ønsket rekkefølge.

    - **Test** – Velg testen du vil utføre. For en kvantitativ test velger du en test der **Type**-feltet er satt til *Brøk* eller *Heltall*.
    - **Gjelder** – Velg den første datoen da testen er gyldig. Hvis du lar du dette feltet stå tomt, er det ingen grense.
    - **Utløp** – Velg den siste datoen da testen er gyldig. Hvis du lar dette feltet stå tomt eller setter det til *Aldri*, finnes det ingen grense.
    - **Fastsettelse av testverdi**– Velg hvordan et godtatt kvalitetstegn skal fastsettes når flere resultater registreres for den samme testen. De tilgjengelige alternativene er *Gjennomsnitt*, *Minimum*, *Maksimum* og *Manuell*.
    - **Attributt** – Hvis du vil registrere testresultater på et partiattributt, velger du attributtet her og merker av for **Oppdater lagerpartiattributt**.
    - **Oppdater lagerpartiattributt** – Merk av her hvis du vil registrere testresultater for partiattributtet som er valgt i **Attributt**-feltet.

1. I den nedre delen av siden velger du kategorien **Generelt**. Noen av innstillingene for testen som er valgt i kategorien **Oversikt**, gjentas her. I tillegg kan du angi følgende felt for testen:

    - **Analysesertifikatrapport** – Sett dette alternativet til *Ja* for å angi at testresultatene skal skrives ut på analysesertifikatet. Denne rapporten kan genereres fra kvalitetsordren.
    - **Handling ved feil** – Velg enten *Godta* eller *Mislykket* for å angi om testen skal bestå eller mislykkes hvis det akseptable kvalitetsnivået ikke er oppfylt.
    - **Akseptabelt kvalitetsnivå** – Angi den totale prosentsatsen av testresultater som må bestås for at testen skal vurderes som bestått.

1. I den nedre delen av siden i kategorien **Test** angir du følgende felt:

    - **Standard** – Angi beløpet (heltall eller brøk) som er forventet for testresultatene. Verdien du angir, blir angitt som standard i testresultatene. I tillegg blir den automatisk angitt som en standardverdi i feltene **Min** og **Maks**.
    - **Min** – Angi den minste tillatte verdien for testresultatene. Verdien du angir, må være mindre enn beløpet som er angitt i **Standard**-feltet. Når du oppdaterer **Min**-feltet, oppdateres feltet **Min. avviksprosent** automatisk. Tilsvarende, når du oppdaterer **Min. avviksprosent**-feltet, oppdateres **Min**-feltet automatisk.
    - **Maks** – Angi den største tillatte verdien for testresultatene. Verdien du angir, må være større enn beløpet som er angitt i **Standard**-feltet. Når du oppdaterer **Maks**-feltet, oppdateres feltet **Maks. avviksprosent** automatisk. Tilsvarende, når du oppdaterer **Maks. avviksprosent**-feltet, oppdateres **Maks**-feltet automatisk.
    - **Testinstrument** – Velg enheten som skal brukes for testen. Hvis et testinstrument er definert, angis det automatisk for testen i testgruppen.

1. Lukk siden.

## <a name="additional-resources"></a>Tilleggsressurser

- [Testinstrumenter for kvalitetsstyring](quality-management-processes.md)
- [Kvalitetsstyringstester](quality-management-processes.md)
- [Testvariabler for kvalitetsstyring](quality-management-processes.md)
- [Kvalitetstilknytninger](quality-management-processes.md)
- [Partiattributter](../production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
