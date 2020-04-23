---
title: Aktivamål
description: Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d128a7d20891353927441bb343831876d72aecbe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208898"
---
# <a name="counters"></a>Tellere

[!include [banner](../../includes/banner.md)]

Emnet forklarer hvordan du oppretter tellertyper i Aktivastyring. Tellertyper brukes til å foreta tellerregistreringer på aktiva, for eksempel når det gjelder antall produksjonstimer eller antall som produseres på aktivumet. Aktivatyper er knyttet til tellertypene. Dette betyr at en teller bare kan brukes på et aktivum hvis telleren er definert på aktivatypen som brukes på aktivumet.

Før du kan foreta tellerregistreringer for aktiva, må du først opprette tellertypene du vil bruke, i **Tellere**. Deretter kan du opprette tellerregistreringer for aktiva i **Tellere**. 

Tellere kan brukes på vedlikeholdsplaner. En vedlikeholdsplanlinje kan være av typen "Teller", for eksempel knyttet til antall produksjonstimer eller antallet som er produsert. 

En tellerregistrering kan oppdateres manuelt eller automatisk basert på produksjonstimer eller produsert antall. En teller kan konfigureres til å bruke én av tre oppdateringsmetoder (valgt i **Oppdater**-feltet i **Tellere**):
  
- Manuell – du må registrere verdier for tellere manuelt.  
- Produksjonstimer – telleren oppdateres automatisk basert på antall produksjonstimer.  
- Produksjonsantall – telleren oppdateres automatisk basert på antallet som er produsert.  

>[!NOTE]
>Hvis produsert antall brukes, blir *alle* registrerte varer inkludert i tellerregistreringen, korrekt antall så vel som feil antall. Det er alltid mulig å utføre manuelle tellerregistreringer om nødvendig.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Opprette tellertyper for aktivatellerregistreringer

1. Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere**.
2. Velg **Ny** for å opprette en ny tellertype.
3. Sett inn en ID i **Teller**-feltet og et tellernavn i **Navn**-feltet.
4. På hurtigfanen **Generelt** velger du en tellerenhet i **Enhet**-feltet.
5. I **Oppdater**-feltet velger du oppdateringsmetoden som skal brukes for telleren.
6. Velg "Ja" på veksleknappen **Arv tellerverdier** hvis underordnede aktiva i en aktivastruktur automatisk skal arve tellerregistreringer som er opprettet på det overordnede objektet.
7. I **Total mengde**-feltet velger du summeringsmetoden som skal brukes for en teller ved bruk av denne tellertypen. "Sum" er standardvalget som brukes til å legge til registrerte verdier i totalverdien kontinuerlig. "Gjennomsnitt" kan brukes hvis det er definert en teller for å overvåke en terskel, for eksempel med temperatur, vibrasjoner eller slitasje på et aktivum. 
8. I feltet **Avvik over** setter du inn det øvre nivået i prosent for validering hvis manuelle tellerregistreringer er innenfor et forventet område. Valideringen er basert på lineær økning i eksisterende tellerregistreringer.
9. I feltet **Avvik under** setter du inn det nedre nivået i prosent for validering hvis manuelle tellerregistreringer er innenfor et forventet område. Valideringen er basert på lineær reduksjon i eksisterende tellerregistreringer.
10. I **Type**-feltet velger du meldingstypen (informasjon, advarsel, feil) som skal vises hvis avvik utenfor det definerte området forekommer når du utfører manuelle tellerregistreringer.
11. På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal kunne bruke telleren.
12. På hurtigfanen **Relaterte aktivatellere** legger du til telleren du vil skal bli automatisk oppdatert når denne telleren oppdateres.


>[!NOTE]
>En relatert teller oppdateres automatisk bare hvis den tilknyttede telleren har aktivatypen som den er relatert til, i telleroppsettet. For eksempel: Du definerer en teller for "Produksjonstimer" og legger til aktivatypen "Lastebilmotor". Når denne telleren oppdateres, oppdateres også en beslektet teller med verdien "olje" med de samme tellerverdiene. Oppsettet i **Tellere** inkluderer oppsettet på timer. I telleren "olje" må også aktivatypen "Lastebilmotor" legges til på hurtigfanen **Aktivatyper** for å sikre tellerrelasjonen. Se skjermbildene nedenfor for et eksempel på oppsettet for tellerne for timer og olje.

Når aktivatyper legges til for en tellertype i **Tellere**, blir denne telleren automatisk lagt til for aktivatypene på hurtigfanen **Tellere** i [Aktivatyper](../setup-for-objects/object-types.md)

![Figur 1](media/071-setup-for-objects.png)

