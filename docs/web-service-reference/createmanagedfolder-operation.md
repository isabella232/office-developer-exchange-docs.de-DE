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
description: Der Vorgang CreateManagedFolder erstellt einen verwalteten Ordner im Exchange-Speicher.
ms.openlocfilehash: 2c2af53dc5dbe1e6fcbc7f3b1174a856e51e4905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757793"
---
# <a name="createmanagedfolder-operation"></a>CreateManagedFolder-Vorgang

Der Vorgang CreateManagedFolder erstellt einen verwalteten Ordner im Exchange-Speicher.
  
## <a name="using-the-createmanagedfolder-operation"></a>Verwenden des CreateManagedFolder-Vorgangs

Der Vorgang CreateManagedFolder hinzugefügt Postfach eines Benutzers einen verwalteten benutzerdefinierten Ordner. Das Exchange-Verwaltungsshell **Get-ManagedFolder** -Cmdlet können Sie die verfügbaren verwalteten Ordner hinzufügen zu suchen. Obwohl dieses Cmdlet verwalteten benutzerdefinierten Ordnern und verwalteten Standardordnern nur verwalteten benutzerdefinierten zurückgibt, können Ordner hinzugefügt werden. Verwaltete benutzerdefinierte Ordnern werden durch den Ordnertyp ManagedCustomFolder identifiziert. Der System.DirectoryServices-Namespace enthält auch Typen, die verwendet werden können, um die Namen der verfügbaren verwaltete Ordner zu ermitteln. 
  
> [!NOTE]
> Exchange-Webdienste können Sie die Namen der verfügbaren verwalteten Ordner hinzufügen zu einem Postfach suchen. 
  
Die FindFolder und GetFolder Vorgänge können Sie verwaltete Ordner zugreifen. FindFolder wird verwendet, um nach Ordnern in einem angegebenen übergeordneten Ordner suchen. Dies kann verwendet werden, damit verwaltete Ordner ermittelt werden können in einem Ordner vor dem Hinzufügen, dass ein Duplikat benutzerdefinierten Ordner in dasselbe Verzeichnis verwaltet. GetFolder wird nach der Operation FindFolder verwendet, um weitere Informationen zu einem verwalteten benutzerdefinierten Ordner abzurufen.
  
## <a name="remarks"></a>Hinweise

Informationen zum Einrichten von messaging Records Management (MRM) Richtlinie finden Sie unter [Gewusst wie: Erstellen einer Postfachrichtlinie für verwaltete Ordner](http://go.microsoft.com/fwlink/?LinkId=100975).
  
Informationen zum Entfernen von verwaltete benutzerdefinierte Ordnern aus einem Postfach finden Sie unter [Remove-ManagedFolder](http://go.microsoft.com/fwlink/?LinkId=100976).
  
## <a name="createmanagedfolder-request-example"></a>Anforderungsbeispiel CreateManagedFolder

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung CreateManagedFolder veranschaulicht das Hinzufügen eines verwalteten Ordners mit der Bezeichnung Test verwaltete Ordner an ein Postfach.
  
> [!NOTE]
> Delegieren des Zugriffs können auch verwaltete benutzerdefinierte Ordnern hinzufügen. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
    
- [Ordnername](foldername.md)
    
Wenn andere Optionen für die Anforderungsnachricht des Vorgangs CreateManagedFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CreateManagedFolder](createmanagedfolder.md) -Element. 
  
## <a name="successful-createmanagedfolder-response"></a>Erfolgreiche CreateManagedFolder Antwort

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine erfolgreiche Antwort auf eine Anforderung CreateManagedFolder.
  
> [!NOTE]
> Attributwerte **-Id** und **ChangeKey** wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet: 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Wenn andere Optionen für die Antwortnachrichten des Vorgangs CreateManagedFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CreateManagedFolderResponse](createmanagedfolderresponse.md) -Element. 
  
## <a name="createmanagedfolder-error-response"></a>Fehlerantwort CreateManagedFolder

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt eine Fehlerantwort an eine CreateManagedFolder-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[GetFolder Operation](getfolder-operation.md)
  
[FindFolder Operation](findfolder-operation.md)


[Suchen nach Ordnern](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Hinzufügen von verwalteten Ordnern](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

