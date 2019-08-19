---
title: Aktivamål
description: Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783497"
---
# <a name="asset-measures"></a>Aktivamål

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring. Aktivamåltyper brukes til å foreta målingsregistreringer på aktiva, for eksempel når det gjelder antall produksjonstimer eller antall som produseres på aktivumet. Aktivatyper er knyttet til aktivamåltypene. Dette betyr at et aktivamål bare kan brukes på et aktivum hvis aktivumet er definert på aktivatypen som brukes på aktivumet.

Før du kan foreta målingsregistreringer for aktiva, må du først opprette aktivamåltypene du vil bruke, i **Tellere**. Deretter kan du opprette målingsregistreringer for aktiva i **Aktivamål**. 

Aktivamål kan brukes på vedlikeholdsplaner. En vedlikeholdsplanlinje kan være av typen "Teller", for eksempel knyttet til antall produksjonstimer eller antallet som er produsert. 

En aktivaregistrering kan oppdateres manuelt eller automatisk, basert på produksjonstimer eller produsert antall. Et aktivum kan konfigureres til å bruke én av tre oppdateringsmetoder (valgt i **Oppdater**-feltet i **Tellere**):
  
- Manuell – du må registrere verdier for aktivamål manuelt.  
- Produksjonstimer – telleren oppdateres automatisk basert på antall produksjonstimer.  
- Produksjonsantall – telleren oppdateres automatisk basert på antallet som er produsert.  

>[!NOTE]
>Hvis produsert antall brukes, blir *alle* registrerte varer inkludert i målingsregistreringen, korrekt antall så vel som feil antall. Det er alltid mulig å utføre manuelle aktivamålregistreringer om nødvendig.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Opprette tellertyper for aktivatellerregistreringer

1. Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere**.
2. Velg **Ny** for å opprette en ny aktivamåltype.
3. Sett inn en ID i **Teller**-feltet og et tellernavn i **Navn**-feltet.
4. På hurtigfanen **Generelt** velger du en målenhet i **Enhet**-feltet.
5. I **Oppdater**-feltet velger du oppdateringsmetoden som skal brukes for aktivamålet.
6. Velg "Ja" på veksleknappen **Arv tellerverdier** hvis underordnede aktiva i en aktivastruktur automatisk skal arve aktivamålregistreringer som er opprettet på det overordnede aktivumet.
7. I **Total mengde**-feltet velger du summeringsmetoden som skal brukes for et aktivamål ved bruk av denne aktivamåltypen. "Sum" er standardvalget som brukes til å legge til registrerte verdier i totalverdien kontinuerlig. "Gjennomsnitt" kan brukes hvis det er definert et aktivamål for å overvåke en terskel, for eksempel med temperatur, vibrasjoner eller slitasje på et aktivum. 
8. I feltet **Avvik over** setter du inn det øvre nivået i prosent for validering hvis manuelle aktivamålregistreringer er innenfor et forventet område. Valideringen er basert på lineær økning i eksisterende aktivamålregistreringer.
9. I feltet **Avvik under** setter du inn det nedre nivået i prosent for validering hvis manuelle aktivamålregistreringer er innenfor et forventet område. Valideringen er basert på lineær reduksjon i eksisterende aktivamålregistreringer.
10. I **Type**-feltet velger du meldingstypen (informasjon, advarsel, feil) som skal vises hvis avvik utenfor det definerte området forekommer når du utfører manuelle aktivamålregistreringer.
11. På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal kunne bruke aktivamalen.
12. På hurtigfanen **Relaterte aktivamål** legger du til aktivamålene du vil skal bli automatisk oppdatert når dette aktivamålet oppdateres.


>[!NOTE]
>Et relatert aktivum oppdateres automatisk bare hvis det tilknyttede aktivumet har aktivatypen som det er relatert til, i aktivamåloppsettet. For eksempel: Du definerer et aktivamål for "produksjon timer" og legger til aktivatypen "lastebilmotor". Når dette aktivumet oppdateres, oppdateres også en beslektet teller med verdien "olje" med de samme anleggsmålverdiene. Oppsettet i **Tellere** inkluderer oppsettet på timer. I aktivamålet "olje" må også aktivatypen "lastebilmotor" legges til på hurtigfanen **Aktivatyper** for å sikre aktivamålrelasjonen. Se skjermbildene nedenfor for et eksempel på oppsettet for aktivamålene for timer og olje.

Når aktivatyper legges til for en aktivamåltype i **Tellere**, blir dette aktivamålet automatisk lagt til for aktivatypene på hurtigfanen **Tellere** i [Aktivatyper](../setup-for-objects/object-types.md)

![Figur 1](media/071-setup-for-objects.png)


