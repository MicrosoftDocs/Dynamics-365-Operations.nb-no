---
title: Kombinasjon av produktdimensjoner for lokasjon
description: Dette emnet inneholder informasjon om kombinasjon av produktdimensjoner for lokasjon. Denne lokasjonsprofilfunksjonaliteten bidrar til å forbedre lokasjonsstyringen når produktvarianter eller produkter som har dimensjoner, brukes, for eksempel i motebransjen. Den lar deg bestemme om konfigurasjoner, farger, stiler og størrelser kan blandes for en bestemt lokasjonsprofil, eller om bare én av disse dimensjonene eller en kombinasjon av dem kan legges til samme lokasjon.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 20085c51230d3ceca46c5119fecbc3cf3291ecd4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578566"
---
# <a name="location-product-dimension-mixing"></a>Kombinasjon av produktdimensjoner for lokasjon

[!include [banner](../includes/banner.md)]

kombinasjon av produktdimensjoner for lokasjon er lokasjonsprofilfunksjonalitet som bidrar til å forbedre lokasjonsstyringen når produktvarianter eller produkter som har dimensjoner, brukes, for eksempel i motebransjen. Den lar deg bestemme om konfigurasjoner, farger, stiler og størrelser kan blandes for en bestemt lokasjonsprofil, eller om bare én av disse dimensjonene eller en kombinasjon av dem kan legges til samme lokasjon.

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a>Slå på funksjonen for kombinasjon av produktdimensjoner for lokasjon

Før du kan bruke kombinasjon av produktdimensjoner for lokasjon, må funksjonen aktiveres i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Kombinasjon av produktdimensjoner for lokasjon*

## <a name="setup"></a>Installasjon

Hver lokasjon på lageret må ha en tilknyttet lokasjonsprofil som beskriver egenskapene til lokasjonen. Alle lokasjoner som bruker samme lokasjonsprofil, vil derfor kunne tillate kombinasjon av produktdimensjoner etter at den er satt opp.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>Konfigurere lokasjonsprofiler for å tillate kombinasjon av produktdimensjoner

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjonsprofiler**.
1. Velg **BULK** i listen over lokasjonsprofiler.
1. I handlingsruten velger du **Rediger**.
1. I **Generelt**-hurtigfanen setter du **Aktiver spesifikk kombinasjon av produktdimensjoner for lokasjon** til *Ja*.

    > [!NOTE]
    > Du kan bare sette dette alternativet til *Ja* hvis **Tillat blandede varer** er satt til *Nei*.

1. I **Tillat kombinasjon av produktdimensjon**-hurtigfanen setter du **Størrelse** til *Ja*. I scenariet som beskrives i dette emnet, kan du bare foreta en blanding for produkter som har ulike **Størrelse**-dimensjoner. Andre alternativer er også tilgjengelige.
1. Velg **Lagre**.

### <a name="create-a-new-product-master-and-product-variants"></a>Opprett en ny produktstandard og produktvarianter

1. Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.
1. I handlingsruten velger du **Ny** for å opprette en produktstandard.
1. Angi følgende verdier i dialogboksen **Nytt produkt**:

    - **Produkttype:** *Vare*
    - **Produktundertype:** *Produktstandard*
    - **Produktnummer:** *B0001*
    - **Produktnavn:** *B0001 Størrelse*
    - **Produktdimensjonsgruppe:** *Størrelse*
    - **Konfigurasjonsteknologi:** *Forhåndsdefinert variant*

1. Velg **OK**.
1. På **Produktdetaljer**-siden på **Generelt**-hurtigfanen angir du følgende verdier:

    - **Generer varianter automatisk:** *Ja*
    - **Størrelsesgruppe:** *CASUALDHIR*

1. Hvis du vil vise de forhåndsdefinerte variantene, velger du **Produktvarianter** i handlingsruten.

    **Produktvarianter**-siden vises og viser en liste over varianter fra konfigurasjonen av størrelsesgruppen.

### <a name="release-products-to-the-usmf-company"></a>Frigi produkter til USMF-firmaet

1. I handlingsruten velger du **Frigi produkter**.
1. På **Velg produkter som skal frigis**-siden bekrefter du at produktnummeret *B0001* er i listen, og deretter velger du **Neste**.
1. Velg **Neste** for å bekrefte produktvariantene som skal frigis.
1. Velg *USMF* på siden **Velg firmaer du vil frigi til**, og velg deretter **Neste** for å bekrefte valget.
1. Velg **Fullfør** på **Bekreft merking**-siden for å fullføre frigivelsen.

    Du får en melding om at operasjonen er fullført.

### <a name="update-a-released-product-in-the-usmf-company"></a>Oppdatere et frigitt produkt i USMF firmaet

1. Kontroller at du er logget på **USMF**-firmaet.
1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter** for å fullføre oppretting av frigitt produkt.
1. Finn og velg varenummer *B0001* for å åpne **Detaljer om frigitt produkt**-siden.
1. I handlingsruten velger du **Rediger**.
1. I **Generelt**-hurtigfanen kontrollerer du at **Varemodellgruppe** er satt til *FIFO*.
1. I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Dimensjonsgrupper**.
1. Angi følgende verdier:

    - **Lagringsdimensjonsgruppe:** *Bølge*
    - **Sporingsdimensjonsgruppe:** *Ingen*

1. Velg **OK**.
1. I gruppen **Oppsett** i fanen **Produkt** i handlingsruten velger du **Reservasjonshierarki**.
1. Sett **Reservasjonshierarki**-feltet til *Standard*, og velg deretter **OK**.
1. I delen **Administrasjon** i hurtigfanen **Generelt** ser du at valgene er oppdatert.
1. Angi *10* i **Pris**-feltet på hurtigfanen **Kjøp**.
1. På hurtigfanen **Styr kostnader** i feltet **Varegruppe** angir du *Lyd*.
1. Angi *10* i **Pris**-feltet på hurtigfanen **Kjøp**.
1. På **LAger**-hurtigfanen angir du *ea* i **Sekvensgruppe-ID for enhet**-feltet.
1. Velg **Lagre**.

### <a name="create-a-location-directive"></a>Opprette et lokasjonsdirektiv

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I den venstre ruten i **Arbeidsordretype**-feltet velger du *Bestillinger*.
1. I listen velger du lokasjonsdirektivet som har navnet *24 PO Direct*.
1. På hurtigfanen **Lokasjonsdirektivhandlinger** velger du **Ny** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** *1*

        Den nye linjen skal være foran den tidligere eksisterende linjen. Hvis du vil gjøre endringen, bruker du knappene **Flytt opp** og **Flytt ned** på verktøylinjen, eller endrer den eksisterende linjens **Sekvensnummer**-verdi til *2*.

    - **Navn:** *Plasser i BULK-lokasjonsprofil*
    - **Bruk av fast lokasjon:** *Faste og ikke-faste lokasjoner*
    - **Tillat negativ beholdning:** *Fjern merket i denne avmerkingsboksen (= Nei)*
    - **Parti aktivert:** *Fjern merket i denne avmerkingsboksen (= Nei)*
    - **Strategi:** *Ingen*

1. Mens den nye linjen fremdeles er valgt, velger du **Rediger spørring** over rutenettet.
1. I spørringsdialogboksen, på **Område**-fanen, velger du **Legg til** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *ID for lokasjonsprofil*
    - **Vilkår:** *BULK*

1. Velg **OK**.
1. Velg **Lagre** i handlingsruten på **Lokasjonsdirektiver**-siden.

> [!NOTE]
> På **Lokasjonsdirektivhandlinger**-hurtigfanen **Strategi**-feltet, hvis du bruker lokasjonsstrategien *Konsolidering*, overstyres oppsettet på **Tillatt kombinasjon av produktdimensjon**-hurtigfanen på **Lokasjonsprofiler**, og varene vil bli plassert på samme lokasjon, selv om denne virkemåten ikke er tillatt i oppsettet.

### <a name="create-a-mobile-device-menu-item"></a>Opprette et menyelement for mobilenhet

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Velg **Ny** i handlingsruten for å opprette et menyelement som skal brukes til sortering.
1. I hodet angir du følgende verdier:

    - **Menyelementnavn:** *PO-linjemottak*
    - **Tittel:** *PO-linjemottak*
    - **Modus:** *Arbeid*
    - **Bruke eksisterende arbeid:** *Nei*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Arbeidsopprettingsprosess:** *Bestillingslinjemottak og -plassering*
    - **Generer nummerskilt:** *Ja*

1. Velg **Lagre**.

### <a name="configure-the-mobile-device-menu"></a>Konfigurere mobilenhetsmenyen

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Meny på mobilenheten**.
1. Velg **Inngående** i listen over menyer.
1. I handlingsruten velger du **Rediger**.
1. I **Tilgjengelige menyer og menyelementer**-listen finner og velger du **PO-linjemottak**-menyelementet.
1. Velg høyre pil for å flytte **PO-linjemottak**-menyelementet til **Menystruktur**-listen. På denne måten legger du til det nye menyelementet på den valgte menyen.
1. Velg **Lagre**.

## <a name="scenario"></a>Scenario

Dette demonstrasjonsscenarioet viser hvordan to ulike produktvarianter kan plasseres på samme lokasjon når lokasjonsprofilen ikke tillater blandede varer, men *Kombinasjon av produktdimensjoner for lokasjon*-funksjonen er aktivert. I dette tilfellet skal du bruke **Størrelse**-varianten som kriterium.

Før du begynner, må du kontrollere at det finnes tomme lokasjoner på lager *24* som bruker *BULK*-lokasjonsprofilen.

### <a name="create-a-purchase-order"></a>Opprette en bestilling

Du oppretter en bestilling som har tre linjer: to linjer for samme produktnummer, men forskjellige **Størrelse**-varianter, og en tredje linje for et annet produkt som ikke har noen varianter.

1. Gå til **Leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Ny** i handlingsruten.
1. I **Opprett bestilling**-dialogboksen angir du følgende verdier:

    - **Leverandørkonto:** *1001*
    - **Lager:** *24*

1. Velg **OK**.
1. Bestillingen opprettes, og det legges til en ny linje på **Bestillingslinjer**-hurtigfanen. Noter deg bestillingsnummeret.
1. På den nye linjen angir du følgende verdier:

    - **Varenummer:** *B0001*
    - **Størrelse** *L*
    - **Antall:** *2*

1. Velg **Legg til linje** over rutenettet for å legge til en ny bestillingslinje, og angi deretter følgende verdier:

    - **Varenummer:** *B0001*
    - **Størrelse** *XL*
    - **Antall:** *2*

1. Velg **Legg til linje** for å legge til en tredje bestillingslinje, og angi deretter følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *1*

1. Velg **Lagre**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>Motta bestillingslinjer i mobilappen Lagerstyring

1. Logg på mobilappen Lagerstyring som en bruker som er aktivert for lager *24*.
1. Velg **Inngående**-menyen.
1. Velg **PO-linjemottak**.
1. Velg **PONUM**-feltet, og angi bestillingsnummeret.
1. Bekreft oppføringen ved å velge Bekreft-knappen (✔) nederst på siden.
1. Angi linjenummeret fra bestillingen som mottas. Velg **LINENUM**-feltet, og bruk deretter talltastaturet til å angi *1*.
1. Bekreft oppføringen.
1. Angi antallet som skal mottas. Velg plusstegn (**+**) to ganger for å øke verdien i **Antall**-feltet til *2*.
1. Registrer oppføringen ved å velge knappen (✔) nederst på siden, og bekreft deretter oppføringen ved å velge knappen (✔) på nytt.
1. Vis informasjonen i **Bestillinger: Plasser**-siden. Denne siden viser arbeidet som er opprettet for plasseringen (Arbeid 1).

    Lokasjonen der den mottatte varen vil plasseres, nummerskiltet, varen, størrelsen og antallet i den **PO-linjemottak**-oppgaven som du nettopp har fullført, vises.

1. Bekreft plasseringsarbeidet.
1. Gjenta trinnene 4 til og med 11 for bestillingslinje 2. I trinn 8 angir du imidlertid et antall på *1*.

    Det opprettes nytt plasseringsarbeid (Arbeid 2) for samme lokasjon som Arbeid 1.

1. Gjenta trinnene 4 til og med 11 igjen for bestillingslinje 2. I trinn 8 angir du gjenværende antall på *1*.

    Det opprettes nytt plasseringsarbeid (Arbeid 3) for samme lokasjon som Arbeid 1 og Arbeid 2. Dette skjer fordi *Konsolidering*-lokasjonsdirektivstrategien brukes, og **Tillatt kombinasjon av produktdimensjon**-hurtigfanen på *Bulk*-**lokasjonsprofiler**-oppsettet gjør at **Størrelse**-varianten kan blandes på en lokasjon.

1. Gjenta trinnene 4 til og med 11 for bestillingslinje 3. I trinn 8 angir du et antall på *1* for varenummer *A0001*.

    Nytt plasseringsarbeid (Arbeid 4) opprettes for en annen lokasjon enn lokasjonen som brukes for bestillingslinje 1 og 2. Dette problemet oppstår fordi lokasjonsprofilen ikke tillater blandede produkter, men den tillater blandede dimensjoner av samme produktstandard.

1. Velg menyknappen øverst på siden (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Avbryt** for å avslutte **PO-linjemottak**.

> [!TIP]
> Du kan gjenta dette scenariet, men denne gangen angir **Størrelse** - *Nei* under **Tillat kombinasjon av produktdimensjon**-hurtigfanen på *BULK*-**lokasjonsprofiler**, slik at ingen av produktdimensjoner kan blandes. I dette tilfellet vil hver produktvariant bli satt til en ny lokasjon når du mottar bestillingen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]