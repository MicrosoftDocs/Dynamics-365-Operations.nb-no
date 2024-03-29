---
title: Registrere varer aktivert for lagerstyringsprosesser ved å bruke en journal for vareankomst
description: Denne artikkelen presenterer et scenario som viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker Warehouse Management-prosesser (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66fc9e21b79d70ec14750440c74d354bb8ec0695
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219606"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Registrere varer aktivert for lagerstyringsprosesser ved å bruke en journal for vareankomst

[!include [banner](../../includes/banner.md)]

Denne artikkelen presenterer et scenario som viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker Warehouse Management-prosesser (WMS). Dette gjøres vanligvis av en mottaksassistent.

## <a name="enable-sample-data"></a>Aktivere eksempeldata

Hvis du vil gå gjennom dette scenariet ved hjelp av eksempelpostene og verdiene som er angitt i denne artikkelen, må du bruke et system der standard [demodata](../../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert, og du må velge den juridiske enheten *USMF* før du begynner.

Du kan i stedet gå gjennom dette scenariet ved å erstatte verdier fra dine egne data hvis du har følgende data tilgjengelige:

- Du må ha en bekreftet bestilling med en åpen bestillingslinje.
- Varen på linjen må være lagerført. Den må ikke brukes produktvarianter og må ikke ha sporingsdimensjoner.
- Varen må være tilknyttet en lagringsdimensjonsgruppe som har lagerbehandlingsprosessen aktivert.
- Lageret som brukes, må være aktivert for WMS, og lokasjonen som du bruker for mottak, må være nummerskiltkontrollert.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Opprett et journalhode for vareankomst som bruker lagerstyring

Dette scenariet viser hvordan du oppretter et journalhode for vareankomst som bruker lagerbehandling:

1. Kontroller at systemet inneholder en bekreftet bestilling som oppfyller kravene som er beskrevet i den forrige delen. Dette scenariet bruker en bestilling for firmaet *USMF*, leverandørkontoen *1001*, lageret *51*, med en ordrelinje for *10 PL* (10 paller) med varenummer *M9200*.
1. Noter deg bestillingsnummeret som du vil bruke.
1. Gå til **Lagerstyring \> Loggoppføringer \> Vareankomst \> Vareankomst**.
1. Velg **Ny** i handlingsruten.
1. Dialogboksen **Opprett lagerbehandlingsjournal** åpnes. Velg et journalnavn i **Navn**-feltet.
    - Hvis du bruker *USMF*-eksempeldata, velger du *WHS*.
    - Hvis du bruker dine egne data, må journalen du velger, ha **Kontroller plukklokasjon** satt til *Nei* og **Karantenestyring** satt til *Nei*.
1. Angi **Referanse** til *Bestilling*.
1. Angi **Kontonummer** til *1001*.
1. Angi **Nummer** til nummeret på bestillingen som du identifiserte for denne øvelsen.

    ![Vareankomstjournal.](../media/item-arrival-journal-header.png "Vareankomstjournal")

1. Velg **OK** for å opprette journalhodet.
1. I **Journallinjer**-delen velger du **Legg til linje** og angir følgende data:
    - **Varenummer** – Angi til *M9200*. **Sted**, **Lager** og **Antall** blir angitt basert på lagertransaksjonsdataene for de 10 pallene (1000 per stk.).
    - **Lokasjon** – Angi til *001*. Denne bestemte lokasjonen sporer ikke nummerskilt.

    ![Vareankomstjournallinje.](../media/item-arrival-journal-line.png "Vareankomstjournallinje")

    > [!NOTE]
    > **Dato**-feltet bestemmer hvilken dato når lagerbeholdningen for denne varen skal registreres i lageret.  
    >
    > **Parti-ID** fylles ut av systemet hvis den kan identifiseres unikt fra informasjonen. Ellers må du angi den manuelt. Dette er et obligatorisk felt, som kobler denne registreringen til en bestemt kildedokumentlinje.  

1. Velg **Valider** i handlingsruten. Dette kontrollerer at journalen er klar for postering. Hvis valideringen mislykkes, må du rette opp feilene før du kan postere journalen.  
1. Dialogboksen **Kontroller journal** åpnes. Velg **OK**.
1. Gå gjennom meldingslinjen. Det skal være en melding om at operasjonen er fullført.  
1. Velg **Poster** i handlingsruten.
1. Dialogboksen **Poster journal** åpnes. Velg **OK**.
1. Gå gjennom meldingslinjen. Det skal være meldinger om at operasjonen er fullført.
1. Velg **Funksjoner > Produktmottak** i handlingsruten for å oppdatere bestillingslinjen og postere et produktmottak.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
