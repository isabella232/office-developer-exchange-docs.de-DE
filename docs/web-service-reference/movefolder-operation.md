---
title: MoveFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und platziert sie in einem anderen Ordner.
ms.openlocfilehash: e0b0e93bd070354d03c511382b6096f2d3a07508
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523859"
---
# <a name="movefolder-operation"></a>MoveFolder-Vorgang

Der MoveFolder-Vorgang verschiebt Ordner aus einem angegebenen Ordner und platziert sie in einem anderen Ordner.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der MoveFolder-Vorgang ähnelt dem CopyFolder-Vorgang. Distinguished Folders können nicht verschoben werden. Sie können mehrere Ordner gleichzeitig in den Zielordner verschieben.
  
## <a name="movefolder-request-example"></a>MoveFolder-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer MoveFolder-Anforderung zeigt, wie Sie eine Anforderung zum Verschieben eines durch die [FolderId](folderid.md) identifizierten Ordners und das Ablegen des Ordners in den Ordner "Junk-E-Mail distinguished" erstellen. 
  
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
> Der Wert des ID-Attributs des [FolderId-Elements](folderid.md) wurde zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese MoveFolder-Anforderung enthält die folgenden Elemente:
  
- [MoveFolder](movefolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
Weitere Elemente, die Sie zum Erstellen einer MoveFolder-Anforderung verwenden können, finden Sie im Schema.
  
> [!NOTE]
> Der Standardspeicherort des Schemas befindet sich im virtuellen EWS-Verzeichnis auf dem Computer, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="successful-movefolder-response-example"></a>Beispiel für eine erfolgreiche MoveFolder-Antwort

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
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
Die FolderId, die in der Antwort zurückgegeben wird, stellt den Ordner dar, der an den neuen Speicherort des Ordners verschoben wurde.
  
### <a name="response-elements"></a>Antwortelemente

Die MoveFolder-Antwort enthält die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Ordner](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="movefolder-error-response-example"></a>MoveFolder-Fehlerantwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort, die auftritt, wenn Sie versuchen, einen definierten Ordner zu verschieben.
  
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

Die MoveFolder-Fehlerantwort enthält die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[CopyFolder-Vorgang](copyfolder-operation.md)

