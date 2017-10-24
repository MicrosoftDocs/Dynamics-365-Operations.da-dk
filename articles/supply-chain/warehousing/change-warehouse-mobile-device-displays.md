---
title: "Skærmindstillinger for lagerstedets mobilenhed"
description: "I denne artikel beskrives det, hvordan du konfigurerer udseendet på en mobilenheds skærm og knytter tastaturgenvejstaster til kontrolelementer, f.eks. knapper."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Skærmindstillinger for lagerstedets mobilenhed

[!include[banner](../includes/banner.md)]


I denne artikel beskrives det, hvordan du konfigurerer udseendet på en mobilenheds skærm og knytter tastaturgenvejstaster til kontrolelementer, f.eks. knapper. 

Denne artikel gælder for funktioner for "avanceret lagersted" i Lagerstedsstyring. Mobilenheder kan bruges til mange af de opgaver, som lagermedarbejderne udføre.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Angive formater og tilknytte tastaturgenveje
Som en del af konfigurationen af mobilenheden, kan du definere forskellige layout for mobilenheder. Hvis du vil gøre dette, skal du kende navnet på CSS-filen (Cascading Style Sheets) og ASPX-filen (Active Server Page Extension). Standardfilerne er installeret som en del af installationen af Warehouse Mobile Devices Portal. Hvis du ikke kender filnavnene, kan du spørge din systemadministrator. Du kan definere en ny typografi på siden **Mobilenhedens skærmindstillinger**:

-    Angiv navnet på din CSS-fil i feltet **CSS-fil**. Du skal medtage filtypenavnet .css.
-   I feltet **Viser mobilenhedens skærmindstillinger** skal du angive ASPX-filen. Medtag **ikke** filtypenavnet .aspx.

CSS- og ASPX-filer skal placeres i en bestemt mappe, så programmet Internet Information Services (IIS) kan indlæse dem. Det kan være nyttigt at definere forskellige CSS-filer, hvis du kører mobilenhedsfunktionen i forskellige typer browsere eller forskellige typer hardware, der kræver kontrol af forskellige layout. Simple indstillinger som baggrundsfarven, skrifttypen og skriftstørrelsen for tekst, og bredden og funktionen af knapperne, kan nemt styres ved en anden brug af CSS-filer. ASPX-filen bruges til at vise mobilwebstedet på serversiden ASP.NET-programmet. Filen styrer, hvordan den overordnede struktur i HTML-koden er opstillet. Det er en god idé at tilpasse denne funktion, hvis du har alvorlige strukturelle problemer med HTML og JavaScript, og du skal ændre denne kode til bestemte enheder. For at knytte HTML-kontrolelementerne på mobilenhedssiden til tastaturgenveje skal du tildele numeriske koder for nøglerne på siden **Mobilenhedens skærmindstillinger** i feltet **Tastaturgenvej**. Du kan bruge menuen **Få vist koder til tastaturgenveje** på mobilenheden for at finde de numeriske tegnkoder. Bemærk, at tilknytningerne kan være forskellig afhængig af den hardware, der bruges. Du skal bruge følgende syntaks for at oprette tilknytning:

&lt;navn på kontrolelement&gt; (&lt;navn på tast&gt;) = &lt;Kode til tast&gt;

Her er en forklaring på delene af syntaksen:

-   **&lt;navn på kontrolelement&gt;** – Navnet på kontrolelementet, for eksempel en knap, der gengives i HTML-format.
-   **(&lt;navn på tast&gt;)** – Navnet på tast på tastaturet, du vil oprette en genvej til.
-   **&lt;Kode til tast&gt;** – Den numeriske tegnkode for den tast, du vil bruge som genvejstasten.

Her er et eksempel:

Annuller (Esc) = 27: Fuld (F2) = 113

På alle sider, der indeholder en knap for **Annuller** , har knappen denne tekst:

**(Esc) Annuller**

Hvis du trykker på tasten Esc på tastaturet, aktiveres knappen **Annuller**. Hvis du vil anvende indstillingerne for typografi og tastaturgenveje på en bestemt enhed, skal du oprette en tilknytning i feltet **Kriterier**. Du skal bruge et regulært .NET-udtryk for at oprette tilknytningen, og udtrykket skal bestå af tre sektioner, der adskilles af en lodret streg (|), som vist her:

Request.UserHostAddress=&lt;brugerhostadresse&gt;|HostName=&lt;brugerhostnavn&gt;|Request.UserAgent=&lt;brugeragent&gt;

Her er en forklaring på delene af udtrykket:

-   **&lt;brugerhostadresse&gt;** – Et regulært .NET-udtryk, der matcher anmoderens IP-adresse.
-   **&lt;brugerhostnavn&gt;** – Et regulært .NET-udtryk, der matcher anmoderens netværksnavn.
-   **&lt;brugeragent&gt;** – Et regulært .NET-udtryk, der matcher identifikationen på den browser, som anmoderen bruger.

Følgende eksempel giver mulighed for, at Internet Explorer 8 kan bruges.

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

Du kan bruge menuen **Få vist serverkonfigurationen til skærmindstillinger** på mobilenheden til at finde oplysninger om opsætningen.

## <a name="define-text-colors-for-messages"></a>Definere tekstfarver for meddelelser
Du kan bruge siden **Tekstfarver for mobilenhed** til at kontrollere de forskellige farver, der bruges i systemgenererede beskeder, f.eks. fejlbeskeder. Tekstfarve kan for eksempel angive formål eller alvoren af meddelelsen. Følgende typer af beskeder vises.

| Meddelelsestype | Beskrivelse                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standard      | Standardmeddelelserne bruger standardfarveindstillingerne for alle meddelelser, som defineret af CSS-filen for Warehouse Mobile Device Portal.                                                   |
| Fejl        | Fejlmeddelelser angiver et problem, som brugeren skal løse, før han eller hun kan fortsætte.                                                                                             |
| Succes      | Meddelelse bekræfter, at en handling er fuldført.                                                                                                                                |
| Advarsel      | Advarselsmeddelelser underretter arbejderen om, at der er et problem, eller, at der kunne være et problem, hvis arbejderen fortsætter. Arbejderen skal dog ikke løse problemet for at fortsætte. |

Klik ind på paletten, eller indtast en hexadecimal farvekode for at vælge farven på siden **Vælg farve**.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Definere datoformatet til brug på mobilenheder
Du kan udvide listen over godkendte datoformater for hver enkelt installation. Denne egenskab kan være brugbar, hvis du f.eks. vil angive et format, der gør det lettere for en arbejder at angive datoer på en mobilenhed. Standardformatet bestemmes af brugerens standardsprog, der er angivet i feltet **Sprog** på siden **Brugerindstillinger**. (Samme side bruges også til at knytte en medarbejder til et bestemt arbejdsbruger for et lagersted). **Bemærk!** Warehouse Mobile Devices Portal bruger ikke indstillingen i feltet **Format for dato, klokkeslæt og tal** på siden **Præferencer for sprog om område**. Hvis du vil ændre et datoformat, skal du være fortrolig med regulære udtryk i Microsoft .NET Framework. Yderligere oplysninger finder du i [Regulære udtryk i .NET Framework](http://go.microsoft.com/fwlink/?LinkId=391260). Hvis du vil definere datoformater,skal du redigere filen Dates.ini, der findes på Content\\Settings\\Dates.ini på Warehouse Mobile Devices Portal-serveren. Denne fil bruger regulære .NET-udtryk til at specificere datoformatet. Det regulære udtryk skal indeholde underordnede udtryk, der opretter navngivne grupper for dag, måned og år (DDMMYY), sådan som det vises i følgende eksempel:

^(?&lt;dag&gt;\\d{2})(?&lt;måned&gt;\\d{2})(?&lt;år&gt;\\d {2})$

Hver underordnet udtryk kræver en til to cifre for dagen og måneden og et til fire cifre for året. F.eks. definerer følgende underordnede udtryk en navngivet gruppe for et år, og kræver mindst to eller maksimalt fire cifre:

(?&lt;år&gt;\\d{2,4})

Du kan angive mere end ét udtryk i den samme fil. Hvert udtryk skal være på en separat linje. Det første udtryk, der er afstemt, bruges til at fortolke datoen.

<a name="see-also"></a>Se også
--------

[Konfiguration af mobilenheder til lagerstedsarbejde](configure-mobile-devices-warehouse.md)




