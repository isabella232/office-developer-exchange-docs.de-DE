---
title: MoveFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und fügt Sie in einen anderen Ordner ein.
ms.openlocfilehash: dc572130ca3b2f2b152abbb4a8b68cc6f67790e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460582"
---
# <a name="movefolder-operation"></a>MoveFolder-Vorgang

Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und fügt Sie in einen anderen Ordner ein.
  
## <a name="remarks"></a>Bemerkungen

Der MoveFolder-Vorgang ähnelt dem CopyFolder-Vorgang. Sie können keine Distinguished Folders migrieren. Sie können mehrere Ordner gleichzeitig in den Zielordner umlegen.
  
## <a name="movefolder-request-example"></a>MoveFolder-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer MoveFolder-Anforderung wird gezeigt, wie eine Anforderung zum Verschieben eines Ordners, der durch die [Ordner](folderid.md) -Nr identifiziert wird, und dem Ordner in den definierten Junk-e-Mail-Ordner gestellt wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

> [!NOTE]
> Der Wert des ID-Attributs des [Folder](folderid.md) -ID-Elements wurde zur Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese MoveFolder-Anforderung umfasst die folgenden Elemente:
  
- [MoveFolder](movefolder.md)
    
- [Tofolder-Datei](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
Weitere Elemente, die Sie zum Erstellen einer MoveFolder-Anforderung verwenden können, finden Sie im Schema.
  
> [!NOTE]
> Der Standardspeicherort des Schemas befindet sich im virtuellen Verzeichnis EWS auf dem Computer, auf dem die Client Zugriffs-Serverrolle installiert ist. 
  
## <a name="successful-movefolder-response-example"></a>Erfolgreiches MoveFolder-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die MoveFolder-Anforderung. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

> [!NOTE]
> Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
Die in der Antwort zurückgegebene Ordner-Nr stellt den Ordner dar, der an den neuen Speicherort des Ordners verschoben wurde.
  
### <a name="response-elements"></a>Response-Elemente

Die MoveFolder-Antwort umfasst die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Ordner](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="movefolder-error-response-example"></a>MoveFolder-Fehlerantwort Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlermeldung, die auftritt, wenn Sie versuchen, einen Distinguished Folder zu verlagern.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

Die MoveFolder-Fehlerantwort umfasst die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[CopyFolder-Vorgang](copyfolder-operation.md)

