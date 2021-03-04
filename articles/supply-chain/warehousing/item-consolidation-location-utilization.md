---
title: Varekonsolidering – lokasjonsutnyttelse
description: Dette emnet gir informasjon om funksjonalitet som gjør det enkelt for lagerledere å vise og filtrere volumbruk av lokasjoner på tvers av lageret. Ledere kan velge lokasjoner og opprette lagerflyttingsarbeid direkte fra siden for varekonsolidering for å konsolidere varer og dermed gjøre bedre bruk av lagerplass.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434733"
---
# <a name="item-consolidation---location-utilization"></a>Varekonsolidering – lokasjonsutnyttelse

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om funksjonalitet som gjør det enkelt for lagerledere å vise og filtrere volumbruk av lokasjoner på tvers av lageret. Ledere kan velge lokasjoner og opprette lagerflyttingsarbeid direkte fra siden for **varekonsolidering** for å konsolidere varer og dermed gjøre bedre bruk av lagerplass.

## <a name="turn-on-the-features"></a>Aktivere funksjonene

Før du kan bruke funksjonene som beskrives i dette emnet, må du aktivere dem i systemet. Administratorer kan bruke arbeidsområdet for [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for disse funksjonene og aktivere dem hvis nødvendig. Slå på begge disse funksjonene i den rekkefølgen de vises i. (Begge funksjonene gjelder for modulen for **Lagerstyring**.)

1. Status for lagerlokasjon
2. Bruk av lokasjon for varekonsolidering

## <a name="warehouse-location-status"></a>Status for lagerlokasjon

Funksjonen *Status for lagerlokasjon* legger til fire nye felt på siden **Lokasjoner** for å spore tilleggsinformasjon om gjeldende status for lokasjonen:

- **Varenummer** – varen som for øyeblikket er på lokasjonen. Hvis lokasjonen inneholder flere varer, er dette feltet tomt.
- **Dato og klokkeslett for siste aktivitet** – tidsstempelet for den siste lagertransaksjonen som ble utført mot lokasjonen.
- **Aldersdato** – datoen da beholdningen i lokasjonen ble hentet inn i lageret. Denne datoen beregnes basert på aldersdatoen til nummerskiltet. Selv om datoen er nøyaktig for nummerskiltsporede lokasjoner, er det kanskje ikke nøyaktig for lokasjoner som ikke er nummerskiltsporet.
- **Lokasjonsstatus** – statusen til lokasjonen. Fire verdier er tilgjengelige:

    - **Ikke bestemt** – lokasjonsprofilen kan ikke spore status. Gjeldende status er derfor ukjent.
    - **Tom** – Det er ikke lager på lokasjonen for øyeblikket.
    - **Plukk** – Utgående transaksjoner er utført mot lokasjonen etter at det sist ble tømt.
    - **Lager** – Bare inngående transaksjoner er utført siden lokasjonen sist ble tømt.

Med disse feltene kan lagerledere få en bedre oversikt over statusen for lagerlokasjonene. De tillater også mer avansert rapportering og filtrering.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Konfigurere varekonsolidering og lokasjonsutnyttelse

Denne delen beskriver hvordan du kan klargjøre systemet til å bruke varekonsolidering og bruk av lokasjon. Fremgangsmåtene bruker eksempelverdier fra standard demodata. Hvis du planlegger å arbeide gjennom eksempelscenarioet som er oppgitt senere i dette emnet, velger du den juridiske enheten **USMF** (som inneholder standard demodata) og oppretter hver post som beskrives i denne delen. Hvis du ikke planlegger å arbeide gjennom eksempelscenarioet, kan verdiene som angis her, vurderes som eksempler på hvilke typer oppsett du må fullføre for å bruke funksjonene.

### <a name="released-product"></a>Frigitt produkt

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. I feltet **Varenummer** velger du *M9201*, og deretter åpner du detaljsiden.
1. I handlingsruten i kategorien **Administrer lager** i gruppen **Lager** velger du **Fysiske dimensjoner**.
1. På **Fysiske dimensjoner**-siden i handlingsruten velger du **Ny**.

    Det blir lagt til en ny linje i rutenettet. **Varenummer**-feltet er forhåndsdefinert.

1. I **Enhet**-feltet velger du *ea*. De gjenværende feltene på linjen angis automatisk.
1. Velg **Lagre**, og lukk siden.

### <a name="location-profile"></a>Lokasjonsprofil

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **ETASJE-05** i listen over lokasjonsprofiler.
1. I handlingsruten velger du **Rediger**.
1. I hurtigfanen **Generelt** kontrollerer du at begge alternativene nedenfor er satt til *Ja*:

    - Aktiver vare i lokasjonen
    - Aktiver lokasjonsstatus

1. Velg **Lagre**.

    > [!IMPORTANT]
    > Hvis alternativene **Aktiver vare på lokasjon** og **Aktiver lokasjonsstatus** allerede er satt til *Ja*, går du videre til instruksjonene for å definere hurtigfanen **Dimensjoner** i trinn 10. Hvis alternativene ikke allerede er satt til *Ja*, må du kjøre en konsekvenskontroll for modulen **Lagerstyring** etter at du har angitt dem manuelt. I dette tilfellet går du videre til neste trinn.

1. Hvis du vil kjøre en konsekvenskontroll, går du til **Systemadministrasjon \> Periodiske oppgaver \> Database \> Konsekvenskontroll**.
1. Angi følgende verdier i dialogboksen **Konsekvenskontroll**:

    - **Modul:** *Lagerstyring*
    - **Kontroller/løs:** *Kontroller*
    - **Fra dato** La dette feltet stå tomt.
    - **Konsekvenskontroll av lagerlokasjonsstatus:** Merk av for dette alternativet.

1. Velg **OK**.

    > [!TIP]
    > Når konsekvenskontrollen er utført, mottar du en varsling. Åpne [handlingssenteret](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) for å vise meldingen. Velg **Meldingsdetaljer** for å vise detaljene.
    >
    > Hvis meldingen for konsekvenskontrollen viser statusen "Feil lokasjonsstatusinformasjon for lokasjonen XXXX i lageret XX", må du kjøre konsekvenskontrollen på nytt. Denne gangen setter du feltet **Kontroller/korriger** til *Rett feil*. Vis meldingene for å være sikker på at ingen feil ble funnet.

1. Du må nå fullføre konfigurasjonen av lokasjonsprofilen. Gå tilbake til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**, velg lokasjonsprofil **ETASJE-05**, og velg deretter **Rediger** i handlingsruten.
1. Angi følgende verdier i **Dimensjoner**-hurtigfanen:

    - **Volumutnyttelsesprosent:** *100*
    - **Volumetrisk metode som brukes for lagerlokasjon:** *Bruk lokasjonsvolum*
    - **Faktisk lokasjonshøyde:** *10*
    - **Faktisk lokasjonsbredde:** *10*
    - **Faktisk dybde for lokasjon:** *10*
    - **Maksimumsvekt:** *100*

1. Velg **Lagre**.

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten for å opprette et menyelement for sortering.
1. I hodet angir du følgende verdier:

    - **Menyelementnavn:** *Juster i*
    - **Tittel:** *Juster inn*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Arbeidsopprettelsesprosess:** *Justering inn*
    - **Lagerjusteringstyper:** *Juster inn*

1. Velg **Lagre**.

### <a name="mobile-device-menu"></a>Meny på mobilenheten

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Lager** i listen over menyer.
1. I handlingsruten velger du **Rediger**.
1. I **Tilgjengelige menyer og menyelementer**-listen finner og velger du **Juster inn**-menyelementet.
1. Velg høyre pil-knappen for å flytte **Juster inn** til listen **Menystruktur**. På denne måten legger du til det nye menyelementet på den valgte menyen.
1. Velg **Lagre**.

### <a name="movement-types"></a>Bevegelsestyper

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Varetilgangstyper**.
1. Velg **Ny** i handlingsruten, og angi deretter følgende verdier:

    - **Bevegelsestypekode:** *KONSOLIDER*
    - **Beskrivelse:** *Konsolider lokasjoner*
    - **Arbeidsklasse-ID:** *InvMov*

1. Velg **Lagre**.

## <a name="example-scenario"></a>Eksempelscenario

Følgende scenario bruker lagerappen på en mobilenhet for å lage en *justering inn* på to steder i lageret.

### <a name="add-inventory-to-locations"></a>Legge til lager på lokasjoner

1. Logg på mobilenheten som en bruker som er aktivert for lager *51*.
1. Gå til **Lager \> Juster inn**.

    Du skal nå angi den første lokasjonsjusteringen.

1. I **Justering inn**-oppgave velger du lokasjonen du vil utføre lagerjusteringen for. Velg **LP-001** i *LOC*-feltet.
1. Bekreft lokasjonen.
1. Opprett en nummerskilt-ID for varen som skal legges til i lokasjonen. I feltet **Nummerskilt** angir du *LP00101*.
1. Bekreft nummerskiltet.
1. Angi varen som skal legges til i nummerskiltet. Angi *M9201* i feltet **ITEM**.
1. Bekreft varen.
1. Angi antallet av varen som skal legges til. I feltet **QTY** angir du *10*.
1. Bekreft antallet.

    Du mottar en Arbeid fullført-melding. Du skal nå angi den andre lokasjonsjusteringen.

1. I **Justering inn**-oppgave velger du lokasjonen du vil utføre lagerjusteringen for. Velg **LP-002** i *LOC*-feltet.
1. Bekreft lokasjonen.
1. Opprett en nummerskilt-ID for varen som skal legges til i lokasjonen. I feltet **Nummerskilt** angir du *LP00201*.
1. Bekreft nummerskiltet.
1. Angi varen som skal legges til i nummerskiltet. Angi *M9201* i feltet **ITEM**.
1. Bekreft varen.
1. Angi antallet av varen som skal legges til. I feltet **QTY** angir du *15*.
1. Bekreft antallet.

    Du mottar en Arbeid fullført-melding.

1. Velg menyknappen (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Avbryt** for å avslutte **Justering inn**-oppgaven.

### <a name="consolidate-locations"></a>Konsolidere lokasjoner

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Varekonsolidering**.
1. I hodet velger du lageret det skal utfører konsolidering for. I **Lager**-feltet angir du *51*.

    Det vises en post for hver lokasjon der vare *M9201* ble justert. Kolonnen **Utnyttelsesprosent** viser volumbruk for hver lokasjon.

1. Hvis du vil konsolidere lageret, velger du alle lokasjonene som må konsolideres, og deretter velger du **Konsolider lager** i handlingsruten.
1. I dialogboksen **Konsolider lager** angir du lokasjonen og bevegelsestypen som skal brukes til å opprette arbeidet for lagerflytting. Angi følgende verdier:

    - **Lokasjon:** *LP-001*
    - **Bevegelsestypekode:** *KONSOLIDER*

1. Velg **OK**.
1. Du mottar en informasjonsmelding som viser bevegelsesarbeidet som ble opprettet. Noter bevegelsesarbeids-IDen.

### <a name="view-movement-work"></a>Vise bevegelsesarbeid

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Vis arbeidet som ble opprettet. Bruk IDen for bevegelsesarbeid fra lagerkonsolideringen for å filtrere eller søke i arbeidsrutenettet.

    I dette scenariet ble det brukt en eksisterende lokasjon som hadde lager, som lagerkonsolideringslokasjon. Derfor ble det bare opprettet én arbeids-ID.

    > [!NOTE]
   > Systemet oppretter én arbeids-ID for hver flytting som må fullføres. Hvis du angir en lokasjon som allerede inneholder lager, opprettes bare én arbeids-ID. Hvis du angir en ny lokasjon, opprettes det to arbeids-IDer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]