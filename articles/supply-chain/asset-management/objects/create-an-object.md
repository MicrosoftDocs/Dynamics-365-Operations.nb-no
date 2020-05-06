---
title: Opprette et aktivum
description: Dette emnet beskriver hvordan du oppretter et aktivum i Aktivumbehandling.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
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
ms.openlocfilehash: f5c77f32caad5e2e79cbc0e21f72a3daa79acecb
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2020
ms.locfileid: "3274171"
---
# <a name="create-an-asset"></a>Opprette et aktivum

[!include [banner](../../includes/banner.md)]

 

Dette emnet beskriver hvordan du oppretter et aktivum i Aktivumbehandling.

1. Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva** eller **Aktive aktiva**.
2. Klikk på **Ny**-knappen.
3. I dialogboksen **Opprett aktiva** setter du inn data angående **Aktiva** (aktiva-ID) og aktivanavn. Velg dato og klokkeslett for aktivumet i feltet **Gjelder fra**. Fra denne datoen kan du installere aktivumet på et arbeidssted, i tillegg til å flytte og erstatte aktivumet i en aktivagruppe.
4. I **Aktivatype**-feltet velger du aktivatypen (obligatorisk felt). Velg om nødvendig også **Aktivaprodusent** og **Aktivamodell**. Hvis bare ett produkt er definert, velges dette produktet automatisk i feltet **Aktivaprodusent**. Valgene som er tilgjengelige i feltene **Aktivaprodusent** og **Aktivamodell**, avhenger av oppsettet i [Aktivaprodusenter og -modeller](../setup-for-objects/product-and-model.md).
5. I **Overordnet objekt**-gruppen er **Aktivum**-feltet tomt som standard. Hvis det er nødvendig, kan du velge et overordnet objekt, og deretter fylles alle feltene i gruppen **Overordnet objekt** ut.
    >[!NOTE]  
    >Når du velger et overordnet objekt, er to eller tre kategorier tilgjengelige: kategorien **Mine aktiva** inneholder aktiva som er knyttet til arbeidsstedene der du (vedlikeholdspersonen som er logget på systemet), kan være tilordnet. Hvis ingen arbeidssteder er definert for en vedlikeholdsperson i skjemaet [Vedlikeholdsarbeidere og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md), er ikke kategorien **Mine aktiva** synlig. Kategorien **Aktive aktiva** inneholder en liste over alle aktiva med statusen "Aktiv" for livsløpstilstanden. Kategorien **Aktivavisning** viser en trevisning av arbeidssteder og aktiva som er installert på disse stedene.

6. Standard arbeidssted du har definert, foreslås for aktivumet i **Aktiva**-gruppen > **Arbeidssted**-feltet. Velg et annet arbeidssted, om nødvendig.

    >[!NOTE]
    >Når du har opprettet et aktivum, kan du installere det på et annet arbeidssted, om nødvendig. Bare aktiva på øverste nivå (aktiva uten et overordnet objekt) kan installeres på et arbeidssted. Dette betyr at du installerer både det øverste nivået i tillegg til eventuelle underordnede objekter på det valgte arbeidsstedet. Les mer om hvordan du installerer aktiva på arbeidssteder i [Innføring i arbeidssteder](../functional-locations/introduction-to-functional-locations.md).

7. Klikk **OK**.
8. Velg aktivumet i **Alle aktiva**-listen, og klikk på **Rediger**-knappen for å legge til mer informasjon om aktivumet.

## <a name="general-information"></a>Generell informasjon

Arbeidsstedet som aktivumet er relatert til, vises i **Arbeidssted**-feltet. Hvis aktivumet er et overordnet objekt, vises antallet underordnede som er knyttet til aktivumet, i feltet **Underordnet**. Hvis aktivumet er et underaktivum til et eksisterende aktivum, vises ID-en til det overordnede objektet i feltet **Overordnet**.

Du kan redigere **Aktivaprodusent** og **Aktivamodell** for aktivumet, som brukes til å administrere reservedeler, alternative reservedeler og jobbtypestandarder. Referer til [Aktivaprodusenter og -modeller](../setup-for-objects/product-and-model.md) for mer informasjon. Du kan også legge til informasjon om **modellår** og **serienummer**, om nødvendig.

**Gjeldende livsløpstilstand** brukes til å definere om aktivaet er aktivt eller inaktivt. Når du oppretter et aktivum, settes stadiet alltid til den første fasen i aktivafasegruppen. Når du er klar til å aktivere et aktivum, klikker du på **Oppdater aktivatilstand**og velger deretter livsløpstilstanden du har definert som "aktivum aktivt", og klikk på **OK**.

**Merk:** Når et aktivum er satt til "inaktiv", er det ikke lenger mulig å opprette arbeidsordrer for aktivumet. Du kan heller ikke planlegge forebyggende vedlikeholdsjobber for et inaktivt aktivum.

Feltene **Servicenivå** og **Kritikalitet** relaterer til arbeidsordrer opprettet for aktivumet. Feltene viser tallene for **Servicenivå** og **Kritikalitet** som er beregnet for det gjeldende oppsettet for aktivumet. Se [Servicenivåer for aktivum](../setup-for-objects/object-priorities.md) og [Type kritisk aktivitet for aktiva](../setup-for-objects/object-criticalities.md) angående oppsettet av disse verdiene.

## <a name="asset"></a>Aktivum

Du kan velge en **ressurs** for aktivaet. Ressursvalget bestemmer hvilken kalender som brukes for planlegging av arbeidsordrer. Ressursvalg brukes ofte for anleggsmidler. Ressurser og ressursgrupper satt opp i **Organisasjonsstyring** > **Ressurser** > **Ressursgrupper** eller **Ressurser**.

I feltet **Anleggsmiddelnummer** kan du velge et anleggsmiddel som skal være relatert til aktivaet. Dette er relevant hvis aktivaet er knyttet til et investeringsprosjekt.

- Hvis aktivaet er knyttet til et anleggsmiddel, kan du opprette en arbeidsordretype som skal brukes for arbeidsordrer som er knyttet til et investeringsprosjekt. 
- Informasjon om anleggsmidler for et aktivum er knyttet til modulen **Anleggsmidler** i Dynamics 365 Supply Chain Management. Dette betyr at i **Anleggsmidler** > **Anleggsmidler** > **Anleggsmidler** kan du få en oversikt over prosjektene i Aktivastyring som kan være relatert til et anleggsmiddel, ved å velge aktivumet i listen og vise innholdet i ruten **Beslektet informasjon** > delen **Tilknyttede prosjekter**.


## <a name="details"></a>Detaljer

I **Aktiv fra**-feltet vises datoen da du oppdaterte livsløpstilstanden for aktivumet til en aktiv tilstand (se [Livsløpstilstander](../setup-for-objects/object-stages.md) angående oppsettet av livsløpstilstander for aktiva). Hvis aktivumet ikke lenger er aktivt og du har oppdatert livsløpstilstanden for aktivumet til en inaktiv tilstand, vises datoen som aktivaet er inaktivt fra, i **Aktiv til**-feltet. Du kan endre disse datoene manuelt om nødvendig.

Hvis det er nødvendig, kan du sette inn en forventet dato for erstatning av aktivumet i feltet **Erstatningsdato**. En estimert verdi for å erstatte aktivumet kan settes inn i feltet **Erstatningsverdi**. Eksempel: Du kan bruke erstatningsinformasjon til å sammenligne den med kostnadene for vedlikehold av et aktivum, og deretter ta en beslutning om å kjøpe et nytt aktivum hvis vedlikeholdskostnadene på eksisterende aktiva øker raskt.

## <a name="notes"></a>Notater

Du kan legge til merknader relatert til aktivumet på hurtigfanen **Notater**. Klikk på knappen **Legg til tidsstempel** før du skriver notatet, hvis du vil legge til brukerinformasjon og et dato-/klokkeslettstempel i notatet.

## <a name="attributes"></a>Attributter

På denne hurtigfanen kan du angi verdier for aktivumattributter. Disse attributtene kan brukes til å beskrive egenskaper som er relevante for aktivaet, for eksempel størrelse, vekt eller maskinkonfigurasjon.

Klikk på **Legg til linje**, og velg attributtypen. Deretter setter du inn **verdien** som er knyttet til attributtypen, og lagrer oppføringen.

>[!NOTE] 
>Du kan få en oversikt over aktivaattributtypene og deres forhold til aktivaene i **Aktivaattributt** og **Oversikt over aktivaattributter**. Se [Oversikt over aktivaattributter](../objects/object-specification-overview.md) for mer informasjon.

## <a name="vendor"></a>Leverandør

På hurtigfanen **Leverandør** velger du en leverandørkonto for aktivumet. Hvis en leverandørgaranti er innvilget, kan du også sette inn garantiinformasjon her.

## <a name="address"></a>Adresse

På hurtigfanen **Adresse** kan du sette inn adressen til utstyret. Hvis ingen adresse er satt inn på aktivaet, bruker aktivaet adressen til et overordnet objekt hvis det overordnede objektet har en adresse. Hvis ingen adresse er knyttet til aktivumet eller noen av de overordnede i aktivahierarkiet, kan adressen til arbeidsstedet der aktivumet er installert, brukes. Hvis dette arbeidsstedet ikke har en adresse knyttet til seg, brukes adressen til det overordnede arbeidsstedet på aktivumet.

## <a name="asset-management-plans"></a>Aktivastyringsplaner

Vedlikeholdsplaner brukes til å planlegge forebyggende vedlikeholdsjobber med regelmessige intervaller på aktivumet. På denne hurtigfanen kan du definere vedlikeholdsplanlinjer for det valgte aktivumet. Vedlikeholdsrunder kan settes opp for ulike aktiva, der du må utføre en lignende oppgave med jevne mellomrom. I kategorien **Vedlikeholdsplaner for arbeidssted** ser du vedlikeholdsplanene som er knyttet til arbeidsstedet der aktivumet er installert.

>[!NOTE]
>Hvis du sletter en vedlikeholdsplanlinje eller en vedlikeholdsrunde knyttet til et aktivum i **Alle aktiva**, sletter du også automatisk alle vedlikeholdsplaner med statusen "Opprettet" som er opprettet basert på denne vedlikeholdsplanen eller vedlikeholdsrunden.

## <a name="functional-location-maintenance-plans"></a>Vedlikeholdsplaner for arbeidssteder

På denne hurtigfanen får du en oversikt over vedlikeholdsplanene som er knyttet til arbeidsstedet der aktivumet er installert.

## <a name="maintenance-rounds"></a>Vedlikeholdsrunder

På denne hurtigfanen kan du legge til eller fjerne vedlikeholdsrunder som er knyttet til aktivumet.

## <a name="financial-dimensions"></a>Finansdimensjoner

Du kan velge en finansdimensjon for aktivaet.
