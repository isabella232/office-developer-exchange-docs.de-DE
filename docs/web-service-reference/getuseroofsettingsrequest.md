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
description: Das GetUserOofSettingsRequest-Element ist das Stammelement mit den Argumenten verwendet, um ein Postfach des Benutzers Out of Office (OOF) Einstellungen abzurufen.
ms.openlocfilehash: e64818961283f90e447e2044cf7f918eccd21f06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829692"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="9d1d8-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="9d1d8-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="9d1d8-104">Das **GetUserOofSettingsRequest** -Element ist das Stammelement mit den Argumenten verwendet, um ein Postfach des Benutzers Out of Office (OOF) Einstellungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="9d1d8-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="9d1d8-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d1d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d1d8-106">Attributes and elements</span></span>

<span data-ttu-id="9d1d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d1d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d1d8-108">Attributes</span></span>

<span data-ttu-id="9d1d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d1d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d1d8-110">Child elements</span></span>

|<span data-ttu-id="9d1d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d1d8-111">**Element**</span></span>|<span data-ttu-id="9d1d8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d1d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d1d8-113">Postfach (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="9d1d8-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="9d1d8-114">Identifiziert den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d1d8-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d1d8-115">Parent elements</span></span>

<span data-ttu-id="9d1d8-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d1d8-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d1d8-117">Remarks</span></span>

<span data-ttu-id="9d1d8-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="9d1d8-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d1d8-119">Example</span></span>

<span data-ttu-id="9d1d8-120">Es folgt ein Beispiel für eine GetUserOofSettings-Anforderung, die Informationen für einen Einzelbenutzer OOF abruft.</span><span class="sxs-lookup"><span data-stu-id="9d1d8-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="9d1d8-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d1d8-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d1d8-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d1d8-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d1d8-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d1d8-123">Schema Name</span></span>  <br/> |<span data-ttu-id="9d1d8-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="9d1d8-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d1d8-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d1d8-125">Validation File</span></span>  <br/> |<span data-ttu-id="9d1d8-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d1d8-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d1d8-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d1d8-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d1d8-128">False</span><span class="sxs-lookup"><span data-stu-id="9d1d8-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d1d8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d1d8-129">See also</span></span>



[<span data-ttu-id="9d1d8-130">GetUserOofSettings-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9d1d8-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

