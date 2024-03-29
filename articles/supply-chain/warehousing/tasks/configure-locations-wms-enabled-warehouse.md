---
title: Konfigurere lokationer på et WMS-aktiveret lagersted
description: Denne vejledning viser, hvordan du konfigurerer lokationsopsætningen for et nyt WMS-aktiveret lagersted (et lagersted, der bruger avancerede lokationsstyringsprocesser (WMS)).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cce7ea0c06938d2ce038853a262f843ec76fe4c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219652"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Konfigurere placeringer på et WMS-aktiveret lagersted

[!include [banner](../../includes/banner.md)]

Denne vejledning viser, hvordan du konfigurerer lokationsopsætningen for et nyt WMS-aktiveret lagersted (et lagersted, der bruger avancerede lokationsstyringsprocesser (WMS)). Processen udføres typisk af en lagerchef. Du kan køre denne guide i demofirmaet USMF eller på dine egne data. En forudsætning er, at du har konfigureret mindst ét websted.


## <a name="create-a-new-warehouse"></a>Opret et nyt lagersted
1. Gå til **Navigationsrude > Moduler > Lagerstyring > Opsætning > Lageropdeling > Lagersteder**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Lagersted**.
4. Skriv en værdi i feltet **Navn**.
5. Vælg eller angiv en eksisterende lokationsværdi i feltet **Websted**.
6. Udvid afsnittet **Lagersted**.
7. Angiv indstillingen **Brug lagerstedsstyringsprocesser** til Ja. Denne indstilling giver dig mulighed at køre lokationsstyringsprocesser (WMS) ved hjælp af lagerstedsarbejde og mobilenheder.
8. Luk siden.

## <a name="define-a-location-format"></a>Definere et lokalitetsformat
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Lokationsformater**. Lokationsformater er et navngivningssystem, der bruges til at oprette entydige og konsekvent navne for de forskellige positioner for lokationsbeholder på et lagersted. Det kan være nyttigt at bruge separatorer som en del af placeringsformatet for at gøre det nemmere at identificere komponenter på lokationen som gangnummeret. I dette eksempel skal vi oprette et navn med fire komponenter. Disse kan for eksempel være gang, reol, hylde og placering.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Lokationsformat**.
4. Skriv en værdi i feltet **Navn**.
5. Skriv en værdi i feltet **Segmentbeskrivelse**. Dette beskriver, hvad den første komponent i lokationsnavnet repræsenterer. Det kan for eksempel være 'Gang'.
6. Angiv et tal i feltet **Længde**. Dette bestemmer, hvor mange tegn denne del af lokationsnavnet må indeholde. Bemærk, at summen af alle komponenterne i navnet, herunder separatorer, ikke må overstige 10 tegn.    
7. Skriv en værdi i feltet **Separator**. Dette bestemmer, hvilket tegn eller symbol der bruges mellem den første og anden komponent i navnet.  
8. Klik på **Ny** i afsnittet **Oplysninger**.
9. Skriv en værdi i feltet **Segmentbeskrivelse**.
10. Angiv et tal i feltet **Længde**.
11. Skriv en værdi i feltet **Separator**.
12. Klik på **Ny** i afsnittet **Oplysninger**.
13. Skriv en værdi i feltet **Segmentbeskrivelse**.
14. Angiv et tal i feltet **Længde**.
15. Skriv en værdi i feltet **Separator**.
16. Klik på **Ny** i afsnittet **Oplysninger**.
17. Skriv en værdi i feltet **Segmentbeskrivelse**.
18. Angiv et tal i feltet **Længde**.
19. Klik på **Gem**.
20. Luk siden.

## <a name="define-location-types"></a>Definere lokalitetstyper
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Lokationstyper**. Lokationstyper kan bruges til at filtrere indstillinger for at styre de forskellige lagerstedsstyringsprocesser. Som minimum skal du oprette midlertidige og endelige afsendelseslokationstyper for at definere styring af udgående lagerprocesser. 
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Lokalitetstype**.
4. Indtast en værdi i feltet **Beskrivelse**.
5. Luk siden.

## <a name="define-location-profile"></a>Definere lokalitetsprofil
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Lokationsprofiler**. Definitionen af lokationsprofiler er meget vigtigt. Grupperede lokaliteters kapacitet kan styres her, og de politikker, der er relateret til, hvilket lager der gemmes, og hvordan det gemmes. Lokationprofiler kan bruges til at filtrere indstillinger for at styre de forskellige lagerstedsstyringsprocesser. Som minimum skal du oprette en brugerlokationsprofil for at aktivere WMS.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Id for lokationsprofil**.
4. Skriv en værdi i feltet **Navn**.
5. Klik på rullelisten i feltet **Lokationsformat** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet **Lokationstype** for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Markér eller fjern markeringen i afkrydsningsfeltet **Tillad blandede lagerstatusser**. Aktiver denne indstilling, hvis du vil tillade blandede lagerstatusværdier på de lokaliteter, der skal grupperes efter denne lokationsprofil. 
12. Markér eller fjern markeringen i afkrydsningsfeltet **Tilsidesæt regler for batchdage**. Aktiver denne indstilling for at tilsidesætte reglen for, hvor mange dage lagerbatchudløbsdatoer kan variere, for at tillade blanding af lagerbatches, der ikke overholder denne regel.  
13. Marker eller fjern markeringen i afkrydsningsfeltet **Tillad cyklusoptælling**. Aktiver denne indstilling, hvis du vil tillade behandling af cyklusoptælling på alle de lokaliteter, der skal grupperes efter denne lokationsprofil. 
14. Vis eller skjul sektionen **Dimensioner**. Fanen Dimensioner giver dig mulighed for at definere parametre og metoder, så der kan foretages aktivere nøjagtige beregninger af belastkapacitet inden for hver af lokaliteterne.  
15. Luk siden.

## <a name="enable-warehouse-management-parameters"></a>Aktivér parametre for lagerstedsstyring
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Parametre til lokationsstyring**. For at kunne behandle lagerstedsarbejde skal du angive parametre for brugerlokationsprofilen, den midlertidige lokationstype og den endelige afsendelseslokationstype. Så snart, den udgående proces afsluttes på den endelige afsendelseslokationstype, du definerer, opdateres de relaterede udgående transaktioner til "Plukket".
2. Udvid sektionen **Lokationsprofiler**.
3. Klik på rullelisten i feltet **Brugerlokation** for at åbne opslaget.
4. Klik op linket i den valgte række på listen.
5. Udvid sektionen **Lokationstyper**.
6. Klik på rullelisten i feltet **Midlertidig lokalitetstype** for at åbne opslaget.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet **Endelig afsendelseslokationstype** for at åbne opslaget.
9. Klik op linket i den valgte række på listen.
10. Luk siden.

## <a name="define-warehouse-zone-groups"></a>Definere lagerstedszonegrupper
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Lagerstedszonegrupper**. Lagerstedszoner kan bruges som filtre for indstillinger for at styre de forskellige lagerstedsstyringsprocesser. Du skal oprette en zonegruppe, før du kan definere en zone.   
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Id for zonegruppe**.
4. Skriv en værdi i feltet **Navn på zonegruppe**.
5. Luk siden.

## <a name="define-warehouse-zones"></a>Definere Lagerstedszoner
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Zoner**.
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Zone-id**.
4. Skriv en værdi i feltet **Navn på zone**.
5. Klik på rullelisten i feltet **Id for zonegruppe** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Luk siden.

## <a name="create-locations-using-the-location-setup-wizard"></a>Oprette lokationer ved hjælp af guiden Konfiguration af lokalitet
1. Gå til **Navigationsrude > Moduler > Lokationsstyring > Opsætning > Lagersted > Guiden Konfiguration af lokation**.
2. Klik på rullelisten i feltet **Lagersted** for at åbne opslaget.
3. Find og vælg den ønskede post på listen.
4. Klik op linket i den valgte række på listen.
5. Klik på rullelisten i feltet **Zone-id** for at åbne opslaget.
6. Find og vælg den ønskede post på listen.
7. Klik op linket i den valgte række på listen.
8. Klik på rullelisten i feltet **Id for lokalitetsprofil** for at åbne opslaget.
9. Find og vælg den ønskede post på listen.
10. Klik op linket i den valgte række på listen.
11. Markér den valgte række på listen.
12. Indtast et tal i feltet **Fra nummer**. Felterne Fra nummer og Til nummer definerer, hvor mange lokaliteter, der bliver oprettet. Hvis du for eksempel angiver Fra nummer til 1 og Til nummer til 3 for alle fire linjer i lokationsformatet, oprettes 81 lokaliteter (3x3x3x3).   
13. Indtast et tal i feltet **Til nummer**.
14. Find og vælg den ønskede post på listen.
15. Indtast et tal i feltet **Fra nummer**.
16. Indtast et tal i feltet **Til nummer**.
17. Find og vælg den ønskede post på listen.
18. Indtast et tal i feltet **Fra nummer**.
19. Indtast et tal i feltet **Til nummer**.
20. Find og vælg den ønskede post på listen.
21. Indtast et tal i feltet **Fra nummer**.
22. Indtast et tal i feltet **Til nummer**.
23. Klik på Opret.

## <a name="create-locations-manually"></a>Oprette lokaliteter manuelt
1. Gå til **Lokationsstyring > Konfiguration > Lagersted > Lokationer**. Det er nemt manuelt at oprette lokaliteter i lagersted. Lokationsnavnet og id for lokationsprofil er obligatoriske værdier. 
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Lagersted**.
4. Skriv en værdi i feltet **Lokation**. Bemærk, at du opretter en ny lokalitet her, så du skal skrive et nyt entydigt navn i stedet for at vælge et eksisterende navn.
5. Skriv en værdi i feltet **Id for lokationsprofil**.
6. Luk siden.

## <a name="define-pack-size-categories"></a>Definere Kategorier af pakkestørrelse
1. Gå til **Lokationsstyring > Opsætning > Lagersted > Kategorier af pakkestørrelse**. Kategorier af pakkestørrelse kan bruges til gruppering af varer, der har samme fysiske pakkestørrelser. I dette eksempel bruges pakkestørrelsekategorien til at styre kapaciteten på plukkelokaliteterne inden for en bestemt zone på lagerstedet. Bemærk, at pakkestørrelsekategori-id'et skal tildeles til det frigivne produkt for at kunne bruges som en del af behandlingen af grænser for lokationslagring.  
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Kategori-id for pakkestørrelse**.
4. Skriv en værdi i feltet **Kategorinavn på pakkestørrelse**.
5. Luk siden.

## <a name="define-location-stocking-limits"></a>Definere grænser for lokalitetslagring
1. Gå til **Lokationsstyring > Konfiguration > Lagersted > Grænser for lokationslagring**. Grænser for lokationslagring hjælper med til at sikre, at arbejdet ikke oprettes for at anmode om, at lageret skal placeres på en lokalitet, der ikke har den fysiske kapacitet til rumme lageret.  
2. Klik på **Ny**.
3. Skriv en værdi i feltet **Lagersted**.
4. Skriv en værdi i feltet **Id for lokationsprofil**.
5. Skriv en værdi i feltet **Kategori-id for pakkestørrelse**.
6. Angiv et tal i feltet **Antal**.
7. Klik på **Gem**.
8. Luk siden.

## <a name="define-fixed-picking-locations"></a>Definere faste plukpladser
1. Gå til **Lokationsstyring > Opsætning > Lagersted > Faste lokationer**. Du kan definere de lokaliteter, der skal bruges pr. produkt eller produktvariant. Det er muligt at oprette flere faste lokaliteter til det samme produkt inden for det samme lager.     
2. Klik på **Ny**.
3. Indtast en værdi i feltet **Varenummer**.
4. Skriv en værdi i feltet **Lagersted**.
5. Klik på rullelisten i feltet **Lokation** for at åbne opslaget.
6. Klik op linket i den valgte række på listen.
7. Luk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
