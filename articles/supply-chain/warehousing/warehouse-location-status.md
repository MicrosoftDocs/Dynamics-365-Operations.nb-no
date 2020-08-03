---
title: Status for lagerlokasjon
description: Dette emnet gir en oversikt over Status for lagerlokasjon-funksjonen.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
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
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 128083b22bb14d9b445863a0ba1217f723727ee4
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597512"
---
# <a name="warehouse-location-status"></a>Status for lagerlokasjon

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management inkluderer flere lokasjonsfelt som gir deg fleksibilitet når du arbeider med og vedlikeholder lokasjoner. Du kan inkludere lokasjonsstatuser i lokasjonsdirektivspørringen for å gi bedre kontroll over lagerflyten.

De fire feltene nedenfor på **Lokasjoner**-siden sporer informasjon om gjeldende status for en lokasjon. Med disse feltene kan lagerledere få en oversikt over statusen for lagerlokasjon. De tillater også avansert rapportering og filtrering.

- **Varenummer** – varen som for øyeblikket er på lokasjonen. Hvis lokasjonen inneholder flere varer, er dette feltet tomt.
- **Dato og klokkeslett for siste aktivitet** – tidsstempelet for den siste lagertransaksjonen som ble utført mot lokasjonen.
- **Aldersdato** – datoen da beholdningen i lokasjonen ble hentet inn i lageret. Denne verdien beregnes basert på aldersdatoen til nummerskiltet. Det er nøyaktig for lokasjoner som er nummerskilt – sporet, men det vil kanskje ikke være nøyaktig for lokasjoner som ikke har nummerskilt – sporet.
- **Lokasjonsstatus** – statusen til lokasjonen. Det er fire mulige verdier:

    - **Ikke bestemt** – lokasjonsprofilen kan ikke spore status. Gjeldende status er derfor ukjent.
    - **Tom** – det er for øyeblikket ingen beholdning på lokasjonen.
    - **Plukk** – utgående transaksjoner er utført mot lokasjonen siden den sist ble tømt.
    - **Lager** – bare inngående transaksjoner er utført mot lokasjonen siden lokasjonen sist ble tømt.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Aktiver funksjonen Status for lagerlokasjon

Før du kan bruke *Status for lagerlokasjon*-funksjonen, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Status for lagerlokasjon*

## <a name="set-up-warehouse-location-status"></a>Definere status for lagerlokasjon

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Klargjøre eksempeldataene som kreves for eksempelscenarioet

Før du begynner å jobbe gjennom scenariet, må du aktivere eksempeldata og konfigurere funksjonen som beskrevet i denne delen. Hvis du vil fullføre eksempelscenarioet, må du bruke enten lagerappen eller den nettleserbaserte emulatoren. Trinnene som oppgis her, bruker lagerappen. Fremgangsmåten for den nettleserbaserte emulatoren ligner.

#### <a name="use-the-usmf-legal-entity"></a>Bruk den juridiske enheten USMF

For å arbeide deg gjennom dette eksempelscenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

#### <a name="set-up-location-profiles"></a>Konfigurer lokasjonsprofiler

Eksempelscenarioet krever at du forbereder to lokasjonsprofiler.

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **Rediger** for å legge siden inn i redigeringsmodus.
1. Velg **BULK-06**-profilen.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Aktiver vare på lokasjon:** Sett dette alternativet til _Ja_.
    - **Aktiver dato og klokkeslett for lokasjonsaktivitet:** Sett dette alternativet til _Ja_.
    - **Aktiver lokasjonsstatus:** Sett dette alternativet til _Ja_.

    Disse alternativene kontrollerer om referansefeltene på lokasjonen er aktive.

1. Gjenta trinn 3 til 4 for **PICK-06**-profilen.

### <a name="scenario"></a>Scenario

1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny**.
1. I **Opprett bestilling**-dialogboksen, på **Leverandør**-hurtigfanen, i **Leverandørkonto**-feltet, velger du *104*.
1. På hurtigfanen **Generelt**, i **Lager**-feltet, velger du *61*.
1. Velg **OK**.
1. Den nye bestillingen (PO) åpnes. Det inneholder en tom linje i **Bestillingslinjer**-rutenettet. På denne linjen angir du følgende verdier:

    - **Varenummer:** _A0002_
    - **Antall:** _5_

1. I handlingsruten på **Kjøp**-fanen, i **Handlinger**-gruppen, velger du **Bekreft** for å bekrefte bestillingen.
1. På den mobile enheten går du til **Inngående \> Kjøpsmottak**.
1. Velg **PONUM**-feltet, angi bestillingsnummeret og bekreft.
1. Velg **ITEM**-feltet, angi *A0002* som varenummer og bekreft.
1. På **QTY**-siden angir du *5* som antallet og bekrefter.

    Du kan angi antallet på en av følgende måter:

    - Velg plusstegnet (**+**) eller minustegn (**–**) for å legge til eller trekke fra en numerisk verdi.
    - Velg det tomme feltet mellom plusstegnet (**+**) og minustegnet (**–**) for å åpne talltastaturet.

1. Bekreft at du har valgt varenummer *A0002* og et antall på *5*. Meldingen Arbeid fullført vises nederst på siden.
1. Velg menyknappen (noen ganger kalt hamburger eller hamburgerknappen) øverst til høyre, og velg deretter **Avbryt** for å avslutte **Kjøpsmottak** og gå tilbake til **Inngående**-menyen.
1. På bestillingssiden velger du **Arbeidsdetaljer** over **Bestillingslinjer**-rutenettet.
1. I **Generelt**-fanen legger du merke til verdiene **Arbeids-ID** og **Målnummerskilt-ID** som ble opprettet.
1. I **Linjer**-inndelinger legger du merke til **Lokasjoner**-verdiene for *Plukk*- og *Plasser*-arbeidstypene.
1. På den mobile enheten går du til **Inngående \> Kjøpsplassering**.
1. Velg **ID**-feltet, angi arbeids-ID og bekreft.
1. Bekreft én gang til for å fullføre *Plukk*-oppføringen.
1. Velg Meny-knappen i øvre høyre hjørne på siden, og velg deretter **Ferdig** for å fullføre *Plukk*-arbeidet.
1. Skriv ned Plasseringslokasjon, og bekreft. Meldingen Arbeid fullført vises nederst på siden.
1. Velg Meny-knappen i øvre høyre hjørne, og velg deretter **Avbryt** for å avslutte **Kjøpsplassering** og gå tilbake til **Inngående**-menyen.
1. Velg **Tilbake** for å gå tilbake til hovedmenyen.
1. Gå til **Lagerstyring** \> Oppsett \> Lager \> Lokasjoner i Dynamics 365 Supply Chain Management.
1. Filtrer på **Lokasjon**, og angi plasseringslokasjon fra bestillingsarbeidet. Du skal se følgende resultater:

    - **Lokasjonsstatus**-kolonnen viser verdien *Lager*, fordi den siste transaksjonen mot denne lokasjonen var en plassering.
    - **Varenummer**-kolonnen viser verdien *A0002*, fordi varen ble mottatt og lagt til lokasjonen.
    - **Dato og klokkeslett for siste aktivitet**-kolonnen viser tidsstempelet for datoen og klokkeslettet da arbeidet ble fullført på lokasjonen.

1. På den mobile enheten går du til **Kvalitet \> Bevegelse**.
1. Velg **LOC/LP**-feltet, og angi lokasjonen du noterte i de forrige trinnene.
1. Bekreft informasjonen som vises. Noter deg nummeret til nummerskiltet som genereres.
1. På **Til informasjon**-skjermen velger du **LOC/LP**-feltet, og angi *06A07R2S1B* som stedet du vil flytte varen til.
1. På **Til informasjon**-skjermen bekrefter du **LP**-verdien (målnummerskilt-ID-en), som genereres automatisk. Meldingen Arbeid fullført vises nederst på siden.
1. Velg Meny-knappen i øvre høyre hjørne, og velg deretter **Avbryt** for å avslutte **Bevegelse** og gå tilbake til **Kvalitetsstyring**-menyen.
1. Velg **Tilbake** for å gå tilbake til hovedmenyen.
1. Gå til **Lagerstyring** \> Oppsett \> Lager \> Lokasjoner i Dynamics 365 Supply Chain Management.
1. Oppdater **Lokasjoner**-siden, og vis den opprinnelige plasseringslokasjonen på nytt. Legg merke til at **Lokasjonsstatus**-feltet nå er *Tomt*, og at **Varenummer**-kolonnen er tom.
1. Vis posten for lokasjon *06A07R2S1B*, og legg merke til at **Status**-verdien er endret til *Lager*, og feltene **Varenummer** og **Dato og klokkeslett for siste aktivitet** oppdatert.
1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny**.
1. I **Opprett salgsordre**-dialogboksen, i **Kundekonto**-feltet, velger du *US-002*.
1. I **Lager**-feltet velger du *61*.
1. Velg **OK**.
1. Den nye salgsordren åpnes. Det inneholder en tom linje i **Salgsordrelinjer**-rutenettet. På denne linjen angir du følgende verdier:

    - **Varenummer:** _A0002_
    - **Antall:** _1_

1. På **Salgsordrelinjer**-fanen, på **Beholdning**-menyen, velger du **Reservasjon**.
1. På **Reservasjon**-siden velger du **Reserver parti** for å reservere ordrelinjen. Velg **Lukk**-knappen (**X**) øverst til høyre for å lukke siden.
1. Velg **Frigi til lager** i gruppen **Handlinger** i kategorien **Lager** i handlingsruten.
1. I **Salgsordrelinjer**-delen, på **Lager**-menyen, velger du **Arbeidsdetaljer**.
1. Kopier **Arbeids-ID**-verdien som ble opprettet.
1. På den mobilen enheten går du til **Utgående \> Salgsplukking**.
1. Velg **ID**-feltet, angi arbeids-ID som du kopierte tidligere, og bekreft.
1. På **Salgsordrer: Plukk**-siden foreslår **LOC**-feltet plukklokasjonen som plasseringslokasjon som ble opprettet tidligere. Noter lokasjonen.
1. Velg **LOC**-feltet, angi lokasjonen og bekreft.
1. Velg **LP**-feltet, angi skiltnummeret du noterte under bevegelsesaktiviteten, og bekreft.
1. Velg **Vare**-feltet, angi *A0002* som varenummer og bekreft.
1. På **QTY**-siden angir du *1* som antallet og bekrefter.

    Du kan angi antallet på en av følgende måter:

    - Velg plusstegnet (**+**) eller minustegn (**–**) for å legge til eller trekke fra en numerisk verdi.
    - Velg det tomme feltet mellom plusstegnet (**+**) og minustegnet (**–**) for å åpne talltastaturet.

1. Velg **TARGET LP**-feltet, angi en brukerdefinert nummerskilt-ID og bekreft.
1. Bekreft én gang til for å fullføre plukkarbeidet. Meldingen Arbeid fullført vises nederst på siden.
1. Velg Meny-knappen i øvre høyre hjørne, og velg deretter **Avbryt** for å fullføre plukkaktiviteten og gå tilbake til **Utgående**-menyen.
1. Gå til **Lagerstyring** \> Oppsett \> Lager \> Lokasjoner i Dynamics 365 Supply Chain Management.
1. Filtrer på **Lokasjon**, og angi plukklokasjon fra salgsordrearbeidet.
1. Legg merke til at **Lokasjonsstatus**-feltet for lokasjonen der salgsordrearbeidet ble plukket fra, nå er satt til *Plukking* og **Dato og klokkeslett for siste aktivitet** er oppdatert.

> [!NOTE]
> Lokasjonsfeltene oppdateres bare etter lagertransaksjoner. Hvis du flytter beholdningen ved hjelp av en journal eller andre ikke-WHS-prosesser, oppdateres ikke feltene.
