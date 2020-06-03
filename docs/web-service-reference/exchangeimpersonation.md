---
title: ExchangeImpersonation
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
description: Das ExchangeImpersonation-Element wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das im ExchangeImpersonation-Element enthaltene Konto zu imitieren.
ms.openlocfilehash: 188219d95453dc45378c6ca65ab93c2de7db4eac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463349"
---
# <a name="exchangeimpersonation"></a><span data-ttu-id="75da5-104">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="75da5-104">ExchangeImpersonation</span></span>

<span data-ttu-id="75da5-105">Das **ExchangeImpersonation** -Element wird im SOAP-Header einer Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="75da5-105">The **ExchangeImpersonation** element is used in the SOAP header of a request.</span></span> <span data-ttu-id="75da5-106">Wenn dieses Element vorhanden ist, versucht der Aufrufer, das im **ExchangeImpersonation** -Element enthaltene Konto zu imitieren.</span><span class="sxs-lookup"><span data-stu-id="75da5-106">When this element is present, the caller is trying to impersonate the account that is contained within the **ExchangeImpersonation** element.</span></span> 
  
[<span data-ttu-id="75da5-107">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="75da5-107">ExchangeImpersonation</span></span>](exchangeimpersonation.md)
  
```xml
<ExchangeImpersonation>
   <ConnectingSID/>
</ExchangeImpersonation>
```

 <span data-ttu-id="75da5-108">**ExchangeImpersonationType**</span><span class="sxs-lookup"><span data-stu-id="75da5-108">**ExchangeImpersonationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75da5-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="75da5-109">Attributes and elements</span></span>

<span data-ttu-id="75da5-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="75da5-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75da5-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="75da5-111">Attributes</span></span>

<span data-ttu-id="75da5-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="75da5-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75da5-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75da5-113">Child elements</span></span>

|<span data-ttu-id="75da5-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="75da5-114">**Element**</span></span>|<span data-ttu-id="75da5-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75da5-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75da5-116">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="75da5-116">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="75da5-117">Stellt ein Konto für den Identitätswechsel dar, wenn Sie den SOAP-ExchangeImpersonation-Header verwenden.</span><span class="sxs-lookup"><span data-stu-id="75da5-117">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75da5-118">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75da5-118">Parent elements</span></span>

<span data-ttu-id="75da5-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="75da5-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75da5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75da5-120">Remarks</span></span>

<span data-ttu-id="75da5-121">Das Anruf Konto muss über das **ms-exch-impersonation** direkt auf dem Client Zugriffsserver und dem **MS-Wechsel-MayImpersonate** -direkt in der Postfachdatenbank, in der das Postfach enthalten ist, den Identitätswechsel oder das Benutzer-Kontaktobjekt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="75da5-121">The calling account must have the **ms-exch-impersonation** right on the Client Access server and the **ms-exch-MayImpersonate** right on either the mailbox database that contains the mailbox to impersonate or the Active Directory User/Contact object.</span></span> 
  
<span data-ttu-id="75da5-122">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="75da5-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75da5-123">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="75da5-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75da5-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="75da5-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75da5-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="75da5-125">Schema name</span></span>  <br/> |<span data-ttu-id="75da5-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="75da5-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="75da5-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="75da5-127">Validation file</span></span>  <br/> |<span data-ttu-id="75da5-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75da5-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75da5-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="75da5-129">Can be empty</span></span>  <br/> |<span data-ttu-id="75da5-130">False</span><span class="sxs-lookup"><span data-stu-id="75da5-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75da5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75da5-131">See also</span></span>



[<span data-ttu-id="75da5-132">Server-zu-Server-Autorisierung in EWS</span><span class="sxs-lookup"><span data-stu-id="75da5-132">Server-to-server authorization in EWS</span></span>](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

