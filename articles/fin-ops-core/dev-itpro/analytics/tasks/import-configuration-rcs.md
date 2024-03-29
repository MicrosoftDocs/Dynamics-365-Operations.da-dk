---
title: (ER) Importere konfigurationer fra RCS
description: Denne artikel giver oplysninger om, hvordan en bruger kan importere en ny version af en ER-konfiguration fra RCS.
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
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290028"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Importere konfigurationer fra RCS

[!include [banner](../../includes/banner.md)]

Følgende trin beskriver, hvordan en bruger i rollen som systemadministrator eller udvikler af elektronisk rapportering kan importere en ny version af en elektronisk rapporteringskonfiguration (ER) til Microsoft Regulatory Configuration Services (RCS). I dette eksempel skal du vælge den version af ER-konfigurationen, der er konfigureret i en RCS-forekomst, og importere den til den aktuelle forekomst for eksempelfirmaet, litware, Inc. Disse trin kan udføres for alle firmaer, fordi ER-konfigurationer deles mellem firmaer. For at fuldføre disse trin skal du først fuldføre trinnene i artiklen [Oprette konfigurationsudbydere og markere dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). Hvis du vil udføre disse trin, skal du også have adgang til en RCS-forekomst, der indeholder mindst én ER-konfiguration, der enten har statussen **Fuldført** eller **Delt**.

1. Gå til **Organisationsadministration** > **Arbejdsområder** > **Elektronisk rapportering**. 
2. Sørg for, at konfigurationsudbyderen for eksempelfirmaet Litware Inc. er tilgængelig og markeret som **Aktiv**. Hvis denne konfigurationsudbyder ikke vises, skal du fuldføre trinnene i artiklen [Opret konfigurationsudbydere, og markér dem som aktive](er-configuration-provider-mark-it-active-2016-11.md). 
3. Hvis du ikke har klargjort et RCS-miljø til dit firma, skal du vælge det eksterne link **Regulatory services – konfiguration** og følge instruktionerne for at klargøre et RCS-miljø. 
4. Vælg **Parametre til elektronisk rapportering**. 
5. Vælg fanen **RCS**. 
6. Hvis RCS-miljøet allerede er klargjort til dit firma, skal du anvende indstillingen for præsenteret på sidens URL-adresser for at få adgang til det. 
7. Luk siden. 

## <a name="register-a-new-er-repository"></a>Registrere et nyt ER-lager. 
1. Markér den valgte række på listen. 
2. Vælg Litware, Inc.-udbyder 
3. Vælg Lagre. 
4. Vælg Tilføj for at åbne dialogboksen. 
5. Skriv RCS i feltet Konfigurationslagertype. 
6. Vælg Opret lager. 
7. Angiv eller vælg en værdi i feltet for vist navn for RCS-miljø. 
8. Vælg det ønskede RCS-forekomst. Du kan have flere af dem. 
9. Vælg OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Importere ER-konfigurationer fra RCS-baseret lager
1. Vælg **Vis filtre**. 
2. Angiv filterværdien "RCS" i feltet **Navn** ved hjælp af filteroperatoren **begynder med**. 
3. Når du åbner det valgte lagersted, skal du på siden **Forbind til Regulatory Configuration Services** vælge linket **Klik her for at oprette forbindelse til Regulatory Configuration Services**. 
4. Vælg **Åbn**. 
5. Vælg **Luk**. 
6. Vælg den ønskede version af ER-konfigurationen, og vælg **Importér** for at overføre den til den aktuelle forekomst.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
