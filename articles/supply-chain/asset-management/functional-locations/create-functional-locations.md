---
title: Opprette funksjonslokasjoner
description: Denne artikkelen forklarer hvordan du oppretter en funksjonslokasjon i Aktivastyring.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7c36fe230db38bfdbfd70fec7bdfd0a313d5a15
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015848"
---
# <a name="create-functional-locations"></a>Opprette funksjonslokasjoner

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen forklarer hvordan du oppretter en funksjonslokasjon i Aktivastyring.

Når du oppretter en funksjonslokasjonsstruktur, må du være oppmerksom på at når du har opprettet en funksjonslokasjon, du kan ikke flytte det fra den opprinnelige plasseringen. Dette betyr at du bør vurdere strukturen til funksjonslokasjonene nøye før du begynner å opprette dem i Aktivastyring. Hvis du angrer på en funksjonslokasjon, kan du slette det, forutsatt at det ennå ikke er tatt i bruk.

For å kunne arbeide med funksjonslokasjoner starter du ved å opprette to "kategorier" av funksjonslokasjoner:

- Opprett *én* standard funksjonslokasjon uten underordnede lokasjoner. Denne funksjonslokasjonen brukes bare som standardsted for aktiva når du oppretter nye aktiva.  
- Opprett funksjonslokasjonsstrukturene som kreves for å administrere vedlikeholdsjobber i firmaet.

## <a name="create-a-default-functional-location"></a>Opprette en standard funksjonslokasjon

Når du bruker funksjonslokasjoner, begynner du med å opprette ett standardsted som skal brukes når du oppretter nye aktiva. Denne funksjonslokasjonen er det du velger i **Aktivastyring** > **Oppsett** > **Parametere for Aktivastyring** > **Aktiva**-koblingen > **Standard funksjonslokasjon**-feltet. Standard funksjonslokasjon kan brukes når du oppretter nye aktiva, og du ennå ikke har definert en funksjonslokasjonsstruktur for disse aktivaene.

1. Velg **Aktivastyring** > **Funksjonslokasjoner** > **Alle funksjonslokasjoner**.  
2. I **Alle funksjonslokasjoner** velger du **Ny**.
3. Sett inn en ID i feltet **Funksjonslokasjon**, for eksempel "0000" eller "Standard", for å angi at dette er en spesiell funksjonslokasjon.
4. Sett inn et navn på standard funksjonslokasjon i **Navn**-feltet.
5. *Ikke* velg et overordnet sted i **Overordnet**-feltet – la dette feltet stå tomt.
6. I feltet **Funksjonslokasjonstype** velger du funksjonslokasjonstypen som skal brukes for standard funksjonslokasjon. Se [Funksjonslokasjonstyper](../setup-for-functional-locations/functional-location-types.md) hvis du vil ha mer informasjon om hvordan du definerer funksjonslokasjonstyper.
7. Velg **OK**. Du bør ikke legge til flere data på denne funksjonslokasjonen, siden det bare brukes som et midlertidig sted for nye aktiva til du installerer aktivaene på funksjonslokasjonene som brukes av firmaet.

## <a name="create-functional-locations"></a>Opprette funksjonslokasjoner

Følgende fremgangsmåte beskriver hvordan du oppretter funksjonslokasjonene som kreves for vedlikeholdsbehandling i firmaet.

1. Velg **Aktivastyring** > **Funksjonslokasjoner** > **Alle funksjonslokasjoner**. Du kan opprette en funksjonslokasjon fra rutenettvisning eller detaljvisning.
2. Velg **Ny**-knappen.
3. Sett inn en ID i feltet **Funksjonslokasjon**.
4. Sett inn et navn på funksjonslokasjonen i **Navn**-feltet.
5. Hvis funksjonslokasjonen er en underordnet plassering i en struktur, velger du den overordnede plasseringen i feltet **Overordnet**.
6. Velg en type i feltet **Funksjonslokasjonstype**.
7. Velg **OK**.
8. Velg funksjonslokasjonen, og klikk på **Rediger**-knappen for å legge til mer informasjon.

>[!NOTE]
>Avhengig av oppsettet av livssyklustilstander for funksjonslokasjoner kan det hende du må opprette alle underordnede steder for en funksjonslokasjon og deretter endre livssyklustilstanden for funksjonslokasjonen før du kan begynne å installere aktiva. Se [Installere aktiva på funksjonslokasjoner](../functional-locations/install-objects-on-functional-locations.md) hvis du vil ha mer informasjon om installasjon av aktiva. Se [Livssyklustilstander for funksjonslokasjoner](../setup-for-functional-locations/functional-location-stages.md) for å finne ut mer om oppsettet av livssyklustilstander for funksjonslokasjoner.

I detaljvisning vil du se hurtigfaner der du kan legge til og redigere informasjon om funksjonslokasjonen.

## <a name="general-information"></a>Generell informasjon

Denne delen gir en oversikt over overordnet og underordnet informasjon i funksjonslokasjonsstrukturen. I **Detaljer**-delen kan du se antall aktivaattributter, vedlikeholdsplaner og aktiva som er knyttet til funksjonslokasjonen. I **Beholdning**-delen kan du velge området og lageret som funksjonslokasjonen er knyttet til. Område og lager brukes i forbindelse med vareprognoser for arbeidsordrer. Når du oppretter en vareprognose, brukes område- og lagerinformasjon fra funksjonslokasjonen til aktivumet automatisk. I delen **Livssyklustilstand** vises informasjon om den livssyklustilstanden for funksjonslokasjonen.

## <a name="installed-assets"></a>Installerte aktiva

Se [Installere aktiva på funksjonslokasjoner](../functional-locations/install-objects-on-functional-locations.md) hvis du vil ha mer informasjon om installasjon av aktiva. Du kan bruke **Vis**-knappen på denne hurtigfanen til å vise flere felt i hurtigfanen. Feltene **Gyldig fra** og **Underaktivum** kan vises i rutenettet.

## <a name="asset-attribute-requirements"></a>Attributtkrav for aktiva

På denne hurtigfanen kan du legge til spesifikke attributtkrav for aktivaene du installerer på funksjonslokasjonen. Disse kravene er kun til informasjonsformål. De hindrer deg ikke fra å installere aktiva med andre attributtkrav. Velg **Legg til linje**, og velg attributtypen. Deretter setter du inn den relevante **verdien**, velger en terskel i feltet **Terskelvilkår** og lagrer posten.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Vedlikeholdsplaner og vedlikeholdsrunder

Her kan du legge til vedlikeholdsplaner og vedlikeholdsrunder på funksjonslokasjonen, inkludert en startdato. Aktivaene som er installert på en funksjonslokasjon, kan ha andre vedlikeholdsplaner konfigurert. Alle vedlikeholdsplaner og vedlikeholdsrunder kan brukes til å planlegge aktivakalenderoppføringer for en funksjonslokasjon og aktivaene som er installert der.

>[!NOTE]
>Hvis du oppdaterer oppsettet for aktivatyper, aktivamerker og aktivamodeller i vedlikeholdsplaner i **Alle funksjonslokasjoner**-detaljvisningen > hurtigfanen **Vedlikeholdsplaner** etter at du har opprettet vedlikeholdsplaner, blir eksisterende oppføringer i vedlikeholdsplanen relatert til funksjonslokasjonen slettet automatisk. Hvis du vil opprette nye tidsplanoppføringer, som samsvarer med det oppdaterte vedlikeholdsplanoppsettet på funksjonslokasjonen, må du kjøre en ny tidsplan for vedlikeholdsplanen for denne funksjonslokasjonen. 

## <a name="address"></a>Adresse

Sett inn adresssen til funksjonslokasjonen i hurtigfanen **Adresse**. Adresser på abeidssteder arves, noe som betyr at hvis et underordnet sted ikke har noen adresse definert, brukes adressen til det overordnede stedet.

## <a name="workers"></a>Arbeidere

I denne hurtigfanen kan du legge til arbeidere som er tilknyttet funksjonslokasjonen, og du kan velge en funksjonslokasjon som det primære for arbeideren. 

## <a name="attributes"></a>Attributter

På denne hurtigfanen kan du angi verdier for funksjonslokasjonsattributter. Disse attributtene kan brukes til å beskrive egenskaper som er relevante for funksjonslokasjonen, for eksempel strukturelle egenskaper, bygningstype, områdebeskrivelser eller plassering over eller under bakken.

Velg **Legg til linje**, og velg attributtypen. Deretter setter du inn **verdien** som er knyttet til attributtypen, og lagrer oppføringen.

## <a name="financial-dimensions"></a>Finansdimensjoner

Du kan velge en finansdimensjon for funksjonslokasjonen. [Funksjonslokasjonstyper](../setup-for-functional-locations/functional-location-types.md) kan defineres til å tillate automatisk oppdatering av finansdimensjoner fra en funksjonslokasjon. Dette betyr at aktiva som er installert på en finansdimensjon, automatisk får finansdimensjonene for funksjonslokasjonen. Dette er nyttig hvis du vil ha forskjellige kostsentre, avhengig av steder.

Når data angående **Område**, **Lager**, **Adresse** og **Finansdimensjoner** oppdateres på en overordnet funksjonslokasjon, kan de relaterte underordnede funksjonslokasjonene oppdateres tilsvarende hvis du gjør dette valget under oppdateringen. Det åpnes en dialogboks som gir deg oppdateringsalternativene.

## <a name="copy-a-functional-location-structure"></a>Kopiere en funksjonslokasjonsstruktur

Hvis firmaet har flere funksjonslokasjoner med lignende stedsstrukturer, kan du bruke kopieringsfunksjonen i Aktivastyring til raskt å opprette flere lignende stedshierarkier. Når du kopierer en bestemt funksjonslokasjon eller en hel struktur, har det nye stedet eller strukturen samme navn som den du kopierte. Når kopieringsprosedyren er ferdig, kan du enkelt endre navnet eller andre innstillinger på den nye funksjonslokasjonen, forutsatt at livssyklustilstanden som er valgt for den nye funksjonslokasjonen, tillater det.

1. I **Alle funksjonslokasjoner** velger du funksjonslokasjonen du vil kopiere. Du velger for eksempel en topplassering (overordnet) hvis du vil kopiere hele funksjonslokasjonsstrukturen, inkludert underordnede steder.
2. Velg knappen **Kopier funksjonslokasjonsstruktur**. Plasseringen du valgte på listesiden, vises i **Kopier fra**-feltet.
3. Sett inn navnet på det nye stedet i feltet **Ny funksjonslokasjon**.
4. I feltet **Overordnet det skal limes inn under** bør du bare sette inn en overordnet ID hvis stedet du oppretter, skal være en del av en eksisterende funksjonslokasjonsstruktur.
5. Klikk på **OK**. Den nye funksjonslokasjonsstrukturen vises i **Alle funksjonslokasjoner**.

>[!NOTE]
>Når du kopierer en funksjonslokasjonsstruktur, er livssyklustilstander for funksjonslokasjoner i den nye strukturen satt til "første tilstand" som du har opprettet for funksjonslokasjoner. Om du kan gi nytt navn til eller slette en funksjonslokasjon ved hjelp av knappene **Gi nytt navn** og **Slett** i **Alle funksjonslokasjoner**, avhenger av den gjeldende livssyklustilstanden til funksjonslokasjonen.

## <a name="delete-a-functional-location"></a>Slette en funksjonslokasjon

En funksjonslokasjon med beslektede underlokasjoner kan slettes hvis ingen aktiva er installert på noen av funksjonslokasjonene du prøver å slette, og hvis den gjeldende livssyklustilstanden for funksjonslokasjonen tillater det.

1. I **Alle funksjonslokasjoner** velger du funksjonslokasjonen du vil slette.
2. Hvis det er nødvendig, oppdaterer du funksjonslokasjonen til en livssyklustilstand som tillater sletting av en funksjonslokasjon.
3. Velg **Slett**.

>[!NOTE]
>Hvis du ikke kan slette en funksjonslokasjon, kan du i stedet håndtere slettingen ved å definere en livssyklustilstand for funksjonslokasjonen til dette formålet. Du kan for eksempel definere en "kassert" eller "slettet" fase, som ikke skal være en aktiv fase, i skjemaet **Livssyklustilstander for funksjonslokasjoner**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]