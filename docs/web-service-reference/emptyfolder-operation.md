---
title: EmptyFolder-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 98161486-e2f2-480f-8d5d-708ba81b208a
description: Der EmptyFolder-Vorgang leert Ordner in einem Postfach. Optional können Sie mit diesem Vorgang die Unterordner des angegebenen Ordners löschen. Wenn ein Unterordner gelöscht wird, werden der Unterordner und die Nachrichten im Unterordner gelöscht.
ms.openlocfilehash: 8191dc7ecea7038a6d885f30d08fe561a59c4ed2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519667"
---
# <a name="emptyfolder-operation"></a>EmptyFolder-Vorgang

Der **EmptyFolder-Vorgang** leert Ordner in einem Postfach. Optional können Sie mit diesem Vorgang die Unterordner des angegebenen Ordners löschen. Wenn ein Unterordner gelöscht wird, werden der Unterordner und die Nachrichten im Unterordner gelöscht. 
  
## <a name="emptyfolder-request-example"></a>EmptyFolder-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

In diesem folgenden Beispiel einer **EmptyFolder-Anforderung** wird gezeigt, wie Sie eine Anforderung zum Leeren eines Ordners erstellen. In diesem Beispiel werden alle Unterordner des angegebenen Ordners gelöscht. 
  
> [!NOTE]
> Die Werte der **Attribute "Id"** und **"ChangeKey"** des ["FolderId"-Elements](folderid.md) wurden zur besseren Lesbarkeit gekürzt. 
  
### <a name="code"></a>Code

```XML
<soap:Envelope xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  <soap:Header>
    <t:RequestServerVersion Version ="Exchange2010_SP1"/>
    </soap:Header>
    <soap:Body>
      <m:EmptyFolder DeleteType="HardDelete" DeleteSubFolders="true">
        <m:FolderIds>
          <t:FolderId Id="AQMkADhhOGU0"  ChangeKey="AQAAABYAAABsMB" />
        </m:FolderIds>
      </m:EmptyFolder>
    </soap:Body>
</soap:Envelope>

```

### <a name="comments"></a>Comments

In diesem Beispiel wird der Ordner endgültig gelöscht.
  
Ordner können entweder durch das [DistinguishedFolderId-Element](distinguishedfolderid.md) oder das [FolderId-Element](folderid.md) für die Verwendung im [FolderIds-Element](folderids.md) identifiziert werden. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [EmptyFolder](emptyfolder.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
## <a name="successful-emptyfolder-response"></a>Erfolgreiche EmptyFolder-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die **EmptyFolder-Anforderung.** 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="1" 
                         MajorBuildNumber="164" 
                         MinorBuildNumber="0" 
                         Version="Exchange2010_SP1"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:EmptyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:EmptyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:EmptyFolderResponseMessage>
      </m:ResponseMessages>
    </m:EmptyFolderResponse>
  </s:Body>
</s:Envelope>

```

### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [EmptyFolderResponse](emptyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [EmptyFolderResponseMessage](emptyfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="emptyfolder-error-response"></a>EmptyFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine **Emptyfolder-Anforderung.** Der Fehler wurde erstellt, da der Vorgang versucht hat, einen Ordner zu leeren, der im Exchange Speicher nicht gefunden wurde. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
            MinorVersion="1" 
            MajorBuildNumber="164" 
            MinorBuildNumber="0" 
            Version="Exchange2010_SP1" 
            xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
            xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse 
          xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

### <a name="error-response-elements"></a>Fehlerantwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetFolderResponse](getfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetFolderResponseMessage](getfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

