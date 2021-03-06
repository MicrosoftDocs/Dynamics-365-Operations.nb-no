---
title: Bruke Power Portal med partdatamodellen
description: Dette emnet beskriver endringene i webrollene i Power Portal på grunn av partdatamodellen i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833096"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Bruke Power Portal med partdatamodellen

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Versjon 2.0.999.0 og senere av løsningen for orkestrering av apper med dobbel skriving inkluderer endringer i datamodeller for parter og global adressebok tabellene Konto og Kontakt. Endringene tillater mange-til-mange-relasjoner som støtter avanserte forretningsscenarier. Disse endringene støttes ikke av webroller for portaler, inkludert kundeportalen, som følger med som standard, eller som allerede fantes i miljøet ditt før du installerte dobbel skriving. For at webrollene skal fungere som forventet, må du opprette nye webroller ved hjelp av den nye datamodellen. 

Kort sagt er måten tabellene fungerer på endret, men tabelltillatelsene i kundeportalen er ikke endret. Dette emnet beskriver hvordan du oppretter nye webroller som arbeider med den nye avanserte datamodellen.

Dette diagrammet viser tabellrelasjonen **uten** parten og den globale adressebokdatamodellen:

   ![uten partmodell](media/without-party-model.PNG)

Dette diagrammet viser tabellrelasjonen **med** parten og den globale adressebokdatamodellen:

   ![med partmodell](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Opprette en ny tabelltillatelse

Følg denne fremgangsmåten for å opprette disse nye tabelltillatelsene:

1. Logg deg på [Power Apps](https://make.powerapps.com), og gå til appene.
2. Velg Portal Management-appen.
3. Velg **Sikkerhet > Tabelltillatelser** i sidefeltet.

    Du må opprette tre nye tillatelser:

    + Kontakt til part-tilkobling
    + Part til konto-tilkobling
    + Konto til ordre-tilkobling

4. Opprett og lagre en ny tillatelse for Kontakt til part-tilkoblingen ved å angi disse parameterne:

    + **Navn:** Part til konto-tilkobling (eller ditt valg)
    + **Tabellnavn**: msdyn_contactforparty
    + **Nettsted**: Kundeportal
    + **Omfang:** Kontakt
    + **Rettigheter**: Velg alle
    + **Webroller**: Godkjente brukere, Kunderepresentant (eller ditt valg)

5. Opprett og lagre en ny tillatelse for Part til konto-tilkoblingen ved å angi disse parameterne:

    + **Navn:** Part til konto-tilkobling (eller ditt valg)
    + **Tabellnavn**: Konto
    + **Nettsted**: Kundeportal
    + **Omfang:** Overordnet
    + **Rettigheter**: Velg alle
    + **Overordnet tabelltillatelse**: Kontakt til part-tilkobling

6. Opprett og lagre en ny tillatelse for Konto til ordre-tilkoblingen ved å angi disse parameterne:

    + **Navn:** Konto til ordre-tilkobling (eller ditt valg)
    + **Tabellnavn**: salgsordre
    + **Nettsted**: Kundeportal
    + **Omfang:** Overordnet
    + **Rettigheter**: Velg alle
    + **Overordnet tabelltillatelse**: Part til konto-tilkobling

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
