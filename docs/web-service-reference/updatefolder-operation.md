---
title: UpdateFolder-Vorgang
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: 'Der UpdateFolder-Vorgang dient zum Ändern der Eigenschaften eines vorhandenen Elements im Exchange Speicher. Jeder UpdateFolder-Vorgang besteht aus folgenden Komponenten:'
ms.openlocfilehash: be8e39e13681cea34e312158c348c60a94374bec
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541763"
---
# <a name="updatefolder-operation"></a>UpdateFolder-Vorgang

Der UpdateFolder-Vorgang dient zum Ändern der Eigenschaften eines vorhandenen Elements im Exchange Speicher. Jeder UpdateFolder-Vorgang besteht aus folgenden Komponenten:
  
- Ein [FolderId-Element,](folderid.md) das einen zu aktualisierenden Ordner angibt. 
    
- Ein interner Pfad eines Elements im Ordner, wie durch das Ordner-Shape angegeben, das die zu aktualisierenden Daten angibt.
    
- Ein Ordner, der den neuen Wert des aktualisierten Felds enthält, wenn es sich bei der Aktualisierung nicht um einen Löschvorgang handelt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Für ein Element können drei grundlegende Aktualisierungsaktionen ausgeführt werden. Diese Aktionen sind in der folgenden Tabelle aufgeführt.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Anfügen  <br/> |Die Anfügeaktion fügt einer vorhandenen Eigenschaft Daten hinzu. Sie behält die Daten bei, die sich derzeit dort befinden. Das Anfügen gilt nicht für alle Eigenschaften.  <br/> |
|Satz  <br/> |Die Set-Aktion ersetzt Daten für eine Eigenschaft, wenn sie Daten enthält, oder erstellt die Eigenschaft und legt ihren Wert fest, wenn sie nicht vorhanden ist. Die Set-Aktion gilt nur für schreibbare Eigenschaften.  <br/> |
|Löschen  <br/> |Die Löschaktion entfernt eine Eigenschaft aus einem Ordner. Dies unterscheidet sich von der Einstellung auf einen leeren Wert. Nach Abschluss des Vorgangs ist die Eigenschaft für den Ordner nicht vorhanden. Das Löschen gilt nur für beschreibbare Eigenschaften.  <br/> |
   
## <a name="updatefolder-request-example"></a>UpdateFolder-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer UpdateFolder-Anforderung zeigt, wie ein Ordneranzeigename aktualisiert wird. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AScA" ChangeKey="GO3u/"/>
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName"/>
              <t:Folder>
                <t:DisplayName>NewFolderName</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </FolderChanges>
    </UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

In diesem Beispiel wird der Anzeigename des Ordners in NewFolderName geändert.
  
> [!NOTE]
> Die Werte der Attribute **"Id"** und **"ChangeKey"** des ["FolderId"-Elements](folderid.md) wurden zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Updates (Ordner)](updates-folder.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Ordner](folder.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
Weitere Elemente, die Sie zum Erstellen einer UpdateFolder-Anforderung verwenden können, finden Sie im Schema.
  
> [!NOTE]
> Der Standardspeicherort des Schemas befindet sich im virtuellen EWS-Verzeichnis auf dem Computer, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="updatefolder-response-example"></a>UpdateFolder-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die UpdateFolder-Anforderung. In diesem Beispiel wird der neue Änderungsschlüssel zurückgegeben, um den aktualisierten Status des Ordners widerzuspiegeln.
  
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
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFVz" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu gewährleisten. 
  
Die Ordner-ID, die in der Antwort zurückgegeben wird, stellt den aktualisierten Ordner dar.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Ordner](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>UpdateFolder-Fehlerantwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine UpdateFolder-Anforderung.
  
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
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Dieses Beispiel zeigt eine Fehlerantwort, die durch ein ungültiges **ChangeKey-Attribut** in der Anforderung verursacht wird. 
  
### <a name="error-response-elements"></a>Fehlerantwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

