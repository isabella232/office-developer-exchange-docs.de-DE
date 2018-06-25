---
title: UserSid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserSid
api_type:
- schema
ms.assetid: f8a0dcd9-8564-4e35-b307-c5d2761b48d8
description: Das Element UserSid stellt Security Descriptor Definition Language (SDDL) Formular der Benutzer Sicherheits-ID in einem serialisierten Sicherheit Kontext SOAP-Header. Tokenserialisierung wird nicht unterstützt.
ms.openlocfilehash: 3c72f68638f99a4ee5081517027f0834ebf65b49
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839468"
---
# <a name="usersid"></a><span data-ttu-id="0a82a-104">UserSid</span><span class="sxs-lookup"><span data-stu-id="0a82a-104">UserSid</span></span>

<span data-ttu-id="0a82a-105">Das Element **UserSid** stellt Security Descriptor Definition Language (SDDL) Formular der Benutzer Sicherheits-ID in einem serialisierten Sicherheit Kontext SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="0a82a-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="0a82a-106">Tokenserialisierung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a82a-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="0a82a-107">**String**</span><span class="sxs-lookup"><span data-stu-id="0a82a-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a82a-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0a82a-108">Attributes and elements</span></span>

<span data-ttu-id="0a82a-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0a82a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a82a-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0a82a-110">Attributes</span></span>

<span data-ttu-id="0a82a-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a82a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a82a-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a82a-112">Child elements</span></span>

<span data-ttu-id="0a82a-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a82a-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a82a-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a82a-114">Parent elements</span></span>

|<span data-ttu-id="0a82a-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a82a-115">**Element**</span></span>|<span data-ttu-id="0a82a-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a82a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a82a-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="0a82a-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="0a82a-118">In den SOAP-Header verwendet für tokenserialisierung für Server-zu-Server-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="0a82a-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a82a-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="0a82a-119">Text value</span></span>

<span data-ttu-id="0a82a-120">Der Textwert stellt Sicherheits-ID des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="0a82a-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a82a-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a82a-121">Remarks</span></span>

<span data-ttu-id="0a82a-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0a82a-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a82a-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0a82a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a82a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a82a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a82a-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0a82a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0a82a-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0a82a-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a82a-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0a82a-127">Validation File</span></span>  <br/> |<span data-ttu-id="0a82a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a82a-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a82a-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0a82a-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a82a-130">False</span><span class="sxs-lookup"><span data-stu-id="0a82a-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a82a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a82a-131">See also</span></span>



- [<span data-ttu-id="0a82a-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="0a82a-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

