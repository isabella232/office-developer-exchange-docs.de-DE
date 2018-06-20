---
title: SenderSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: Das SenderSmtpAddress-Element darstellt, die SMTP-Adresse für das Postfach, das den Ordner enthält, der gemeinsam genutzt werden.
ms.openlocfilehash: 70905dd1ae2c3df18224aceeea246b542d1338e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831334"
---
# <a name="sendersmtpaddress"></a><span data-ttu-id="20164-103">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="20164-103">SenderSmtpAddress</span></span>

<span data-ttu-id="20164-104">Das **SenderSmtpAddress** -Element darstellt, die SMTP-Adresse für das Postfach, das den Ordner enthält, der gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="20164-104">The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared.</span></span> 
  
```xml
<SenderSmtpAddress/>
```

 <span data-ttu-id="20164-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="20164-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20164-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="20164-106">Attributes and elements</span></span>

<span data-ttu-id="20164-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="20164-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20164-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="20164-108">Attributes</span></span>

<span data-ttu-id="20164-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="20164-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20164-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20164-110">Child elements</span></span>

<span data-ttu-id="20164-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="20164-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20164-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="20164-112">Parent elements</span></span>

|<span data-ttu-id="20164-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="20164-113">**Element**</span></span>|<span data-ttu-id="20164-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20164-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="20164-115">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="20164-115">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="20164-116">Definiert eine Anforderung an ein undurchsichtiger Authentifizierungstoken erhalten möchten, die die Einladung zur Freigabe identifiziert.</span><span class="sxs-lookup"><span data-stu-id="20164-116">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="20164-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="20164-117">Text value</span></span>

<span data-ttu-id="20164-118">Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20164-118">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20164-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20164-119">Remarks</span></span>

<span data-ttu-id="20164-120">Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="20164-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20164-121">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="20164-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20164-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="20164-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="20164-123">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="20164-123">Schema Name</span></span>  <br/> |<span data-ttu-id="20164-124">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="20164-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="20164-125">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="20164-125">Validation File</span></span>  <br/> |<span data-ttu-id="20164-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="20164-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20164-127">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="20164-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="20164-128">False</span><span class="sxs-lookup"><span data-stu-id="20164-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20164-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20164-129">See also</span></span>



[<span data-ttu-id="20164-130">GetSharingMetadata-Vorgang</span><span class="sxs-lookup"><span data-stu-id="20164-130">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="20164-131">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="20164-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

