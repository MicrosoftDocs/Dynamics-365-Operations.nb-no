---
title: (ER) Importere konfigurasjoner fra RCS
description: Denne artikkelen inneholder informasjon om hvordan en bruker kan importere en ny versjon av en ER-konfigurasjon fra RCS.
author: kfend
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 55e7a3ae23b708acecb5ac219b885f43b4c7aa0a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290042"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Importere konfigurasjoner fra RCS

[!include [banner](../../includes/banner.md)]

De følgende trinnene forklarer hvordan en bruker i rollen Systemansvarlig eller Utvikler av elektronisk rapportering kan importere en ny versjon av en ER-konfigurasjon (elektronisk rapportering) fra Microsoft Regulatory Configuration Services (RCS). I dette eksemplet skal du velge versjonen av ER-konfigurasjonen som er konfigurert i en RCS-forekomst, og importere den til gjeldende forekomst for eksempelfirma, Litware, Inc. Disse trinnene kan utføres i alle firmaer fordi ER-konfigurasjoner deles mellom firmaer. For å fullføre disse trinnene må du først fullføre trinnene i artikkelen [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). For å kunne fullføre disse trinnene må du også ha tilgang til en RCS-forekomst som inneholder minst én ER-konfigurasjon med statusen **Fullført** eller **Delt**.

1. Gå til **Organisasjonsstyring** > **Arbeidsområder** > **Elektronisk rapportering**. 
2. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet Litware, Inc. er tilgjengelig og merket som **Aktiv**. Hvis du ikke ser denne konfigurasjonsleverandøren, må du fullføre trinnene i artikkelen [Opprette konfigurasjonsleverandører og merke dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 
3. Hvis du ikke har noe RCS-miljø klargjort for firmaet, velger du den eksterne koblingen **Regulatory Services – Configuration** og følger instruksjonene for å klargjøre et RCS-miljø. 
4. Velg **Parametere for elektronisk rapportering**. 
5. Velg kategorien **RCS**. 
6. Hvis RCS-miljøet allerede er klargjort for firmaet ditt, kan du bruke URL-adressene på siden til å få tilgang til det. 
7. Lukk siden. 

## <a name="register-a-new-er-repository"></a>Registrere et nytt ER-repositorium. 
1. Merk den valgte raden i listen. 
2. Velg leverandøren Litware, Inc. 
3. Velg Repositorier. 
4. Velg Legg til for å åpne nedtrekksdialogen. 
5. Angi RCS i feltet Type konfigurasjonsrepositorium. 
6. Velg Opprett repositorium. 
7. Angi eller velg en verdi i feltet for visningsnavn på RCS-miljø. 
8. Velg ønsket RCS-forekomst. Du kan ha flere av dem. 
9. Velg OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Importere ER-konfigurasjoner fra RCS-basert repositorium
1. Velg **Vis filtre**. 
2. Angi filterverdien «RCS» i **Navn**-feltet ved hjelp av filteroperatoren **begynner med**. 
3. Når du åpner det valgte repositoriet, velger du koblingen **Velg her for å koble til Regulatory Configuration Service** på siden **Koble til Regulatory Configuration Services**. 
4. Velg **Åpne**. 
5. Velg **Lukk**. 
6. Velg ønsket versjon av ER-konfigurasjon, og velg **Importer** for å hente den inn i gjeldende forekomst.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
