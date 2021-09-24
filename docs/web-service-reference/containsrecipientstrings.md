---
title: ContainsRecipientStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContainsRecipientStrings
api_type:
- schema
ms.assetid: a7fd13ac-0f13-4610-ac9b-98e27ac3940b
description: Das ContainsRecipientStrings-Element gibt die Zeichenfolgen an, die in den ToRecipients- oder CcRecipients-Eigenschaften eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 9d4bb53e4963af6d25fd5e2aaf3819ac20a39479
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520934"
---
# <a name="containsrecipientstrings"></a>ContainsRecipientStrings

Das **ContainsRecipientStrings-Element** gibt die Zeichenfolgen an, die in den **ToRecipients-** oder **CcRecipients-Eigenschaften** eingehender Nachrichten angezeigt werden müssen, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<ContainsRecipientStrings>
    <String/>
</ContainsRecipientStrings>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[String](string.md) <br/> |Stellt eine Zeichenfolge dar, die entweder in den **ToRecipients-** oder **CcRecipients-Eigenschaften** eingehender Nachrichten angezeigt werden muss, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

