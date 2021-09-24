---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: Das GetSharingMetadata-Element definiert eine Anforderung zum Abrufen eines undurchsichtigen Authentifizierungstokens, das die Freigabe-Einladung identifiziert. Dieses Element ist das Basiselement für den GetSharingMetadata-Vorgang.
ms.openlocfilehash: 65da8371b25c42e59f898c79403f06fa17e5a24a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523051"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

Das **GetSharingMetadata-Element** definiert eine Anforderung zum Abrufen eines undurchsichtigen Authentifizierungstokens, das die Freigabe-Einladung identifiziert. Dieses Element ist das Basiselement für den [GetSharingMetadata-Vorgang.](getsharingmetadata-operation.md)
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Stellt den Bezeichner des Ordners auf dem Server dar, der freigegeben wird. Dieses Element ist erforderlich.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Stellt die SMTP-E-Mail-Adresse dar, die dem Postfach entspricht, das den Ordner enthält, der durch das [IdOfFolderToShare-Element](idoffoldertoshare.md) identifiziert wird. Dieses Element ist erforderlich.  <br/> |
|[Empfänger (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Stellt die SMTP-E-Mail-Adressen einer oder mehrerer Entitäten dar, denen Zugriff auf die Daten in dem Ordner gewährt wird, der vom [IdOfFolderToShare-Element](idoffoldertoshare.md) identifiziert wird. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

