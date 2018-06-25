---
title: CopyFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: CopyFolder-Vorgang kopiert Ordner in einem Postfach.
ms.openlocfilehash: a83444ff0927a3c8fe075c79d44d02357a737773
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757719"
---
# <a name="copyfolder-operation"></a>CopyFolder-Vorgang

CopyFolder-Vorgang kopiert Ordner in einem Postfach.
  
## <a name="using-the-copyfolder-operation"></a>Verwenden des CopyFolder-Vorgangs

Der Vorgang CopyFolder ähnelt der [MoveFolder-Vorgang](movefolder-operation.md). Kopiert die angegebene Ordnern und gibt die **Id** und **ChangeKey** der kopierten Ordner. 
  
## <a name="copyfolder-request-example"></a>CopyFolder-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung CopyFolder veranschaulicht, wie Ordner in den Ordner Posteingang zu kopieren.
  
> [!NOTE]
> Der Wert des **Id** -Attributs des Elements [FolderId](folderid.md) wurde zur besseren Lesbarkeit gekürzt. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Ordner können durch das [DistinguishedFolderId](distinguishedfolderid.md) -Element oder das [FolderId](folderid.md) -Element für die Verwendung in entweder die [ToFolderId](tofolderid.md) oder die [FolderIds](folderids.md) Elemente identifiziert werden. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CopyFolder](copyfolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Wenn andere Optionen für die Anforderungsnachricht des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CopyFolder](copyfolder.md) -Element. 
  
## <a name="successful-copyfolder-response"></a>Erfolgreiche CopyFolder-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung CopyFolder. 
  
> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comment

Das [FolderId](folderid.md) -Element, das in der Antwort zurückgegeben wird steht für den Ordner, der in den neuen Ordnerspeicherort kopiert wurde. 
  
### <a name="response-elements"></a>Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Wenn andere Optionen für die Antwortnachricht des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CopyFolderResponse](copyfolderresponse.md) -Element. 
  
## <a name="copyfolder-error-response"></a>CopyFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine CopyFolder-Anforderung. Der Fehler aufgetreten, weil ein Ordner mit dem gleichen Anzeigenamen bereits vorhanden ist.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs CopyFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CopyFolderResponse](copyfolderresponse.md) -Element. 
  
## <a name="see-also"></a>Siehe auch

- [MoveFolder-Vorgang](movefolder-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

