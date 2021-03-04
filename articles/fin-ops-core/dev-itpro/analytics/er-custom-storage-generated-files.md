---
title: Angive brugerdefinerede lagersteder til oprettede dokumenter
description: I dette emne beskrives, hvordan du kan udvide listen over placering til lagring af dokumenter, som genereres ved elektronisk rapportering (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 362ac7f10cc61e26be89dfbae0e84745d42588a3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680752"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>Angive brugerdefinerede lagersteder til oprettede dokumenter

[!include[banner](../includes/banner.md)]

Med API'en (application programming interface) i den elektroniske rapporteringsstruktur (ER) kan du udvide listen over lagerplaceringer til dokumenter, som ER-formater genererer. Dette emne forklarer, hvordan du kan føje en brugerdefineret lagerplacering til genererede dokumenter ved at delegere opgaven til oprettelse af ER-destinationer til standarddestinationsfabrikken og derefter implementere en brugerdefineret klasse, der har sin egen destinationslogik.

## <a name="prerequisites"></a>Forudsætninger

Installer en topologi, der understøtter fortløbende build. Du kan finde flere oplysninger under [Installere topologier, der understøtter fortløbende build og automatisering af test](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation). Du skal også have adgang til denne topologi for en af følgende roller:

- Udvikler til elektronisk rapportering
- Funktionel konsulent i elektronisk rapportering
- Systemadministrator

Du skal også have adgang til udviklingsmiljøet for denne topologi.

Alle opgaverne i dette emne kan fuldføres i **USMF**-firmaet.

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>Importere ER-formatet Rul anlægsaktiver fremad

Hvis du vil generere de dokumenter, som du planlægger at tilføje en brugerdefineret lagerplacering for, skal du [importere](er-download-configurations-global-repo.md) konfigurationen af ER-formatet **Rul anlægsaktiver fremad** til den aktuelle topologi.

![Siden Konfigurationslager](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>Køre rapporten Rul anlægsaktiver fremad

1. Gå til **Anlægsaktiver** \> **Forespørgsler og rapporter** \> **Transaktionsrapporter** \> **Rul anlægsaktiver fremad**.
2. I feltet **Fra dato** skal du indtaste **01-01-2017** (1. januar 2017).
3. I feltet **Til dato** skal du indtaste **31-01-2017** (31. januar 2017).
4. Vælg **Regnskabsvaluta** i feltet **Valuta**.
5. Gå til feltet **Formattilknytning**, og vælg **Rul anlægsaktiver fremad**.
6. Vælg **OK**.

![Kørselsdialogboks for rapporten Rul anlægsaktiver fremad](./media/er-custom-storage-generated-files-runtime-dialog.png)

I Microsoft Excel skal du gennemse det udgående dokument, der er oprettet, og som kan hentes. Denne funktionsmåde er [standardfunktionsmåden](electronic-reporting-destinations.md#default-behavior) for et ER-format, der ikke er konfigureret [destinationer](electronic-reporting-destinations.md) for, og som kører i interaktiv tilstand.

## <a name="review-the-source-code"></a>Gennemse kildekoden

Gennemse koden for metoden `generateReportByGER()` i klassen `AssetRollForwardService`. Bemærk, at metoden `Run()` bruges til at kalde ER-strukturen og generere rapporten **Rul anlægsaktiver fremad**.

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a>Ændre kildekoden

1. I Visual Studio-projektet skal du tilføje en ny klasse (`AssetRollForwardDestination` i dette eksempel) og skrive kode for at implementere den brugerdefinerede destination for de **Rul anlægsaktiver fremad**-rapporter, der genereres.

    - Metoden `new()` er beregnet til at hente det oprindelige ER-destinationsobjekt og den programlogikbaserede parameter, der angiver den brugerdefinerede placering, hvor genererede rapporter skal gemmes. I dette eksempel er den brugerdefinerede placering navnet på en mappe i det lokale filsystem på den server, der kører AOS-tjenesten (applikationsobjektserver).
    - Metoden `saveFile()` er udviklet til at gemme et genereret dokument i en mappe i det lokale filsystem på den server, der kører AOS-tjenesten.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. I Visual Studio-projektet skal du tilføje en ny klasse (`AssetRollForwardDestinationFactory` i dette eksempel) og skrive kode for at oprette en brugerdefineret destinationsfabrik, der uddelegerer oprettelsen af en destination til standarddestinationsfabrikken, og for at ombryde en destinationsfil med din egen destination.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. Rediger den eksisterende `AssetRollForwardService`-klasse, og skriv kode for at oprette en brugerdefineret destinationsfabrik for rapportkørslen. Bemærk, at når der er oprettet en brugerdefineret destinationsfabrik, overføres den applikationsbaserede parameter, der angiver en destinationsmappe. På denne måde bruges denne destinationsmappe til lagring af genererede filer.

    > [!NOTE] 
    > Kontroller, at den angivne mappe (**c:\\0** i dette eksempel) findes i det lokale filsystem på den server, der kører AOS-tjenesten. Ellers udløses der en [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1)-undtagelse ved kørsel.

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. Gendan dit projekt.

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>Køre rapporten Rul anlægsaktiver fremad igen

1. Gå til **Anlægsaktiver** \> **Forespørgsler og rapporter** \> **Transaktionsrapporter** \> **Rul anlægsaktiver fremad**.
2. Gå til feltet **Fra dato**, og indtast **01-01-2017**.
3. Gå til feltet **Til dato**, og indtast **31-01-2017**.
4. Vælg **Regnskabsvaluta** i feltet **Valuta**.
5. Gå til feltet **Formattilknytning**, og vælg **Rul anlægsaktiver fremad**.
6. Vælg **OK**.
7. Gennemse den lokale **C:\\0**-mappe for at søge efter den genererede fil.

> [!NOTE]
> Da `originDestination`-objektet ikke bruges i `AssetRollForwardDestination`-objektet i dette eksempel, ignoreres konfigurationerne for ER-formatets [destinationer](electronic-reporting-destinations.md) under kørsel.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Destinationer for elektronisk rapportering (ER)](electronic-reporting-destinations.md)
- [Startside for udvidelsesmuligheder](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]