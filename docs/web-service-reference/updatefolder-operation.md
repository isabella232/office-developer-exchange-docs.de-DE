---
title: UpdateFolder-Vorgang
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: 'Der UpdateFolder-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern. Jeder UpdateFolder-Vorgang besteht aus folgenden Elementen:'
ms.openlocfilehash: fb894d9f42358b67f81e9fe8ae41ba61e6f46460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467361"
---
# <a name="updatefolder-operation"></a>UpdateFolder-Vorgang

Der UpdateFolder-Vorgang wird verwendet, um die Eigenschaften eines vorhandenen Elements in der Exchange-Informationsspeicher zu ändern. Jeder UpdateFolder-Vorgang besteht aus folgenden Elementen:
  
- Ein [Folder](folderid.md) -Element, mit dem ein zu aktualisierbarer Ordner angegeben wird. 
    
- Ein interner Pfad eines Elements im Ordner, wie durch die Ordner Form angegeben, die die zu aktualisierende Daten angibt.
    
- Ein Ordner, der den neuen Wert des aktualisierten Felds enthält, wenn es sich bei der Aktualisierung nicht um eine Löschung handelt.
    
## <a name="remarks"></a>Bemerkungen

Für ein Element können drei grundlegende Updateaktionen ausgeführt werden. Diese Aktionen sind in der folgenden Tabelle aufgeführt.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Append  <br/> |Mit der Append-Aktion werden einer vorhandenen Eigenschaft Daten hinzugefügt. Die Daten, die derzeit vorhanden sind, werden beibehalten. Append gilt nicht für alle Eigenschaften.  <br/> |
|Satz  <br/> |Die Set-Aktion ersetzt Daten für eine Eigenschaft, wenn Sie Daten enthält, oder erstellt die Eigenschaft und legt ihren Wert fest, wenn Sie nicht vorhanden ist. Die Aktion festlegen gilt nur für schreibbare Eigenschaften.  <br/> |
|Löschen  <br/> |Die DELETE-Aktion entfernt eine Eigenschaft aus einem Ordner. Dies unterscheidet sich von der Einstellung auf einen leeren Wert. Wenn dieser Vorgang abgeschlossen ist, ist die Eigenschaft für den Ordner nicht vorhanden. DELETE gilt nur für schreibbare Eigenschaften.  <br/> |
   
## <a name="updatefolder-request-example"></a>UpdateFolder-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer UpdateFolder-Anforderung wird gezeigt, wie ein Ordneranzeige Name aktualisiert wird. 
  
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

In diesem Beispiel wird der Anzeigename des Ordners in "neuer FolderName" geändert.
  
> [!NOTE]
> Die Werte der Attribute **ID** und **ChangeKey** des [Folder](folderid.md) -Elements wurden zur Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Updates (Ordner)](updates-folder.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
Weitere Elemente, die Sie zum Erstellen einer UpdateFolder-Anforderung verwenden können, finden Sie im Schema.
  
> [!NOTE]
> Der Standardspeicherort des Schemas befindet sich im virtuellen Verzeichnis EWS auf dem Computer, auf dem die Client Zugriffs-Serverrolle installiert ist. 
  
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
> Die Ordner-ID und der Change-Schlüssel wurden verkürzt, um die Lesbarkeit zu erhalten. 
  
Die in der Antwort zurückgegebene Ordner-ID stellt den aktualisierten Ordner dar.
  
### <a name="successful-response-elements"></a>Erfolgreiche Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>UpdateFolder-Fehlerantwort Beispiel

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

Dieses Beispiel zeigt eine Fehlerantwort, die durch ein ungültiges **ChangeKey** -Attribut in der Anforderung verursacht wird. 
  
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

