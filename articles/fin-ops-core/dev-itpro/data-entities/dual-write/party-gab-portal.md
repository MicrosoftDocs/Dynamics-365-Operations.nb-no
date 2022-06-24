---
title: Bruke Microsoft Power Apps-portaler med partdatamodellen
description: Denne artikkelen beskriver endringene i webrollene i Microsoft Power Apps-portaler på grunn av partdatamodellen i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: c2e9d0f47ef90167bf84bb5b20e6a7ad2d58ffd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898953"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Bruke Microsoft Power Apps-portaler med partdatamodellen

[!INCLUDE[banner](../../includes/banner.md)]



Versjon 2.0.999.0 og senere av løsningen for orkestrering av apper med dobbel skriving inkluderer endringer i datamodeller for parter og global adressebok tabellene Konto og Kontakt. Endringene tillater mange-til-mange-relasjoner som støtter avanserte forretningsscenarier. Disse endringene støttes ikke av webroller for portaler, inkludert kundeportalen, som følger med som standard, eller som allerede fantes i miljøet ditt før du installerte dobbel skriving. For at webrollene skal fungere som forventet, må du opprette nye webroller ved hjelp av den nye datamodellen. 

Kort sagt er måten tabellene fungerer på endret, men tabelltillatelsene i kundeportalen er ikke endret. Denne artikkelen beskriver hvordan du oppretter nye webroller som arbeider med den nye avanserte datamodellen.

Dette diagrammet viser tabellrelasjonen **uten** parten og den globale adressebokdatamodellen:

   ![uten partmodell.](media/without-party-model.PNG)

Dette diagrammet viser tabellrelasjonen **med** parten og den globale adressebokdatamodellen:

   ![med partmodell.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Opprette en ny tabelltillatelse

Følg denne fremgangsmåten for å opprette disse nye tabelltillatelsene:

1. Logg deg på [Power Apps](https://make.powerapps.com), og gå til appene.
2. Velg Portal Management-appen.
3. Velg **Sikkerhet > Tabelltillatelser** i sidefeltet.

    Du må opprette tre nye tillatelser:

    + **Kontakt** til **part**-tabelltilkobling
    + **Part** til **konto**-tabelltilkobling
    + **Konto** til **ordre**-tabelltilkobling

4. Opprett og lagre en ny tillatelse for Kontakt til part-tilkoblingen ved å angi disse parameterne:

    + **Navn**: **Part** til **konto**-tabelltilordning (eller ditt valg)
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
