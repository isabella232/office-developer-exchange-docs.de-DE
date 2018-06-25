---
title: CreateFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 6f6c334c-b190-4e55-8f0a-38f2a018d1b3
description: Der CreateFolder-Vorgang erstellt Ordner, Kalenderordnern, Kontakteordner, Aufgaben Ordner und Suche Ordner.
ms.openlocfilehash: 97156d4a3747cacbdcf9563d21d93a0aa44c3358
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757758"
---
# <a name="createfolder-operation"></a>CreateFolder Operation

Der CreateFolder-Vorgang erstellt Ordner, Kalenderordnern, Kontakteordner, Aufgaben Ordner und Suche Ordner.
  
## <a name="createfolder-request-example"></a>CreateFolder-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung CreateFolder veranschaulicht eine Anforderung zum Erstellen von zwei neue Ordner im Stamm Postfach bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ParentFolderId>
        <t:DistinguishedFolderId Id="msgfolderroot"/>
      </ParentFolderId>
      <Folders>
        <t:Folder>
          <t:DisplayName>Folder1</t:DisplayName>
        </t:Folder>
        <t:Folder>
          <t:DisplayName>Folder2</t:DisplayName>
        </t:Folder>
      </Folders>
    </CreateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Anfordern von Elementen

In der Anforderung werden folgende Elemente verwendet:
  
- [CreateFolder](createfolder.md)
    
- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [DisplayName (Zeichenfolge)](displayname-string.md)
    
> [!NOTE]
> Das Schema, das diese Elemente beschreibt, befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
Um weitere Optionen für die Anforderung an die CreateFolder-Operation zu suchen, verwenden Sie die Schemahierarchie. Starten Sie die [CreateFolder](createfolder.md) -Element. 
  
> [!NOTE]
> Wenn Sie einen Suchordner mit einer Einschränkung mithilfe der **Kalender: Organizer** -Eigenschaft erstellen, zurückgegebenen Gespräch Ordner nachfolgende Get die Einschränkung wieder mit der **Nachricht: aus** -Eigenschaft in seine Position. Diese beiden Eigenschaften zuordnen der gleichen zugrunde liegenden MAPI-Eigenschaft. 
  
Die CreateFolder-Operation unterstützt die Erstellung einer benutzerdefinierten Ordner-Klasse nur, wenn Sie des Ordners erstellen mithilfe eine generische Ordner "Type"-Element und das **FolderClass** -Element festgelegt. 
  
## <a name="successful-createfolder-response-example"></a>Erfolgreiche CreateFolder-Antwort-Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf die CreateFolder-Anforderung. In diesem Beispiel gibt die Antwort den IDs der neuen Ordner.
  
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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
        <m:CreateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn==" />
            </t:Folder>
          </m:Folders>
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>Elemente einer erfolgreichen Antwort

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
Wenn andere Optionen für die Antwortnachricht des Vorgangs CreateFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CreateFolderResponse](createfolderresponse.md) -Element. 
  
## <a name="createfolder-error-response"></a>CreateFolder-Fehlerantwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an eine CreateFolder-Anforderung.
  
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
    <CreateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A folder with the specified name already exists.</m:MessageText>
          <m:ResponseCode>ErrorFolderExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CreateFolderResponseMessage>
      </m:ResponseMessages>
    </CreateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Fehler Antwortelemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateFolderResponse](createfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateFolderResponseMessage](createfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Ordner](folders-ex15websvcsotherref.md)
    
Wenn andere Optionen für die Fehlermeldung Antwort des Vorgangs CreateFolder suchen möchten, verwenden Sie die Schemahierarchie. Starten Sie das [CreateFolderResponse](createfolderresponse.md) -Element. 
  
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindFolder Operation](findfolder-operation.md)
  
 **CreateFolderType**


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Erstellen von Ordnern (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

