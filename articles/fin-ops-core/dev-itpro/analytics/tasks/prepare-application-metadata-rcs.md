---
title: Klargjøre programmetadataene som skal brukes i RCS
description: Dette emnet beskriver hvordan du oppretter en ny rapporteringskonfigurasjon som inneholder programmetadata.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9609da50482f39bafe65d3a7b655e5047c74bdba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560123"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Klargjøre programmetadataene som skal brukes i RCS
[!include [banner](../../includes/banner.md)]

Trinnene nedenfor forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan opprette en ny ER-konfigurasjon (elektronisk rapportering) som inneholder programmetadata for utforming av ER-modelltilordningskonfigurasjoner i Regulatory Configuration Service (RCS). Denne konfigurasjonen brukes til å utforme et eksempel på ER-modelltilordningskonfigurasjon for å få tilgang til utenrikshandelstransaksjoner. I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Denne fremgangsmåten kan utføres i et hvilket som helst firma. For å fullføre disse trinnene må du først fullføre trinnene i emnet [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Forutsetninger
1.    Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**. 
2.    Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i prosedyren [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 
3.    Klikk på **Metadatakonfigurasjoner**. 
4.    Anta at RCS brukes til å utforme en ER-løsning for et Finance and Operations-program som skal brukes til å generere elektroniske dokumenter som inneholder informasjon fra forretningsdomenet for utenrikshandel. Hvis du vil angi tilordningen mellom ER-datamodell og kilder til nødvendige data, må vi ha tilgang til programmetadata for Finance and Operations-programmet i RCS. Vi konfigurerer derfor en ny ER-metadatakonfigurasjon som en del av utformingen av ER-løsningen, og som inneholder alle metadataene som kreves for å generere ER-rapporter for det valgte forretningsdomenet. 

## <a name="add-metadata-configuration"></a>Legge til metadatakonfigurasjon 
1.    Klikk på **Opprett konfigurasjon** for å åpne nedtrekksdialogen. 
2.    I **Navn**-feltet skriver du inn «Metadata for utenrikshandel». 
3.    Klikk på **Opprett konfigurasjon**. 
4.    Klikk på **Utforming**. 
5.    Klikk på **Legg til**. 
  
> [!NOTE]
> Du kan velge alle metadataene for hele programmet eller valgte modeller eller moduler. Vær i dette tilfellet oppmerksom på at følgende metadata blir lagt til automatisk: tabeller med poster, opplistinger og utvidede datatyper. Når det er behov flere typer metadata, må de legges til manuelt. 
 
Vi har enkelte metadata som er knyttet til utenrikshandelstransaksjoner, ved å velge metadataelementer manuelt. 
  
6.    Klikk på **Legg til datakilde**. 
7.    Klikk på **Tabellposter**. 
8.    Bruk hurtigfilteret til å filtrere på **Navn**-feltet med verdien «Intrastat». 
9.    Velg **Intrastat**-tabellposten. 
10.    Klikk på **OK**.
  
Vi la til metadatainformasjon om Intrastat-tabellen med poster. 
  
11.    Utvid **Tabellposter Intrastat**\>**Relasjoner** i treet. 
12.    Velg **Tabellposter Intrastat**\>**Relasjoner\IntrastatCommodity (Tabellposter EcoResCategory)** i treet.     
13.    Klikk på **Legg til metadata**. 
  
> [!NOTE]
> Metadata om nødvendige relasjoner for den valgte tabellen med poster må legges til manuelt. 
  
16.    Klikk på **Legg til datakilde**. 
17.    Klikk på **Opplisting**. 
18.    Bruk hurtigfilteret til å filtrere på **Navn**-feltet med verdien «IntrastatDirection». 
19.    Velg posten **IntrastatDirection-opplisting**. 
20.    Klikk på **OK**. 
21.    Klikk på **Lagre**.  
22.    Lukk siden. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Fullføre kladdeversjonen av metadatakonfigurasjonen
1.    Klikk på **Endre status**. 
2.    Klikk på **Fullført**. 
3.    Klikk på **OK**. 
4.    Velg fullført versjon **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Eksportere den fullførte versjonen av metadatakonfigurasjonen fra programmet som en XML-fil
1.    Klikk på **Veksle**. 
2.    Klikk på **Eksporter som XML-fil**. 
3.    Klikk på **OK**. 
    
ER-metadatakonfigurasjonen har blitt lagret som en XML-fil som kan importeres til RCS og brukes som kilden til informasjon om metadata for forretningsdomenet for utenrikshandel. Basert på denne informasjonen kan vi angi tilordningen mellom programmetadata og ER-datamodellen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]