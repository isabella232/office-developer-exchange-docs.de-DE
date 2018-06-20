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
description: 'Der Vorgang UpdateFolder wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern. Jede UpdateFolder-Operation besteht aus den folgenden:'
ms.openlocfilehash: b33937bb09f0dcbe3d3ed61bbf5233423f320d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839348"
---
# <a name="updatefolder-operation"></a>UpdateFolder-Vorgang

Der Vorgang UpdateFolder wird verwendet, um die Eigenschaften eines vorhandenen Elements im Exchange-Speicher zu ändern. Jede UpdateFolder-Operation besteht aus den folgenden:
  
- Ein [FolderId](folderid.md) -Element, einen Ordner aktualisieren angibt. 
    
- Ein interner Pfad eines Elements im Ordner gemäß den Ordner-Shape, das zu aktualisierenden gibt.
    
- Ein Ordner, der den neuen Wert des Felds aktualisierte enthält, wenn das Update nicht auf eine Löschung ist.
    
## <a name="remarks"></a>Hinweise

Drei grundlegende Update-Aktionen können für ein Element ausgeführt werden. Diese Aktionen sind in der folgenden Tabelle aufgeführt.
  
|**Aktion**|**Beschreibung**|
|:-----|:-----|
|Anfügeabfrage  <br/> |Die Append-Aktion hinzugefügt Daten auf eine vorhandene Eigenschaft. Beibehalten die Daten, die derzeit vorhanden ist. Fügen Sie gilt nicht für alle Eigenschaften.  <br/> |
|Gruppe  <br/> |Die Set-Aktion ersetzt Daten für eine Eigenschaft aus, wenn Daten enthält, oder die Eigenschaft erstellt und legt deren Wert fest, wenn er nicht vorhanden ist. Die Set-Aktion gilt nur für schreibbaren Eigenschaften.  <br/> |
|Löschen  <br/> |Die Löschaktion entfernt eine Eigenschaft aus einem Ordner. Dies unterscheidet sich auf einen leeren Wert festlegen. Nach Abschluss des Vorgangs ist die Eigenschaft für den Ordner nicht vorhanden. Delete gilt nur für schreibbaren Eigenschaften.  <br/> |
   
## <a name="updatefolder-request-example"></a>Anforderungsbeispiel UpdateFolder

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer Anforderung UpdateFolder veranschaulicht einen Anzeigenamen für den Ordner zu aktualisieren. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a>Kommentare

In diesem Beispiel wird der Anzeigename des Ordners auf NeuerOrdnername geändert.
  
> [!NOTE]
> Die Werte der **Id** und **ChangeKey** Attribute des Elements [FolderId](folderid.md) wurden zur besseren Lesbarkeit gekürzt. 
  
### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Updates (Element)](updates-item.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
Finden Sie im Schema für zusätzliche Elemente, die Sie verwenden können, um eine Anforderung UpdateFolder bilden.
  
> [!NOTE]
> Der Standardspeicherort des Schemas ist in das virtuelle EWS-Verzeichnis auf dem Computer, der die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="updatefolder-response-example"></a>UpdateFolder antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die Anforderung UpdateFolder. In diesem Beispiel wird der neue Änderungsschlüssel gemäß den aktualisierten Status des Ordners zurückgegeben.
  
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
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Kommentare

> [!NOTE]
> Die Ordner-ID und der Änderungsschlüssel wurden gekürzt, um die Lesbarkeit zu erhalten. 
  
Die Ordner-ID, die in der Antwort zurückgegeben wird, stellt aktualisierten Ordner.
  
### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>Antwortbeispiel UpdateFolder-Fehler

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine UpdateFolder-Anforderung.
  
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
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>Kommentare

Dieses Beispiel zeigt eine Fehlerantwort an, die durch ein ungültiges **ChangeKey** -Attribut in der Anforderung verursacht wird. 
  
### <a name="error-response-elements"></a>Fehler Antwortelemente

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

