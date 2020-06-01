---
title: UserSID
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
description: Das users-Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar. Die Serialisierung von Token wird nicht unterstützt.
ms.openlocfilehash: b8ee51b1998546fc4ab14bd3666192ae63c8dba8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462017"
---
# <a name="usersid"></a><span data-ttu-id="d6010-104">UserSID</span><span class="sxs-lookup"><span data-stu-id="d6010-104">UserSid</span></span>

<span data-ttu-id="d6010-105">Das **Users** -Element stellt das SDDL-Formular (Security Descriptor Definition Language) der Benutzer Sicherheits-ID in einem serialisierten Sicherheitskontext-SOAP-Header dar.</span><span class="sxs-lookup"><span data-stu-id="d6010-105">The **UserSid** element represents the security descriptor definition language (SDDL) form of the user security identifier in a serialized security context SOAP header.</span></span> <span data-ttu-id="d6010-106">Die Serialisierung von Token wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6010-106">Token serialization is not supported.</span></span> 
  
```xml
<UserSid/>
```

 <span data-ttu-id="d6010-107">**String**</span><span class="sxs-lookup"><span data-stu-id="d6010-107">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d6010-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6010-108">Attributes and elements</span></span>

<span data-ttu-id="d6010-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6010-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6010-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6010-110">Attributes</span></span>

<span data-ttu-id="d6010-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6010-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6010-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6010-112">Child elements</span></span>

<span data-ttu-id="d6010-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6010-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6010-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6010-114">Parent elements</span></span>

|<span data-ttu-id="d6010-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6010-115">**Element**</span></span>|<span data-ttu-id="d6010-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6010-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6010-117">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="d6010-117">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="d6010-118">Wird im SOAP-Header für die Token-Serialisierung in der Server-zu-Server-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6010-118">Used in the SOAP header for token serialization in server-to-server authentication.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d6010-119">Textwert</span><span class="sxs-lookup"><span data-stu-id="d6010-119">Text value</span></span>

<span data-ttu-id="d6010-120">Der Wert Text stellt die Sicherheits-ID eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="d6010-120">The text value represents a user's security identifier.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6010-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6010-121">Remarks</span></span>

<span data-ttu-id="d6010-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6010-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6010-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d6010-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6010-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6010-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6010-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6010-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d6010-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d6010-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6010-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6010-127">Validation File</span></span>  <br/> |<span data-ttu-id="d6010-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6010-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6010-129">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d6010-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6010-130">False</span><span class="sxs-lookup"><span data-stu-id="d6010-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6010-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6010-131">See also</span></span>



- [<span data-ttu-id="d6010-132">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d6010-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

