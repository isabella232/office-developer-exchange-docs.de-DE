---
title: GetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 15dea99c-7f5d-4af1-82ff-4255127fe567
description: Das GetUserOofSettingsRequest-Element ist das Stammelement, das die Argumente enthält, mit denen die Abwesenheit (Out of Office, OOF) Einstellungen eines Postfachbenutzers abgerufen werden.
ms.openlocfilehash: f515e8cf016d3aff6c652ae92a0da71a8f0a5f6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457830"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="f1ea3-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="f1ea3-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="f1ea3-104">Das **GetUserOofSettingsRequest** -Element ist das Stammelement, das die Argumente enthält, mit denen die Abwesenheit (Out of Office, OOF) Einstellungen eines Postfachbenutzers abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="f1ea3-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="f1ea3-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1ea3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1ea3-106">Attributes and elements</span></span>

<span data-ttu-id="f1ea3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1ea3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1ea3-108">Attributes</span></span>

<span data-ttu-id="f1ea3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1ea3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1ea3-110">Child elements</span></span>

|<span data-ttu-id="f1ea3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1ea3-111">**Element**</span></span>|<span data-ttu-id="f1ea3-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1ea3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1ea3-113">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f1ea3-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="f1ea3-114">Identifiziert den Postfachbenutzer für eine SetUserOofSettings-oder GetUserOofSettings-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1ea3-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1ea3-115">Parent elements</span></span>

<span data-ttu-id="f1ea3-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1ea3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1ea3-117">Remarks</span></span>

<span data-ttu-id="f1ea3-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="f1ea3-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1ea3-119">Example</span></span>

<span data-ttu-id="f1ea3-120">Im folgenden finden Sie ein Beispiel für eine GetUserOofSettings-Anforderung, die die OOF-Informationen eines einzelnen Benutzers abruft.</span><span class="sxs-lookup"><span data-stu-id="f1ea3-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="f1ea3-121">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f1ea3-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1ea3-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1ea3-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1ea3-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1ea3-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f1ea3-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="f1ea3-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f1ea3-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1ea3-125">Validation File</span></span>  <br/> |<span data-ttu-id="f1ea3-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f1ea3-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1ea3-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f1ea3-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1ea3-128">False</span><span class="sxs-lookup"><span data-stu-id="f1ea3-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1ea3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1ea3-129">See also</span></span>



[<span data-ttu-id="f1ea3-130">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f1ea3-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

