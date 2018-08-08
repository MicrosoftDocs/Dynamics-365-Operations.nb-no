---
title: "Produktmottak mot kjøpsordrer"
description: "Denne artikkelen beskriver de ulike alternativene for å registrere produktene som mottatt."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93113
ms.assetid: d4ec3e86-fce2-4546-911b-e0acf64c8887
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c227664da360f6f8d54b49f15e1b7160aa142ba9
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="product-receipt-against-purchase-orders"></a>Produktmottak mot kjøpsordrer

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Denne artikkelen beskriver de ulike alternativene for å registrere produktene som mottatt.

Produktmottak er prosessen med å registrere at produkter som ble bestilt, er mottatt, slik at bestillingslinjer deretter kan behandles for fakturering. I noen tilfeller går produkter gjennom forhåndsregistreringen, der tilleggsinformasjon fra leverandøren registreres før varene mottas. Når produkter ankommer, merkes de først som **Registrert**. Produktene kan deretter gå gjennom flere prosesser, for eksempel kvalitetsstyring, før de til slutt merkes som **Mottatt**.

## <a name="preregistration-asn"></a>Forhåndsregistrering (Forhåndsvarsel for forsendelse)
Leverandører kan dele informasjon om produkter som skal leveres. I slike tilfeller kan du forhåndsregistrere produktene for å registrere informasjonen før varene mottas. Ved forhåndsregistrering av produkter, kan du redusere arbeidsmengden kreves under vareregistrering og -mottak. Leverandører kan gi produktinformasjon elektronisk via et forhåndsvarsel for forsendelse (ASN) som deretter registreres automatisk i systemet. Informasjonen i forhåndsvarselet for forsendelse inneholder produktantallet som leveres og datoen de leveres. Forhåndsvarselet for forsendelse kan også omfatte informasjon som parti- eller serienumre. Registrering av forhåndsvarsel for forsendelse utføres i modulen **Transportstyring**.

## <a name="registration"></a>Registrering
Registrering av produktmottak skjer ofte i mottakssoner på et lager. Det utføres ved hjelp av en håndholdt enhet eller via ankomstjournaler. Du kan eventuelt manuelt registrere produktmottak ved hjelp av handlingen **Registrering** på siden **Bestilling**. I begge tilfeller merkes produkter som **Registrert**. Legg merke til at produktene ennå ikke er merket som **Mottatt**.  

Produkter som er mottatt i lageret kan gå gjennom kvalitetsinspeksjon før de er plassert på lageret. Kvalitetsordrer eller karanteneordrer kan brukes til å utføre kvalitetskontroll. Hvis kvalitetsordrer brukes, kan du konfigurere prosessen for å blokkere produkter midlertidig via en reservasjon mens de kontrolleres. Hvis karanteneordrer brukes, flyttes produkter til et annet lager for inspeksjon. Dette lageret kalles karantenelageret. I begge kvalitetsinspeksjonsprosessene kan noen av varene kasseres fordi de ikke samsvarer med forventet kvalitet, eller fordi kvalitetsinspeksjonen omfatter destruktiv testing av et utvalg av produktet.

## <a name="product-receipt"></a>Produktkvittering
Vanligvis brukes handlingen **Produktmottak** på siden **Bestillinger** til å merke produkter som **Mottatt** på bestillingen. Siden **Posterer produktkvittering** har flere forskjellige alternativer for antallet som er registrert som mottatt. Du kan for eksempel sette feltet **Antall** til **Bestilt antall** eller **Motta nå-antall**. Hvis en prosess for ankomst i lageret er brukt, du vil ofte sette dette feltet til **Registrert antall**. Du kan endre antallet for hver ordrelinje som vil bli merket som **Mottatt**, for å ta hensyn til eventuelle avvik, for eksempel underlevering og overlevering. Under produktmottak må du angi en identifikator for produktmottak, som vanligvis er en referanse til følgeseddelen fra leverandøren. Denne identifikatoren er nødvendig for regnskap, fordi den gjør det mulig å aktivere kontrollere eller revisjoner av leverandørfølgesedler mot det som er mottatt, og registrert lager eller utgifter.  

Hvis en ansatt bestilte varer ved hjelp av en innkjøpsrekvisisjon, kan den ansatt bli bedt om å bekrefte mottak av produktet selv. Du kan konfigurere denne virkemåten ved hjelp av en arbeidsflyt. Du kan konfigurere arbeidsflytbetingelsene slik at de samsvarer med forretningsprosessen.  

Bestillinger kan opprettes for produkter som ikke er ment som beholdning, men regnes som en utgift. Denne kategorien inneholder ordrelinjer der produktene er merket som **Ikke lagerført** av lagermodellgruppen, og også linjer som bruker innkjøpskategorier. I slike tilfeller kan det hende varene ikke går gjennom ankomstregistrering og -mottak i lageret. I stedet brukes handlingen **Produktmottak** til å registrere mottaket direkte på bestillingen, og mottaket er basert på det bestilte antallet, ikke det registrerte antallet.  

Du kan opprette bestillingslinjer der alternativet **Nytt anleggsmiddel** er aktivert. Dette alternativet angir at bestillingen skal betraktes som et anleggsmiddel i stedet beholdning. I slike tilfeller vil reglene for fastsettelse av anleggsmidler som er konfigurert, bestemme om kjøpet av produktet eller kategori overskrider bestemt terskler, og må derfor tas med i betraktningen som et anleggsmiddel og gå gjennom anleggsmiddelbehandling. Kjøp kan også gjøres mot et eksisterende anleggsmiddel. I slike tilfeller justeres antallet etter behov.  

Du kan velge flere ordrer og behandle mottak på alle ordrer samtidig. Denne fremgangsmåten brukes ikke så ofte, men det kan hende du vil bruke den hvis en leverandør har konsolidert forsendelser for deg i én enkelt last. Under produktmottaket av kjøpet er det en funksjon for å gjøre samleoppdateringer. Samleoppdateringer lar deg postere en enkelt følgeseddel fra leverandøren for mer enn én bestilling.  

Bestillinger kan opprettes fra en salgsordre der alternativet **Direktelevering** er valgt. Når direktelevering brukes, ankommer produktene aldri på lageret, men de leveres direkte fra leverandøren til kunden. I slike tilfeller registreres mottaket vanligvis direkte på bestillingen. Mottaket kan utføres automatisk, for eksempel via integrering av utveksling av elektroniske data (EDI) med leverandøren. Hvis bestillingen er en konsernintern bestilling, automatiserer Microsoft Dynamics 365 for Finance and Operations mottaket på den konserninterne salgsordren når forsendelse skjer. Når direktelevering brukes, registreres produkter fremdeles som beholdning, selv om de ikke mottas fysisk på lageret. Når produktmottaket registreres på bestillingen, oppdateres derfor salgsordren automatisk med en følgeseddel, slik at den totale endringen i beholdningen er 0 (null). I situasjoner med direktelevering bør du ikke kreve forhåndsregistrering. Hvis du bruker lagre som er aktivert for lagerstyring, kan du omgå kravet til nummerskiltregistrering ved å angi et virtuelt lager i stedet. Du angir dette lageret lager i feltet **Lager for direktelevering** på produktet. 

Når produktmottak er behandlet på bestillingen, sette bestillingsstatusen til **Mottatt** for å angi at fakturaen kan behandles for ordren. Du kan se gjennom informasjon om produkter som allerede er mottatt ved hjelp av siden **Produktkvitteringsjournaler**.  

Du får tilgang til denne siden fra handlingsgruppen **Mottak** på siden **Bestilling**. Informasjonen i journalene inneholder informasjon om antall, datoer og dimensjoner.

<a name="additional-resources"></a>Tilleggsressurser
--------

[Oversikt over bestilling](purchase-order-overview.md)

[Opprett bestilling](purchase-order-creation.md)

[Bestillingsgodkjenning og -bekreftelse](purchase-order-approval-confirmation.md)

[Oversikt over leverandørfakturaer](../../financials/accounts-payable/vendor-invoices-overview.md)




