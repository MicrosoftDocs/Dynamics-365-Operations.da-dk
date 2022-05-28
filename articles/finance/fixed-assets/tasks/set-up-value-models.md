---
title: Opret værdimodeller
description: Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727055"
---
# <a name="set-up-value-models"></a>Opret værdimodeller

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Denne procedure viser, hvordan du opretter et nyt anlægskartotek og knytter det til en anlægsaktivgruppe.

## <a name="create-a-book"></a>Opret en bog
1. Gå til **Anlægsaktiver** \> Opsætning \> Bøger.
2. Vælg **Ny**.
3. Angiv en værdi i feltet **Bog**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Angiv indstillingen **Beregn afskrivning** til **Ja**.

    Hvis indstillingen **Beregn afskrivning** er angivet til **Ja**, medtages den tilknyttede aktivbog i afskrivningsforslag. Hvis den er angivet til **Nej**, afskrives anlægskartotek ikke automatisk.

6. Indtast eller vælg en værdi i feltet **Afskrivningsprofil**.

    * En alternativ afskrivningsprofil kaldes også en switch-over-metode til afskrivning. Afskrivningsforslaget skifter til denne profil, når den alternative profil beregner et afskrivningsbeløb, der er lig med eller større end standardafskrivningsprofilen.
    * Afskrivningsprofilen Ekstraordinær bruges som yderligere afskrivningsmetode for et aktiv under usædvanlige omstændigheder. Du kan f.eks. bruge dette til at registrere afskrivning, der sker som følge af en naturkatastrofe.
    * Hvis du vælger **Opret reguleringer af afskrivning med basisreguleringer**, oprettes afskrivningsreguleringer automatisk, når værdien af aktivet opdateres. Ellers påvirker den opdaterede aktivværdi kun fremtidige afskrivningsberegninger.

7. Angiv indstillingen **Opret reguleringer af afskrivning med basisreguleringer** til **Ja**.

    * Transaktioner i bogen til anlægsaktiver bogføres som standard i finansmodulet. Men du kan deaktivere bogføring i finansmodulet for bogen ved at angive indstillingen **Bogfør i finans** til **Nej**. Bøger, der ikke bogføres i finansmodulet, bruges typisk til momsrapporteringen. Denne indstilling giver dig mere fleksibilitet til at slette historiske posteringer for anlægsaktivkartoteket, fordi transaktionerne ikke er gemt i finansmodulet.
    * Feltet **Posteringslag** angives som standard til **Nuværende lag**, hvis bogen bogføres i finans, og til **Ingen**, hvis bogen ikke bogføres i finans. Opdater værdien i feltet **Posteringslag**, hvis transaktioner for denne bog skal bogføres til et andet lag.

8. Beregn positiv afskrivning.

    * Som standard er indstillingen **Beregn positiv afskrivning** angivet til **Nej**. Denne indstilling angiver, at afskrivningen krediterer det valgte anlægsarkiv. Derudover er indstillingerne for **Tillad bogført nettoværdi, der er højere end anskaffelsesprisen**, og **Tillad negativ bogført nettoværdi** begge angivet til **Nej**, og indstillingerne kan ændres uafhængigt. 
    * Hvis du vil beregne positiv afskrivning, skal du angive indstillingen **Beregn positiv afskrivning** til **Ja**. Denne indstilling angiver, at afskrivningen debiterer anlægsaktivbogen. Når indstillingen **Beregn positiv afskrivning** er angivet til **Ja**, angives indstillingen **Tillad bogført nettoværdi, der er højere end anskaffelsesprisen** og **Tillad negativ bogført nettoværdi** automatisk til **Ja**, og de spærres. Denne spærring hjælper med at sikre, at positiv afskrivning kun anvendes på anlægsaktiver, der er anskaffet med negativ bogført værdi (kredit). 

10. Indtast eller vælg en værdi i feltet **Kalender**.

    Afledte bøger bogfører transaktioner til forskellige bøger på samme tid. Du kan oprette posteringer med den primære bog, og under bogføring bogføres en nøjagtig kopi af posteringen i den afledte bog. Der er ingen genberegning med afledte posteringer, så det ikke skal bruges til afskrivningsposteringer.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Knyt bogen til en anlægsaktivgruppe

1. Vælg **Anlægsaktivgrupper**.
2. Skriv eller vælg en værdi i feltet **Anlægsaktivgruppe**.
3. Angiv et tal i feltet **Levetid**.

    * Afskrivningsperioder beregnes, efter levetiden for aktivet er angivet.
    * Afskrivningsprincippet kan indstilles som påkrævet af skattemæssige årsager.
    * For anlægsaktiver, der er tilknyttet leasinger, tilsidesættes værdien i feltet **Levetid** af den korteste af leasingperioden i anlægsaktivkartoteket og aktivets brugstid. Hvis indstillingen **Overførsel af ejerskab** er angivet til **Ja** for leasingbogen, vil værdien i feltet **Levetid** altid være aktivets brugstid.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
