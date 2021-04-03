---
title: Konfigurere nummerserier enkeltvis
description: Dette emnet forklarer hvordan du konfigurerer nummerserier enkeltvis.
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ae2fb85bfca6c6a30ec5bd7a13838628a6376f9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560513"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Konfigurere nummerserier enkeltvis

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer nummerserier enkeltvis. Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Du kan konfigurere alle nødvendige nummerserier samtidig ved å bruke veiviseren **Definer nummerserier**, eller du kan opprette eller endre enkeltnummerserier ved å bruke siden **Nummerserier**.

1. Gå til **Navigasjonsrute > Moduler > Organisasjonsadministrasjon > Nummerserier > Nummerserier**.
2. Velg **Nummerserie**.
3. Skriv inn en verdi i feltet **Nummerseriekode**.
4. Skriv inn en verdi i **Navn**-feltet.
5. I hurtigfanen **Omfangsparametere** velger du et omfang for nummerserien og velger omfangsverdier fra rullegardinlisten. Omfanget angir hvilke organisasjoner som bruker nummerserien. Nummerserier som har et annet omfang enn **Delt**, kan i tillegg ha segmenter som samsvarer med omfanget. En nummerserie med omfanget **Juridisk enhet** kan for eksempel inneholder et segment for en juridisk enhet. Hvis du vil ha mer informasjon om omfang, kan du se [Oversikt over nummerserie](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview). 
6. Utvid seksjonen **Segmenter**.
    - Definer formatet for nummerserien ved å legge til, fjerne og ordne segmenter.  
    - Nummerserier for alle områder kan inneholde *Konstant-segmenter* og *Alfanumerisk-segmenter*. Konstant-segmenter inneholder et sett med alfanumeriske tegn som ikke endres. Bruk denne segmenttypen til å legge til en bindestrek eller andre skilletegn mellom nummerseriesegmenter. Alfanumerisk-segmenter inneholder en kombinasjon av nummertegn (#) og &-tegn. Disse tegnene representerer bokstaver og tall som økes hver gang et nummer i serien brukes. Bruk nummertegnet (#) for å angi økende tall og et &-tegn for å angi økende bokstaver. Formatet `#####_2014` oppretter for eksempel serien `00001_2014`, `00002_2014` og så videre. Det må finnes minimum ett alfanumerisk segment. Omfangselementer, for eksempel firma eller juridisk enhet, er ikke obligatorisk. Hvis du ikke inkluderer omfangselementer i formatet, genereres det imidlertid tall per omfang for den valgte referansen.  
7. Vis delen **Referanser**. Velg dokumenttypen eller posten nummerserien skal tilordnes. Dette trinnet er valgfritt for serier som er angitt for mønstre for bruk av spesialprogrammer. I slike scenarier genereres et nytt tall ved hjelp av verdien for en nummerseriekode eller ID, uten bruk av en referanse. Et eksempel på et mønster for bruk av spesialprogram er en bilagsserie som brukes for spesifikke journalnavn. Det anbefales imidlertid ikke at du bruker slike mønstre.  
8. Utvid delen **Generelt**. I hurtigfanen Generelt angir du om en nummerserie er manuell, sammenhengende eller ikke-sammenhengende. Angi i tillegg det minste og største tallet som kan brukes i nummerserien. Det anbefales ikke at du endrer ikke-sammenhengende nummerserier til sammenhengende nummerserier. Nummerserien vil ikke være virkelig sammenhengende. Denne endringen kan også føre til duplikatnøkkelbrudd i databasen. Sammenhengende nummerserier har i tillegg en større innvirkning på ytelsen.   
9. Klikk på **Lagre**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]