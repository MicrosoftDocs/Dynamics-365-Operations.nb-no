---
title: Opprette arbeidssteder
description: Dette emnet forklarer hvordan du oppretter et arbeidssted i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8ba905224fbbcc5db95820e2b228a0d478e6146
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205413"
---
# <a name="create-functional-locations"></a>Opprette arbeidssteder

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du oppretter et arbeidssted i Aktivastyring.

Når du oppretter en arbeidsstedsstruktur, må du være oppmerksom på at når du har opprettet et arbeidssted, du kan ikke flytte det fra den opprinnelige plasseringen. Dette betyr at du bør vurdere strukturen til arbeidsstedene nøye før du begynner å opprette dem i Aktivastyring. Hvis du angrer på et arbeidssted, kan du slette det, forutsatt at det ennå ikke er tatt i bruk.

For å kunne arbeide med arbeidssteder starter du ved å opprette to "kategorier" av arbeidssteder:

- Opprett *ett* standard arbeidssted uten underordnede steder. Dette arbeidsstedet brukes bare som standardsted for aktiva når du oppretter nye aktiva.  
- Opprett arbeidsstedsstrukturene som kreves for å administrere vedlikeholdsjobber i firmaet.

## <a name="create-a-default-functional-location"></a>Opprette et standard arbeidssted

Når du bruker arbeidssteder, begynner du med å opprette ett standardsted som skal brukes når du oppretter nye aktiva. Dette arbeidsstedet er det du velger i **Aktivastyring** > **Oppsett** > **Parametere for Aktivastyring** > **Aktiva**-koblingen > **Standard arbeidssted**-feltet. Standard arbeidssted kan brukes når du oppretter nye aktiva, og du ennå ikke har definert en arbeidsstedsstruktur for disse aktivaene.

1. Velg **Aktivastyring** > **Felles** > **Arbeidssteder** > **Alle arbeidssteder**.  
2. I **Alle arbeidssteder** velger du **Ny**.
3. Sett inn en ID i feltet **Arbeidssted**, for eksempel "0000" eller "Standard", for å angi at dette er et spesielt arbeidssted.
4. Sett inn et navn på standardarbeidsstedet i **Navn**-feltet.
5. *Ikke* velg et overordnet sted i **Overordnet**-feltet – la dette feltet stå tomt.
6. I feltet **Arbeidsstedstype** velger du arbeidsstedstypen som skal brukes for standard arbeidssted. Se [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md) hvis du vil ha mer informasjon om hvordan du definerer arbeidsstedstyper.
7. Velg **OK**. Du bør ikke legge til flere data på dette arbeidsstedet, siden det bare brukes som et midlertidig sted for nye aktiva til du installerer aktivaene på arbeidsstedene som brukes av firmaet.

## <a name="create-functional-locations"></a>Opprette arbeidssteder

Følgende fremgangsmåte beskriver hvordan du oppretter arbeidsstedene som kreves for vedlikeholdsbehandling i firmaet.

1. Velg **Aktivastyring** > **Felles** > **Arbeidssteder** > **Alle arbeidssteder**. Du kan opprette et arbeidssted fra rutenettvisning eller detaljvisning.
2. Velg **Ny**-knappen.
3. Sett inn en ID i feltet **Arbeidssted**.
4. Sett inn et navn på arbeidsstedet i **Navn**-feltet.
5. Hvis arbeidsstedet er en underordnet plassering i en struktur, velger du den overordnede plasseringen i feltet **Overordnet**.
6. Velg en type i feltet **Arbeidsstedstype**.
7. Velg **OK**.
8. Velg arbeidsstedet, og klikk på **Rediger**-knappen for å legge til mer informasjon.

>[!NOTE]
>Avhengig av oppsettet av livsløpstilstander for arbeidssteder kan det hende du må opprette alle underordnede steder for et arbeidssted og deretter endre livsløpstilstanden for arbeidsstedet før du kan begynne å installere aktiva. Se [Installere aktiva på arbeidssteder](../functional-locations/install-objects-on-functional-locations.md) hvis du vil ha mer informasjon om installasjon av aktiva. Se [Livsløpstilstander for arbeidssteder](../setup-for-functional-locations/functional-location-stages.md) for å finne ut mer om oppsettet av livsløpstilstander for arbeidssteder.

I detaljvisning vil du se hurtigfaner der du kan legge til og redigere informasjon om arbeidsstedet.

## <a name="general-information"></a>Generell informasjon

Denne delen gir en oversikt over overordnet og underordnet informasjon i arbeidsstedsstrukturen. I **Detaljer**-delen kan du se antall aktivaattributter, vedlikeholdsplaner og aktiva som er knyttet til arbeidsstedet. I **Beholdning**-delen kan du velge området og lageret som arbeidsstedet er knyttet til. Område og lager brukes i forbindelse med vareprognoser for arbeidsordrer. Når du oppretter en vareprognose, brukes område- og lagerinformasjon fra arbeidsstedet til aktivumet automatisk. I delen **Livsløpstilstand** vises informasjon om den livsløpstilstanden for arbeidsstedet.

## <a name="installed-assets"></a>Installerte aktiva

Se [Installere aktiva på arbeidssteder](../functional-locations/install-objects-on-functional-locations.md) hvis du vil ha mer informasjon om installasjon av aktiva. Du kan bruke **Vis**-knappen på denne hurtigfanen til å vise flere felt i hurtigfanen. Feltene **Gyldig fra** og **Underaktivum** kan vises i rutenettet.

## <a name="asset-attribute-requirements"></a>Attributtkrav for aktiva

På denne hurtigfanen kan du legge til spesifikke attributtkrav for aktivaene du installerer på arbeidsstedet. Disse kravene er kun til informasjonsformål. De hindrer deg ikke fra å installere aktiva med andre attributtkrav. Velg **Legg til linje**, og velg attributtypen. Deretter setter du inn den relevante **verdien**, velger en terskel i feltet **Terskelvilkår** og lagrer posten.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Vedlikeholdsplaner og vedlikeholdsrunder

Her kan du legge til vedlikeholdsplaner og vedlikeholdsrunder på arbeidsstedet, inkludert en startdato. Aktivaene som er installert på et arbeidssted, kan ha andre vedlikeholdsplaner konfigurert. Alle vedlikeholdsplaner og vedlikeholdsrunder kan brukes til å planlegge aktivakalenderoppføringer for et arbeidssted og aktivaene som er installert der.

>[!NOTE]
>Hvis du oppdaterer oppsettet for aktivatyper, aktivamerker og aktivamodeller i vedlikeholdsplaner i **Alle arbeidssteder**-detaljvisningen > hurtigfanen **Vedlikeholdsplaner** etter at du har opprettet vedlikeholdsplaner, blir eksisterende oppføringer i vedlikeholdsplanen relatert til arbeidsstedet slettet automatisk. Hvis du vil opprette nye tidsplanoppføringer, som samsvarer med det oppdaterte vedlikeholdsplanoppsettet på arbeidsstedet, må du kjøre en ny tidsplan for vedlikeholdsplanen for dette arbeidsstedet. 

## <a name="address"></a>Adresse

Sett inn adresssen til arbeidsstedet i hurtigfanen **Adresse**. Adresser på abeidssteder arves, noe som betyr at hvis et underordnet sted ikke har noen adresse definert, brukes adressen til det overordnede stedet.

## <a name="workers"></a>Arbeidere

I denne hurtigfanen kan du legge til arbeidere som er tilknyttet arbeidsstedet, og du kan velge et arbeidssted som det primære for arbeideren. 

## <a name="attributes"></a>Attributter

På denne hurtigfanen kan du angi verdier for arbeidsstedsattributter. Disse attributtene kan brukes til å beskrive egenskaper som er relevante for arbeidsstedet, for eksempel strukturelle egenskaper, bygningstype, områdebeskrivelser eller plassering over eller under bakken.

Velg **Legg til linje**, og velg attributtypen. Deretter setter du inn **verdien** som er knyttet til attributtypen, og lagrer oppføringen.

## <a name="financial-dimensions"></a>Finansdimensjoner

Du kan velge en finansdimensjon for arbeidsstedet. [Arbeidsstedstyper](../setup-for-functional-locations/functional-location-types.md) kan defineres til å tillate automatisk oppdatering av finansdimensjoner fra et arbeidssted. Dette betyr at aktiva som er installert på en finansdimensjon, automatisk får finansdimensjonene for arbeidsstedet. Dette er nyttig hvis du vil ha forskjellige kostsentre, avhengig av steder.

Når data angående **Område**, **Lager**, **Adresse** og **Finansdimensjoner** oppdateres på et overordnet arbeidssted, kan de relaterte underordnede arbeidsstedene oppdateres tilsvarende hvis du gjør dette valget under oppdateringen. Det åpnes en dialogboks som gir deg oppdateringsalternativene.

## <a name="copy-a-functional-location-structure"></a>Kopiere en arbeidsstedsstruktur

Hvis firmaet har flere arbeidssteder med lignende stedsstrukturer, kan du bruke kopieringsfunksjonen i Aktivastyring til raskt å opprette flere lignende stedshierarkier. Når du kopierer et bestemt arbeidssted eller en hel struktur, har det nye stedet eller strukturen samme navn som den du kopierte. Nårkopierings prosedyren er ferdig, kan du enkelt endre navnet eller andre innstillinger på det nye arbeidsstedet, forutsatt at livsløpstilstanden som er valgt for det nye arbeidsstedet, tillater det.

1. I **Alle arbeidssteder** velger du arbeidsstedet du vil kopiere. Du velger for eksempel en topplassering (overordnet) hvis du vil kopiere hele arbeidsstedsstrukturen, inkludert underordnede steder.
2. Velg knappen **Kopier arbeidsstedsstruktur**. Plasseringen du valgte på listesiden, vises i **Kopier fra**-feltet.
3. Sett inn navnet på det nye stedet i feltet **Nytt arbeidssted**.
4. I feltet **Overordnet det skal limes inn under** bør du bare sette inn en overordnet ID hvis stedet du oppretter, skal være en del av en eksisterende arbeidsstedsstruktur.
5. Klikk **OK**. Den nye arbeidsstedsstrukturen vises i **Alle arbeidssteder**.

>[!NOTE]
>Når du kopierer en arbeidsstedsstruktur, er livsløpstilstander for arbeidssteder i den nye strukturen satt til "første tilstand" som du har opprettet for arbeidssteder. Om du kan gi nytt navn til eller slette et arbeidssted ved hjelp av knappene **Gi nytt navn** og **Slett** i **Alle arbeidssteder**, avhenger av den gjeldende livsløpstilstanden til arbeidsstedet.

## <a name="delete-a-functional-location"></a>Slette et arbeidssted

Et arbeidssted med beslektede understeder kan slettes hvis ingen aktiva er installert på noen av arbeidsstedene du prøver å slette, og hvis den gjeldende livsløpstilstanden for arbeidsstedet tillater det.

1. I **Alle arbeidssteder** velger du arbeidsstedet du vil slette.
2. Hvis det er nødvendig, oppdaterer du arbeidsstedet til en livsløpstilstand som tillater sletting av et arbeidssted.
3. Velg **Slett**.

>[!NOTE]
>Hvis du ikke kan slette et arbeidssted, kan du i stedet håndtere slettingen ved å definere en livsløpstilstand for arbeidsstedet til dette formålet. Du kan for eksempel definere en "kassert" eller "slettet" fase, som ikke skal være en aktiv fase, i skjemaet **Livsløpstilstander for arbeidssteder**.
