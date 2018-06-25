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
description: MoveFolder-Vorgang Ordner aus einem angegebenen Ordner verschoben und in einem anderen Ordner verschoben.
ms.openlocfilehash: 5da6929f11ce9ba74db190db6d799f25974d2192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830490"
---
# <a name="movefolder-operation"></a>MoveFolder-Vorgang

MoveFolder-Vorgang Ordner aus einem angegebenen Ordner verschoben und in einem anderen Ordner verschoben.
  
## <a name="remarks"></a>Hinweise

MoveFolder-Vorgang ähnelt der CopyFolder-Vorgang. Sie können nicht definierten Ordner verschieben. Sie können gleichzeitig mehrere Ordner in den Zielordner verschieben.
  
## <a name="movefolder-request-example"></a>MoveFolder-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung MoveFolder bilden eine Anforderung zum Verschieben eines Ordners durch die [FolderId](folderid.md) identifiziert, und legen den Ordner im Ordner "Junk-e-Mail definierten" veranschaulicht. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Kommentare

> [!NOTE]
> Der Wert des ID-Attributs des Elements [FolderId](folderid.md) wurde zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

Diese MoveFolder-Anforderung enthält die folgenden Elemente:
  
- [MoveFolder](movefolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
Finden Sie im Schema für weitere Elemente, die Sie verwenden können, um eine Anforderung MoveFolder bilden.
  
> [!NOTE]
> Der Standardspeicherort des Schemas ist in das virtuelle EWS-Verzeichnis auf dem Computer, der die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="successful-movefolder-response-example"></a>Erfolgreiche MoveFolder-Antwort-Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung MoveFolder. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Kommentare

> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
Die FolderId, die in der Antwort zurückgegeben wird steht für den Ordner, die wurde verschoben zu den neuen Speicherort des Ordners.
  
### <a name="response-elements"></a>Antwortelemente

Die Antwort MoveFolder umfasst die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="movefolder-error-response-example"></a>MoveFolder-Fehler antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an, die auftritt, wenn Sie versuchen, einen definierten Ordner zu verschieben.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <MoveFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="error-response-elements"></a>Fehler Antwortelemente

MoveFolder-Fehlerantwort umfasst die folgenden Elemente:
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



[CopyFolder-Vorgang](copyfolder-operation.md)

