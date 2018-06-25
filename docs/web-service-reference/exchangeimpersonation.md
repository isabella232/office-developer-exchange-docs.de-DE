---
title: "\"ExchangeImpersonation\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExchangeImpersonation
api_type:
- schema
ms.assetid: d8cbac49-47d0-4745-a2a7-545d33f8da93
description: Das Element "ExchangeImpersonation" wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der "ExchangeImpersonation"-Element enthalten ist.
ms.openlocfilehash: aedeff22cda865ce1eec80dab9760d49fdc178f7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758299"
---
# <a name="exchangeimpersonation"></a><span data-ttu-id="d829e-104">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="d829e-104">ExchangeImpersonation</span></span>

<span data-ttu-id="d829e-105">Das Element **"ExchangeImpersonation"** wird im SOAP-Header einer Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d829e-105">The **ExchangeImpersonation** element is used in the SOAP header of a request.</span></span> <span data-ttu-id="d829e-106">Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der **"ExchangeImpersonation"** -Element enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d829e-106">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span> 
  
[<span data-ttu-id="d829e-107">"ExchangeImpersonation"</span><span class="sxs-lookup"><span data-stu-id="d829e-107">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 <span data-ttu-id="d829e-108">**ExchangeImpersonationType**</span><span class="sxs-lookup"><span data-stu-id="d829e-108">**ExchangeImpersonationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d829e-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d829e-109">Attributes and elements</span></span>

<span data-ttu-id="d829e-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d829e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d829e-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d829e-111">Attributes</span></span>

<span data-ttu-id="d829e-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d829e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d829e-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d829e-113">Child elements</span></span>

|<span data-ttu-id="d829e-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="d829e-114">**Element**</span></span>|<span data-ttu-id="d829e-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d829e-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d829e-116">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="d829e-116">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="d829e-117">Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.</span><span class="sxs-lookup"><span data-stu-id="d829e-117">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d829e-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d829e-118">Parent elements</span></span>

<span data-ttu-id="d829e-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d829e-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d829e-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d829e-120">Remarks</span></span>

<span data-ttu-id="d829e-121">Das aufrufende Konto muss die **ms-Exch-Impersonation** direkt auf dem Clientzugriffsserver und das **ms-Exch-MayImpersonate** Recht auf entweder haben die Postfachdatenbank, die das Postfach Identität enthält oder den Active Directory-Benutzer/Kontakt -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d829e-121">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory User/Contact object.</span></span> 
  
<span data-ttu-id="d829e-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d829e-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d829e-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d829e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d829e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="d829e-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d829e-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d829e-125">Schema name</span></span>  <br/> |<span data-ttu-id="d829e-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d829e-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="d829e-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d829e-127">Validation file</span></span>  <br/> |<span data-ttu-id="d829e-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d829e-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d829e-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d829e-129">Can be empty</span></span>  <br/> |<span data-ttu-id="d829e-130">False</span><span class="sxs-lookup"><span data-stu-id="d829e-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d829e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d829e-131">See also</span></span>



[<span data-ttu-id="d829e-132">Server-zu-Server-Autorisierung in Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="d829e-132">Server-to-server authorization in EWS</span></span>](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

