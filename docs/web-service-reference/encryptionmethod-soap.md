---
title: EncryptionMethod (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: bc632c85-ec74-4a00-baec-df5973e032fa
description: Das Element EncryptionMethod stellt die kryptografische Methode, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird.
ms.openlocfilehash: 5062d357a54019a576e391e1be4d4e8dfcc6e38d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758216"
---
# <a name="encryptionmethod-soap"></a>EncryptionMethod (SOAP)

Das Element **EncryptionMethod** stellt die kryptografische Methode, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird. 
  
```XML
<EncryptionMethod/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ProtocolConnection (SOAP)](protocolconnection-soap.md) <br/> |Stellt die Verbindung Protokoll des Webclients Server dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist die kryptografische-Methode, die für die POP-, IMAP- und SMTP-Protokolle verwendet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlung-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserSettings-Vorgang (SOAP)](getusersettings-operation-soap.md)

