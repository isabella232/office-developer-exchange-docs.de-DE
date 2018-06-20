---
title: Empfänger (ArrayOfSmtpAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: Das Empfänger-Element gibt ein Array von Empfänger einer Nachricht.
ms.openlocfilehash: 8490988043b1e06fd3a8f553fcefaeb2e90e9d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830988"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="69621-103">Empfänger (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="69621-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="69621-104">Das **Empfänger** -Element gibt ein Array von Empfänger einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="69621-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="69621-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="69621-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69621-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69621-106">Attributes and elements</span></span>

<span data-ttu-id="69621-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69621-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69621-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="69621-108">Attributes</span></span>

<span data-ttu-id="69621-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="69621-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69621-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69621-110">Child elements</span></span>

|<span data-ttu-id="69621-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="69621-111">**Element**</span></span>|<span data-ttu-id="69621-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69621-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69621-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="69621-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="69621-114">Stellt die Simple Mail Transfer Protocol (SMTP) Empfängeradresse eines Kalenders oder Kontakt Freigabeanfrage dar.</span><span class="sxs-lookup"><span data-stu-id="69621-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69621-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69621-115">Parent elements</span></span>

|<span data-ttu-id="69621-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="69621-116">**Element**</span></span>|<span data-ttu-id="69621-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69621-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69621-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="69621-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="69621-119">Definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="69621-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69621-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="69621-120">Remarks</span></span>

<span data-ttu-id="69621-121">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="69621-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69621-122">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="69621-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69621-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="69621-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69621-124">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69621-124">Schema Name</span></span>  <br/> |<span data-ttu-id="69621-125">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="69621-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="69621-126">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69621-126">Validation File</span></span>  <br/> |<span data-ttu-id="69621-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="69621-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69621-128">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="69621-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="69621-129">False</span><span class="sxs-lookup"><span data-stu-id="69621-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69621-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69621-130">See also</span></span>



[<span data-ttu-id="69621-131">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="69621-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="69621-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="69621-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

