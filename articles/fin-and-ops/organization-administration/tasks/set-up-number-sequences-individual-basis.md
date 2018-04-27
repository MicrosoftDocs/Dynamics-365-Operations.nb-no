--- 
title: Konfigurere nummerserier enkeltvis
description: "Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem."
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e2808e57dc8d137fac892d48e99d7687ff1bf81
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Konfigurere nummerserier enkeltvis

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Nummerserier brukes til å generere lesbare, unike IDer for hoveddataposter og transaksjonsposter som krever dem. En hoveddata- eller transaksjonspost som krever en ID kalles en referanse. Du må konfigurere en nummerserie og tilknytte den referansen før du kan opprette nye poster for en referanse. Du kan konfigurere alle nødvendige nummerserier samtidig ved å bruke veiviseren Definer nummerserier, eller du kan opprette eller endre enkeltnummerserier ved å bruke siden Nummerserier.

1. Gå til Organisasjonsadministrasjon > Nummerserier > Nummerserier.
2. Klikk Nummerserie.
3. Skriv inn en verdi i feltet Nummerserie.
4. Skriv inn en verdi i Navn-feltet.
5. Vis delen Omfangsparametere.
    * I hurtigfanen Omfangsparametere velger du et omfang for nummerserien og velger omfangsverdier.     Omfanget angir hvilke organisasjoner som bruker nummerserien. Nummerserier som har et annet omfang enn Delt, kan i tillegg ha segmenter som samsvarer med omfanget. En nummerserie med omfanget Juridisk enhet kan for eksempel inneholder et segment for en juridisk enhet. Hvis du vil ha mer informasjon om omfang, kan du se hjelpeemnet Oversikt over nummerserie.  
6. Utvid seksjonen Segmenter.
    * I hurtigfanen Segmenter angir du formatet for nummerserien ved å legge til, fjerne og ordne segmenter.  
    * Nummerserier for alle områder kan inneholde Konstant-segmenter og Alfanumerisk-segmenter. Konstant-segmenter inneholder et sett med alfanumeriske tegn som ikke endres. Bruk denne segmenttypen til å legge til en bindestrek eller andre skilletegn mellom nummerseriesegmenter. Alfanumerisk-segmenter inneholder en kombinasjon av nummertegn (#) og &-tegn. Disse tegnene representerer bokstaver og tall som økes hver gang et nummer i serien brukes. Bruk nummertegnet (#) for å angi økende tall og et &-tegn for å angi økende bokstaver. Formatet #####_2014 oppretter for eksempel serien 00001_2014, 00002_2014 og så videre.     Det må finnes minimum ett alfanumerisk segment. Omfangselementer, for eksempel firma eller juridisk enhet, er ikke obligatorisk. Hvis du ikke inkluderer omfangselementer i formatet, genereres det imidlertid tall per omfang for den valgte referansen.  
7. Vis delen Referanser.
    * I hurtigfanen Referanser velger du dokumenttypen eller posten nummerserien skal tilordnes.     Dette trinnet er valgfritt for serier som er angitt for mønstre for bruk av spesialprogrammer. I slike scenarier genereres et nytt tall ved hjelp av verdien for en nummerseriekode eller ID, uten bruk av en referanse. Et eksempel på et mønster for bruk av spesialprogram er en bilagsserie som brukes for spesifikke journalnavn. Det anbefales imidlertid ikke at du bruker slike mønstre.  
8. Utvid seksjonen Generelt.
    * I hurtigfanen Generelt angir du om en nummerserie er manuell, sammenhengende eller ikke-sammenhengende. Angi i tillegg det minste og største tallet som kan brukes i nummerserien.     Det anbefales ikke at du endrer ikke-sammenhengende nummerserier til sammenhengende nummerserier. Nummerserien vil ikke være virkelig sammenhengende. Denne endringen kan også føre til duplikatnøkkelbrudd i databasen. Sammenhengende nummerserier har i tillegg en større innvirkning på ytelsen.   
9. Klikk Lagre.


