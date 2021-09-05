---
title: Opret værdimodeller
description: Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe.
author: moaamer
ms.date: 08/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46c26e5fad3c5c60d87c2fea2b29043c69b82b5d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344652"
---
# <a name="set-up-value-models"></a>Opret værdimodeller

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]


Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe. Den bruger rollen Revisor og demodata for den juridiske enhed USMF.

## <a name="create-a-book"></a>Opret en bog
1. Gå til Anlægsaktiver > Opsætning > Bøger.
2. Klik på Ny.
3. Skriv en værdi i feltet Bog.
4. Skriv en værdi i feltet Beskrivelse.
    * Hvis Beregn afskrivning er markeret, medtages den tilknyttede bog for anlægsaktiver i afskrivningsforslag. Hvis feltet ikke er markeret, afskrives anlægskartotek ikke automatisk.  
5. Vælg Ja i feltet Beregn afskrivning.
6. Indtast eller vælg en værdi i feltet Afskrivningsprofil.
    * En alternativ afskrivningsprofil kaldes også en switch-over-metode til afskrivning. Afskrivningsforslaget skifter til denne profil, når den alternative profil beregner et afskrivningsbeløb, der er lig med eller større end standardafskrivningsprofilen.  
    * Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder. Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.  
    * Hvis Opret reguleringer af afskrivning med basisreguleringer er valgt, oprettes afskrivningsreguleringer automatisk, når værdien af aktivet opdateres. Hvis feltet ikke er markeret, påvirker den opdaterede aktivværdi kun afskrivningsberegninger fremadrettet.  
7. Vælg Ja i feltet Opret reguleringer af afskrivning med basisreguleringer.
    * Transaktioner i bogen til anlægsaktiver bogføres som standard i finansmodulet. Du kan deaktivere bogføring i finansmodulet for bogen ved at angive feltet Bogfør i finans til Nej. Bøger, der ikke bogføres i Finans, bruges typisk til momsrapporteringen. Det giver dig yderligere fleksibilitet til at slette historiske posteringer for anlægskartoteket, fordi de ikke er bundet til finansmodulet.  
    * Posteringslaget anvender som laget Nuværende, hvis bogen bogføres i finans, og Ingen, hvis den ikke bogføres i finans. Opdater posteringslag, hvis du har brug for, at transaktioner for denne bog bogføres til et andet lag.  
8. Indtast eller vælg en værdi i feltet Kalender.
    * Afledte bøger bogfører transaktioner til forskellige bøger på samme tid. Du kan oprette posteringer med den primære bog, og under bogføring bogføres en nøjagtig kopi af posteringen i den afledte bog. Der er ingen genberegning med afledte posteringer, så det ikke skal bruges til afskrivningsposteringer.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knyt bogen til en anlægsaktivgruppe
1. Klik på Anlægsaktivgrupper.
2. Skriv eller vælg en værdi i feltet Anlægsaktivgruppe.
3. Angiv et tal i feltet Levetid.

  - Afskrivningsperioder beregnes, efter levetiden for aktivet er angivet.  
  - Afskrivningsprincippet kan indstilles som påkrævet af skattemæssige årsager.
  - For anlægsaktiver, der er tilknyttet leasinger, tilsidesættes værdien i feltet **Levetid** af den korteste af enten leasingperioden i anlægsaktivkartoteket eller aktivets brugstid. Hvis feltet **Overførsel af ejerskab** er angivet til **Ja** for leasingbogen, vil værdien i feltet **Levetid** altid være aktivets brugstid.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
