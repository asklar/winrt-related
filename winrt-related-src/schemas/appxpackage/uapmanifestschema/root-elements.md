---
description: Summarizes the allowed hierarchies for the app package manifest for Windows 10 apps schema.
Search.Product: eADQiWindows 10XVcnh
title: Element Hierarchy (Windows 10 package schema)
ms.assetid: 5dfced88-48fd-4bf6-963c-7ab090b3e26e
keywords: windows 10, uwp, schema, package manifest
ms.topic: reference
ms.date: 04/19/2019
ms.custom: 19H1
---

# Element Hierarchy (package schema for Windows 10)


The following list summarizes the allowed hierarchies for this schema, starting with the outermost (document) element at the top.

-   [**Package**](element-package.md)
    -   [**Identity**](element-identity.md)
    -   [**mp:PhoneIdentity**](element-mp-phoneidentity.md)
    -   [**Properties**](element-properties.md)
        -   [**Framework**](element-framework.md)
        -   [**DisplayName**](element-displayname.md)
        -   [**PublisherDisplayName**](element-publisherdisplayname.md)
        -   [**Description**](element-description.md)
        -   [**Logo**](element-logo.md)
        -   [**ResourcePackage**](element-resourcepackage.md)
        -   [**uap:SupportedUsers**](element-uap-supportedusers.md)
        -   [**uap6:AllowExecution**](element-uap6-allowexecution.md)
        -   [**desktop6:FileSystemWriteVirtualization**](element-desktop6-filesystemwritevirtualization.md)
        -   [**desktop6:RegistryWriteVirtualization**](element-desktop6-registrywritevirtualization.md)
        -   [**rescap6:ModificationPackage**](element-rescap6-modificationpackage.md)
        -   [**uap10:AllowExternalContent**](element-uap10-allowexternalcontent.md)
        -   [**uap10:PackageIntegrity**](element-uap10-packageintegrity.md)
            -   [**uap10:Content**](element-uap10-content.md)
    -   [**Resources**](element-resources.md)
        -   [**Resource**](element-resource.md)
    -   [**Dependencies**](element-dependencies.md)
        -   [**TargetDeviceFamily**](element-targetdevicefamily.md)
        -   [**PackageDependency**](element-packagedependency.md)
        -   [**uap3:MainPackageDependency**](element-uap3-mainpackagedependency-manual.md)
        -   [**uap5:DriverDependency**](element-uap5-driverdependency.md)
        -   [**uap7:OSPackageDependency**](element-uap7-ospackagedependency.md)
        -   [**uap10:HostRuntimeDependency**](element-uap10-hostruntimedependency.md)
        -   [**win32dependencies:ExternalDependency**](element-win32dependencies-externaldependency.md)
    -   [**Capabilities**](element-capabilities.md)
        -   [**Capability**](element-capability.md)
        -   [**uap:Capability**](element-uap-capability.md)
        -   [**uap3:Capability**](element-uap3-capability-manual.md)
        -   [**uap4:CustomCapability**](element-uap4-customcapability.md)
        -   [**uap6:Capability**](element-uap6-capability.md)
        -   [**uap7:Capability**](element-uap7-capability.md)        
        -   [**DeviceCapability**](element-devicecapability.md)
            -   [**Device**](element-device.md)
                -   [**Function**](element-function.md)
    -   [**Extensions**](element-extensions.md)
        -   [**desktop2:Extension**](element-desktop2-package-extension.md)
            -   [**desktop2:FirewallRules**](element-desktop2-firewallrules.md)
                -   [**desktop2:Rule**](element-desktop2-rule.md)
            -   [**desktop2:DesktopEventLogging**](element-desktop2-desktopeventlogging.md)
                -   [**desktop2:EventMessageFiles**](element-desktop2-eventmessagefiles.md)
                    -   [**desktop2:File**](element-desktop2-file.md)
                -   [**desktop2:TypesSupported**](element-desktop2-typessupported.md)
                    -   [**desktop2:TypeSupported**](element-desktop2-typesupported.md)
        -   [**desktop6:Extension**](element-desktop6-package-extension.md)
            -   [**desktop6:MutablePackageDirectories**](element-desktop6-mutablepackagedirectories.md)
                -   [**desktop6:MutablePackageDirectory**](element-desktop6-mutablepackagedirectory.md)
            -   [**desktop6:CustomInstall**](element-desktop6-custominstall.md)
                -   [**desktop6:InstallActions**](element-desktop6-installactions.md)
                    -   [**desktop6:InstallAction**](element-desktop6-installaction.md)
                -   [**desktop6:RepairActions**](element-desktop6-repairactions.md)
                    -   [**desktop6:RepairAction**](element-desktop6-repairaction.md)
                -   [**desktop6:UninstallActions**](element-desktop6-uninstallactions.md)
                    -   [**desktop6:UninstallAction**](element-desktop6-uninstallaction.md)
        -   [**desktop7:Extension**](element-desktop7-package-extension.md)
            - [**desktop7:ShadowCopyExcludeFiles**](element-desktop7-shadowcopyexcludefiles.md)
                - [**desktop7:ShadowCopyExcludeFile**](element-desktop7-shadowcopyexcludefile.md)
            - [**desktop7:ErrorReporting**](element-desktop7-errorreporting.md)
                - [**desktop7:RuntimeExceptionHelperModule**](element-desktop7-runtimeexceptionhelpermodule.md)
        -   [**Extension**](element-extension.md)
            -   [**com:ComInterface**](element-com-package-cominterface.md)
                -   [**com:ProxyStub**](element-com-package-proxystub.md)
                    -   [**com2:ProxyStubDll**](element-com2-package-proxystubdll.md)
                -   [**com:Interface**](element-com-package-interface.md)
                    -   [**com:TypeLib**](element-com-package-interface-typelib.md)
                -   [**com:TypeLib**](element-com-package-typelib.md)
                    -   [**com:Version**](element-com-package-version.md)
                        -   [**com:Win32Path**](element-com-package-win32path.md)
                        -   [**com:Win64Path**](element-com-package-win64path.md)
            -   [**InProcessServer**](element-inprocessserver.md)
                -   [**Path**](element-path.md)
                -   [**ActivatableClass**](element-activatableclass.md)
                    -   [**ActivatableClassAttribute**](element-activatableclassattribute.md)
            -   [**OutOfProcessServer**](element-outofprocessserver.md)
                -   [**Path**](element-1-path.md)
                -   [**Arguments**](element-arguments.md)
                -   [**Instancing**](element-instancing.md)
                -   [**ActivatableClass**](element-1-activatableclass.md)
                    -   [**ActivatableClassAttribute**](element-1-activatableclassattribute.md)
            -   [**ProxyStub**](element-proxystub.md)
                -   [**Path**](element-2-path.md)
                -   [**Interface**](element-interface.md)
            -   [**Certificates**](element-certificates.md)
                -   [**Certificate**](element-certificate.md)
                -   [**TrustFlags**](element-trustflags.md)
                -   [**SelectionCriteria**](element-selectioncriteria.md)
            -   [**PublisherCacheFolders**](element-publishercachefolders.md)
                -   [**Folder**](element-folder.md)
            -   [**uap6:LoaderSearchPathOverride**](element-uap6-LoaderSearchPathOverride.md)
                -   [**uap6:LoaderSearchPathEntry**](element-uap6-LoaderSearchPathEntry.md)
        -   [**uap7:Extension**](element-uap7-extension.md)  
            -   [**uap7:SharedFonts**](element-uap7-sharedfonts.md)
            -   [**uap7:EnterpriseDataProtection**](element-uap7-EnterpriseDataProtection.md)
    -   [**Applications**](element-applications.md)
        -   [**Application**](element-application.md)
            -   [**uap:VisualElements**](element-uap-visualelements.md)
                -   [**uap:DefaultTile**](element-uap-defaulttile.md)
                    -   [**uap:TileUpdate**](element-uap-tileupdate.md)
                    -   [**uap:ShowNameOnTiles**](element-uap-shownameontiles.md)
                        -   [**uap:ShowOn**](element-uap-showon.md)
                    -   [**uap5:MixedRealityModel**](element-uap5-mixedrealitymodel.md)
                        -   [**uap6:SpatialBoundingBox**](element-uap6-SpatialBoundingBox.md)
                -   [**uap:LockScreen**](element-uap-lockscreen.md)
                -   [**uap:SplashScreen**](element-uap-splashscreen.md)
                -   [**uap:InitialRotationPreference**](element-uap-initialrotationpreference.md)
                    -   [**uap:Rotation**](element-uap-rotation.md)
            -   [**uap:ApplicationContentUriRules**](element-uap-applicationcontenturirules.md)
                -   [**uap:Rule**](element-uap-rule.md)
            -   [**uap3:VisualElements**](element-uap3-visualelements-manual.md) 
            -   [**uap7:Properties**](element-uap7-properties.md)
                -   [**uap7:ImportRedirectionTable**](element-uap7-importredirectiontable.md)              
            -   [**Extensions**](element-1-extensions.md)
                -   [**Extension**](element-1-extension.md)
                    -   [**BackgroundTasks**](element-backgroundtasks.md)
                        -   [**Task**](element-task.md)
                        -   [**uap:Task**](element-uap-task.md)
                -   [**com:Extension**](element-com-extension.md)
                    -   [**com:ComInterface**](element-com-cominterface.md)
                        -   [**com:ProxyStub**](element-com-proxystub.md)
                            -   [**com2:ProxyStubDll**](element-com2-proxystubdll.md)
                        -   [**com:Interface**](element-com-interface.md)
                            -   [**TypeLib**](element-com-interface-typelib.md)
                        -   [**com:TypeLib**](element-com-typelib.md)
                            -   [**com:Version**](element-com-version.md)
                                -   [**com:Win32Path**](element-com-win32path.md)
                                -   [**com:Win64Path**](element-com-win64path.md)
                    -   [**com:ComServer**](element-com-comserver.md)
                        -   [**com:ExeServer**](element-com-exeserver.md)
                            -   [**com:Class**](element-com-exeserver-class.md)
                                -   [**com:ImplementedCategories**](element-com-exe-implementedcategories.md)
                                    -   [**com:ImplementedCategory**](element-com-exe-implementedcategory.md)
                                -   [**com:Conversion**](element-com-exe-conversion.md)
                                    -   [**Readable**](element-com-exe-readable.md)
                                        -   [**Format**](element-com-exe-rformat.md)
                                    -   [**ReadWritable**](element-com-exe-readwritable.md)
                                        -   [**Format**](element-com-exe-rwformat.md)
                                -   [**com:DataFormats**](element-com-exe-dataformats.md)
                                    -   [**com:DataFormat**](element-com-exe-dataformat.md)
                                -   [**com:MiscStatus**](element-com-exe-miscstatus.md)
                                    -   [**com:Aspect**](element-com-exe-aspect.md)
                                -   [**com:Verbs**](element-com-exe-verbs.md)
                                    -   [**com:Verb**](element-com-exe-verb.md)
                                -   [**com:DefaultIcon**](element-com-exe-defaulticon.md)
                                -   [**com:ToolboxBitmap32**](element-com-exe-toolboxbitmap32.md)
                        -   [**com:SurrogateServer**](element-com-surrogateserver.md)
                            -   [**com:Class**](element-com-surrogateserver-class.md)
                                -   [**com:ImplementedCategories**](element-com-surrogate-implementedcategories.md)
                                    -   [**com:ImplementedCategory**](element-com-surrogate-implementedcategory.md)
                                -   [**com:Conversion**](element-com-surrogate-conversion.md)
                                    -   [**Readable**](element-com-surrogate-readable.md)
                                        -   [**Format**](element-com-surrogate-rformat.md)
                                    -   [**ReadWritable**](element-com-surrogate-readwritable.md)
                                        -   [**Format**](element-com-surrogate-rwformat.md)
                                -   [**com:DataFormats**](element-com-surrogate-dataformats.md)
                                    -   [**com:DataFormat**](element-com-surrogate-dataformat.md)
                                -   [**com:MiscStatus**](element-com-surrogate-miscstatus.md)
                                    -   [**com:Aspect**](element-com-surrogate-aspect.md)
                                -   [**com:Verbs**](element-com-surrogate-verbs.md)
                                    -   [**com:Verb**](element-com-surrogate-verb.md)
                                -   [**com:DefaultIcon**](element-com-surrogate-defaulticon.md)
                                -   [**com:ToolboxBitmap32**](element-com-surrogate-toolboxbitmap32.md)
                        -   [**com:ProgId**](element-com-progid.md)
                        -   [**com:TreatAsClass**](element-com-treatasclass.md)
                -   [**com2:Extension**](element-com2-extension.md)
                    -   [**com2:ComServer**](element-com2-comserver.md)
                        -   [**com3:ServiceServer**](element-com3-serviceserver.md)
                            -   [**com3:Class**](element-com3-class.md)
                        -   [**com3:ExeServer**](element-com3-exeserver.md)
                        -   [**com3:SurrogateServer**](element-com3-surrogateserver.md)
                        -   [**com3:TreatAsClass**](element-com3-treatasclass.md)
                        -   [**com3:ProgId**](element-com3-progid.md)
                    -   [**com2:ComInterface**](element-com2-cominterface.md)
                -   [**desktop:Extension**](element-desktop-extension.md)
                    -   [**desktop:FullTrustProcess**](element-desktop-fulltrustprocess.md)
                        -   [**desktop:ParameterGroup**](element-desktop-parametergroup.md)
                -   [**desktop2:Extension**](element-desktop2-extension.md)
                    -   [**desktop2:AppPrinter**](element-desktop2-appprinter.md)
                    -   [**desktop2:SearchFilterHandler**](element-desktop2-searchfilterhandler.md)
                        -   [**desktop2:FilterExtension**](element-desktop2-filterextension.md)
                    -   [**desktop2:SearchPropertyHandler**](element-desktop2-searchpropertyhandler.md)
                -   [**desktop3:Extension**](element-desktop3-extension.md)
                    -   [**desktop3:AutoPlayHandler**](element-desktop3-autoplayhandler.md)
                        -   [**desktop3:InvokeAction**](element-desktop3-invokeaction.md)
                            -   [**desktop3:Content**](element-desktop3-content.md)
                            -   [**desktop3:Device**](element-desktop3-device.md)
                    -   [**desktop3:CloudFiles**](element-desktop3-cloudfiles.md)
                        -   [**desktop3:CustomStateHandler**](element-desktop3-customstatehandler.md)
                        -   [**desktop3:ThumbnailProviderHandler**](element-desktop3-thumbnailproviderhandler.md)
                        -   [**desktop3:ExtendedPropertyHandler**](element-desktop3-ExtendedPropertyHandler.md)
                        -   [**desktop3:BannersHandler**](element-desktop3-BannersHandler.md)
                        -   [**desktop3:CloudFilesContextMenus**](element-desktop3-CloudFilesContextMenus.md)
                            -   [**desktop3:Verb**](element-desktop3-verb.md)
                        -   [**desktop4:ContentUriSource**](element-desktop4-ContentUriSource.md)
                        -   [**desktop4:DesktopIconOverlayHandlers**](element-desktop4-DesktopIconOverlayHandlers.md)
                            -   [**desktop4:DesktopIconOverlayHandler**](element-desktop4-DesktopIconOverlayHandler.md)
                -   [**desktop4:Extension**](element-desktop4-extension.md)
                    -   [**desktop4:FileExplorerContextMenus**](element-desktop4-fileexplorercontextmenus.md)
                        -   [**desktop4:ItemType**](element-desktop4-itemtype.md)
                            -   [**desktop4:Verb**](element-desktop4-verb.md)
                        -   [**desktop5:ItemType**](element-desktop5-itemtype.md)
                            -   [**desktop5:Verb**](element-desktop5-verb.md)
                -   [**desktop6:Extension**](element-desktop6-extension.md)
                    -   [**desktop6:Service**](element-desktop6-service.md)
                        -   [**desktop6:Dependencies**](element-desktop6-dependencies.md)
                            -   [**desktop6:DependentService**](element-desktop6-dependentservice.md)
                        -   [**desktop6:TriggerEvents**](element-desktop6-triggerevents.md)
                            -   [**desktop6:TriggerCustom**](element-desktop6-triggercustom.md)
                                -   [**desktop6:StringData**](element-desktop6-stringdata.md)
                                    -   [**desktop6:DataItem**](element-desktop6-dataitem.md)
                                -   [**desktop6:BinaryData**](element-desktop6-binarydata.md)
                                -   [**desktop6:LevelData**](element-desktop6-leveldata.md)
                                -   [**desktop6:KeywordAnyData**](element-desktop6-keywordanydata.md)
                                -   [**desktop6:KeywordAllData**](element-desktop6-keywordalldata.md)
                -   [**desktop7:Extension**](element-desktop7-extension.md)
                    - [**desktop7:ApprovedShellExtension**](element-desktop7-approvedshellextension.md)
                    - [**desktop7:ControlPanelItem**](element-desktop7-controlpanelitem.md)
                        - [**desktop7:DefaultIcon**](element-desktop7-defaulticon.md)
                        - [**desktop7:LocalizedString**](element-desktop7-localizedstring.md)
                        - [**desktop7:InfoTip**](element-desktop7-infotip.md)
                    - [**desktop7:Service**](element-desktop7-service.md)
                    - [**desktop7:MailProvider**](element-desktop7-mailprovider.md)
                    - [**desktop7:Shortcut**](element-desktop7-shortcut.md)
                        - [**desktop7:AppMigrations**](element-desktop7-appmigrations.md)
                            - [**desktop7:AppMigration**](element-desktop7-appmigration.md)
                    - [**desktop7:ApplicationRegistration**](element-desktop7-applicationregistration.md)
                    - [**desktop7:DesktopAppMigration**](element-desktop7-desktopappmigration.md)
                        - - [**desktop7:DesktopApp**](element-desktop7-desktopapp.md)
                    - [**desktop7:SystemFileAssociation**](element-desktop7-systemfileassociation.md)
                    - [**desktop7:ShadowCopyExcludeFiles**](element-desktop7-shadowcopyexcludefiles.md)
                        - [**desktop7:ShadowCopyExcludeFile**](element-desktop7-shadowcopyexcludefile.md)
                    - [**desktop7:ErrorReporting**](element-desktop7-errorreporting.md)
                        - [**desktop7:RuntimeExceptionHelperModule**](element-desktop7-runtimeexceptionhelpermodule.md)
                -   [**desktop9:Extension**](element-desktop9-extension.md)
                    -   [**desktop9:FileExplorerClassicContextMenuHandler**](element-desktop9-fileexplorerclassiccontextmenuhandler.md)
                        -   [**desktop9:ExtensionHandler**](element-desktop9-extensionhandler.md)
                    -   [**desktop9:FileExplorerClassicDragDropContextMenuHandler**](element-desktop9-fileexplorerclassicdragdropcontextmenuhandler.md)
                -   [**rescap2:Extension**](element-rescap2-extension-manual.md)
                -   [**rescap3:Extension**](element-rescap3-extension.md)
                    -   [**rescap3:DesktopAppMigration**](element-rescap3-desktopappmigration.md)
                        -   [**rescap3:DesktopApp**](element-rescap3-desktopapp.md)
                -   [**rescap4:Extension**](element-rescap4-extension.md)
                    -   [**rescap4:ClassicAppCompatKeys**](element-rescap4-ClassicAppCompatKeys.md)
                        -   [**rescap4:ClassicAppCompatKey**](element-rescap4-ClassicAppCompatKey.md)
                -   [**serverpreview:Extension**](element-serverpreview-extension-manual.md)
                    -   [**serverpreview:IisModules**](element-serverpreview-iismodules-manual.md)
                        -   [**serverpreview:IisModule**](element-serverpreview-iismodule-manual.md)
                            -   [**serverpreview:SectionGroupDefinition**](element-serverpreview-sectiongroupdefinition-manual.md)
                                -   [**serverpreview:SectionDefinition**](element-serverpreview-sectiondefinition-manual.md)
                            -   [**serverpreview:SectionDefinition**](element-serverpreview-sectiondefinition-manual.md)
                            -   [**serverpreview:SectionData**](element-serverpreview-sectiondata-manual.md)
                                -   [**serverpreview:CollectionElement**](element-serverpreview-collectionelement-manual.md)
                                -   [**serverpreview:Attribute**](element-serverpreview-attribute-manual.md)
                    -   [**serverpreview:NTServices**](element-serverpreview-ntservices-manual.md)
                        -   [**serverpreview:NTService**](element-serverpreview-ntservice-manual.md)
                            -   [**serverpreview:ServiceDependencies**](element-serverpreview-servicedependencies-manual.md)
                                -   [**serverpreview:ServiceDependency**](element-serverpreview-servicedependency-manual.md)
                            -   [**serverpreview:ServiceParameters**](element-serverpreview-serviceparameters-manual.md)
                                -   [**serverpreview:ServiceParameterDword**](element-serverpreview-serviceparameterdword-manual.md)
                                -   [**serverpreview:ServiceParameterString**](element-serverpreview-serviceparameterstring-manual.md)
                                -   [**serverpreview:ServiceParameterKey**](element-serverpreview-serviceparameterkey-manual.md)
                    -   [**serverpreview:WmiProviders**](element-serverpreview-wmiproviders-manual.md)
                        -   [**serverpreview:WmiProvider**](element-serverpreview-wmiprovider-manual.md)
                            -   [**serverpreview:Mof**](element-serverpreview-mof-manual.md)
                    -   [**serverpreview:PerformanceProviders**](element-serverpreview-performanceproviders-manual.md)
                        -   [**serverpreview:PerformanceProvider**](element-serverpreview-performanceprovider-manual.md)
                    -   [**serverpreview:EventProviders**](element-serverpreview-eventproviders-manual.md)
                        -   [**serverpreview.EventProvider**](element-serverpreview-eventprovider-manual.md)
                -   [**uap:Extension**](element-uap-extension.md)
                    -   [**uap:FileTypeAssociation**](element-uap-filetypeassociation.md)
                        -   [**desktop2:DesktopPreviewHandler**](element-desktop2-DesktopPreviewHandler.md)
                        -   [**desktop2:DesktopPropertyHandler**](element-desktop2-desktoppropertyhandler.md)
                        -   [**desktop2:OleClass**](element-desktop2-oleclass.md)                                                    
                        -   [**desktop2:ThumbnailHandler**](element-desktop2-thumbnailhandler.md)
                        -   [**rescap3:MigrationProgIds**](element-rescap3-migrationprogids.md)
                            -   [**rescap3:MigrationProgId**](element-rescap3-migrationprogid.md)                        
                        -   [**uap:DisplayName**](element-uap-displayname.md)
                        -   [**uap:Logo**](element-uap-logo.md)
                        -   [**uap:InfoTip**](element-uap-infotip.md)
                        -   [**uap:EditFlags**](element-uap-editflags.md)
                        -   [**uap:SupportedFileTypes**](element-uap-supportedfiletypes.md)
                            -   [**uap:FileType**](element-uap-filetype.md)
                        -   [**uap2:SupportedVerbs**](element-uap2-supportedverbs.md)
                            -   [**uap2:Verb**](element-uap2-verb.md)
                            -   [**uap3:Verb**](element-uap3-verb.md)
                        -   [**uap4:KindMap**](element-uap4-kindmap.md)
                            -   [**uap4:Kind**](element-uap4-kind.md)
                    -   [**uap:Protocol**](element-uap-protocol.md)
                        -   [**rescap3:MigrationProgIds**](element-uap-protocol-migrationprogids.md)
                            -   [**rescap3:MigrationProgId**](element-uap-protocol-migrationprogid.md)
                        -   [**uap:Logo**](element-1-uap-logo.md)
                        -   [**uap:DisplayName**](element-1-uap-displayname.md)
                    -   [**uap:AutoPlayContent**](element-uap-autoplaycontent.md)
                        -   [**uap:LaunchAction**](element-uap-launchaction.md)
                    -   [**uap:AutoPlayDevice**](element-uap-autoplaydevice.md)
                        -   [**uap:LaunchAction**](element-1-uap-launchaction.md)
                    -   [**uap:ShareTarget**](element-uap-sharetarget.md)
                        -   [**uap:SupportedFileTypes**](element-1-uap-supportedfiletypes.md)
                            -   [**uap:FileType**](element-1-uap-filetype.md)
                            -   [**uap:SupportsAnyFileType**](element-uap-supportsanyfiletype.md)
                        -   [**uap:DataFormat**](element-uap-dataformat.md)
                    -   [**uap:FileOpenPicker**](element-uap-fileopenpicker.md)
                        -   [**uap:SupportedFileTypes**](element-2-uap-supportedfiletypes.md)
                            -   [**uap:FileType**](element-2-uap-filetype.md)
                            -   [**uap:SupportsAnyFileType**](element-1-uap-supportsanyfiletype.md)
                    -   [**uap:FileSavePicker**](element-uap-filesavepicker.md)
                        -   [**uap:SupportedFileTypes**](element-3-uap-supportedfiletypes.md)
                            -   [**uap:FileType**](element-3-uap-filetype.md)
                            -   [**uap:SupportsAnyFileType**](element-2-uap-supportsanyfiletype.md)
                    -   [**uap:AppointmentsProvider**](element-uap-appointmentsprovider.md)
                        -   [**uap:AppointmentsProviderLaunchActions**](element-uap-appointmentsproviderlaunchactions.md)
                            -   [**uap:LaunchAction**](element-2-uap-launchaction.md)
                    -   [**uap:WebAccountProvider**](element-uap-webaccountprovider.md)
                        -   [**uap:ManagedUrls**](element-uap-managedurls.md)
                            -   [**uap:Url**](element-uap-url.md)
                    -   [**uap:DialProtocol**](element-uap-dialprotocol.md)
                    -   [**uap:AppService**](element-uap-appservice.md)
                    -   [**uap:MediaPlayback**](element-uap-mediaplayback.md)
                        -   [**uap:Codec**](element-uap-codec.md)
                    -   [**uap:VoipCall**](element-uap-voipcall.md)
                        -   [**uap:VoipCallUpgrade**](element-uap-voipcallupgrade.md)
                        -   [**uap:VoipDialPhoneNumber**](element-uap-voipdialphonenumber.md)
                    -   [**uap3:AppService**](element-uap3-appservice-manual.md)
                -   [**uap3:Extension**](element-uap3-extension-manual.md)
                    -   [**uap3:AppExtensionHost**](element-uap3-appextensionhost-manual.md)
                        -   [**uap3:Name**](elemennt-uap3-name-manual.md)
                    -   [**uap3:AppExtension**](element-uap3-appextension-manual.md)
                        -   [**uap3:Properties**](elemnt-uap3-properties-manual.md)
                    -   [**uap3:AppUriHandler**](element-uap3-appurihandler-manual.md)
                        -   [**uap3:Host**](element-uap3-host-manual.md)
                    -   [**uap3:AppExecutionAlias**](element-uap3-appexecutionalias.md)
                        -   [**desktop:ExecutionAlias**](element-desktop-executionalias.md)
                        -   [**uap8:ExecutionAlias**](element-uap8-executionalias.md)
                    -   [**uap3:AppointmentDataProvider**](element-uap3-appointmentdataprovider-manual.md)
                    -   [**uap3:EmailDataProvider**](element-uap3-emaildataprovider-manual.md)
                    -   [**uap3:ContactDataProvider**](element-uap3-contactdataprovider-manual.md)
                -   [**uap4:Extension**](element-uap4-extension.md)
                    -   [**uap4:ContactPanel**](element-uap4-contactpanel.md)
                    -   [**uap4:DevicePortalProvider**](element-uap4-deviceportalprovider.md)
                    -   [**uap4:LoopbackAccessRules**](element-uap4-loopbackaccessrules.md)
                        -   [**uap4:Rule**](element-uap4-rule.md)
                    -   [**uap4:MediaCodec**](element-uap4-mediacodec.md)
                        -   [**uap4:MediaEncodingProperties**](element-uap4-mediaencodingproperties.md)
                            -   [**uap4:InputTypes**](element-uap4-inputtypes.md)
                                -   [**uap4:InputType**](element-uap4-inputtype.md)
                            -   [**uap4:OutputTypes**](element-uap4-outputtypes.md)
                                -   [**uap4:OutputType**](element-uap4-outputtype.md)
                    -   [**uap4:SharedFonts**](element-uap4-sharedfonts.md)
                        -   [**uap4:Font**](element-uap4-font.md)
                    -   [**uap4:UserDataTaskDataProvider**](element-uap4-userdatataskdataprovider.md)
                -   [**uap5:Extension**](element-uap5-extension.md)
                    -   [**uap5:UserActivity**](element-uap5-useractivity.md)
                    -   [**uap5:MediaSource**](element-uap5-mediasource.md)
                        -   [**uap5:SupportedContentTypes**](element-uap5-SupportedContentTypes.md)
                            -   [**uap5:ContentType**](element-uap5-contenttype.md)
                        -   [**uap5:SupportedFileTypes**](element-uap5-SupportedFileTypes.md)
                            -   [**uap5:FileType**](element-uap5-filetype.md)
                    -   [**uap5:VideoRendererEffect**](element-uap5-VideoRendererEffect.md)
                        -   [**uap5:VideoRendererExtensionProfiles**](element-uap5-VideoRendererExtensionProfiles.md)
                            -   [**uap5:VideoRendererExtensionProfile**](element-uap5-videorendererextensionprofile.md)
                        -   [**uap5:InputTypes**](element-uap5-inputtypes.md)
                            -   [**uap5:InputType**](element-uap5-inputtype.md)
                    -   [**uap5:ActivatableClass.OutOfProcessServer**](element-uap5-OutOfProcessServer.md)
                        -   [**uap5:Path**](element-uap5-path.md)
                        -   [**uap5:Arguments**](element-uap5-arguments.md)
                        -   [**uap5:Instancing**](element-uap5-instancing.md)
                        -   [**uap5:ActivatableClass**](element-uap5-activatableclass.md)
                    -   [**uap5:StartupTask**](element-uap5-StartupTask.md)
                    -   [**uap5:AppExecutionAlias**](element-uap5-AppExecutionAlias.md)
                        -   [**uap5:ExecutionAlias**](element-uap5-executionalias.md)
                -   [**uap6:Extension**](element-uap6-extension.md)
                    - [**uap6:BarcodeScannerProvider**](element-uap6-barcodescannerprovider.md)
                    - [**uap6:LocalExperiencePack**](element-uap6-localexperiencepack.md)
                -   [**uap10:Extension**](element-uap10-extension.md)
                    - [**uap10:HostRuntime**](element-uap10-hostruntime.md)
                    - [**uap10:InstalledLocationVirtualization**](element-uap10-installedlocationvirtualization.md)
                        - [**uap10:UpdateActions**](element-uap10-UpdateActions.md)
