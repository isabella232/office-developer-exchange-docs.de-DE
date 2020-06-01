---
title: CreateManagedFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: Mit dem CreateManagedFolder-Vorgang wird ein verwalteter Ordner im Exchange-Informationsspeicher erstellt.
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44444593"
---
# <a name="createmanagedfolder-operation"></a>CreateManagedFolder-Vorgang

Mit dem CreateManagedFolder-Vorgang wird ein verwalteter Ordner im Exchange-Informationsspeicher erstellt.
  
## <a name="using-the-createmanagedfolder-operation"></a>Verwenden des CreateManagedFolder-Vorgangs

Mit dem CreateManagedFolder-Vorgang wird dem Postfach eines Benutzers ein verwalteter benutzerdefinierter Ordner hinzugefügt. Mit dem Cmdlet Exchange-Verwaltungsshell **Get-ManagedFolder** können Sie nach verfügbaren verwalteten Ordnern suchen, die hinzugefügt werden sollen. Dieses Cmdlet gibt zwar sowohl verwaltete benutzerdefinierte Ordner als auch verwaltete Standardordner zurück, nur verwaltete benutzerdefinierte Ordner können hinzugefügt werden. Verwaltete benutzerdefinierte Ordner werden anhand des ManagedCustomFolder-Ordnertyps identifiziert. Der System. DirectoryServices-Namespace enthält auch Typen, die zum Ermitteln der Namen von verfügbaren verwalteten Ordnern verwendet werden können. 
  
> [!NOTE]
> Sie können Exchange Webdienste nicht verwenden, um die Namen der verfügbaren verwalteten Ordner zu finden, die einem Postfach hinzugefügt werden sollen. 
  
Sie können die FindFolder-und GetFolder-Vorgänge verwenden, um auf verwaltete Ordner zuzugreifen. FindFolder wird verwendet, um nach Ordnern in einem angegebenen übergeordneten Ordner zu suchen. Dies kann verwendet werden, damit verwaltete Ordner in einem Ordner erkannt werden können, bevor ein doppelter verwalteter benutzerdefinierter Ordner demselben Verzeichnis hinzugefügt werden kann. GetFolder wird nach dem FindFolder-Vorgang verwendet, um weitere Informationen zu einem verwalteten benutzerdefinierten Ordner abzurufen.
  
## <a name="remarks"></a>Bemerkungen

Informationen zum Einrichten der Messaging-Datensatzverwaltung (MRM)-Richtlinie finden Sie unter [Erstellen einer Postfachrichtlinie für verwalteten Ordner](https://go.microsoft.com/fwlink/?LinkId=100975).
  
Informationen zum Entfernen verwalteter benutzerdefinierter Ordner aus einem Postfach finden Sie unter [Remove-ManagedFolder](https://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>CreateManagedFolder-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer CreateManagedFolder-Anforderung wird gezeigt, wie einem Postfach ein verwalteter Ordner mit dem Namen "Test Managed Folder" hinzugefügt wird.
  
> [!NOTE]
> Sie können auch den Stellvertretungszugriff zum Hinzufügen verwalteter benutzerdefinierter Ordner verwenden. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
Um andere Optionen für die Anforderungsnachricht des CreateManagedFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie. Beginnen Sie mit dem [CreateManagedFolder](createmanagedfolder.md) -Element. 
  
## <a name="successful-createmanagedfolder-response"></a>Erfolgreiche CreateManagedFolder-Antwort

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine erfolgreiche Antwort auf eine CreateManagedFolder-Anforderung.
  
> [!NOTE]
> Die **ID** -und **ChangeKey** -Attributwerte wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Um andere Optionen für die Antwortnachrichten des CreateManagedFolder-Vorgangs zu finden, erkunden Sie die Schemahierarchie. Beginnen Sie mit dem [CreateManagedFolderResponse](createmanagedfolderresponse.md) -Element. 
  
## <a name="createmanagedfolder-error-response"></a>CreateManagedFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine Fehlerantwort auf eine CreateManagedFolder-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[GetFolder-Vorgang](getfolder-operation.md)
  
[FindFolder-Vorgang](findfolder-operation.md)


[Suchen von Ordnern](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

