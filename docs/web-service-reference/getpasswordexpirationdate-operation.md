---
title: GetPasswordExpirationDate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: Der Vorgang GetPasswordExpirationDate enthält das Ablaufdatum des e-Mail-Konto ein Kennwort für den aktuellen Benutzer.
ms.openlocfilehash: c57942c88b09a910e2d529a12ea279bb2da5d693
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758758"
---
# <a name="getpasswordexpirationdate-operation"></a><span data-ttu-id="623d1-103">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="623d1-103">GetPasswordExpirationDate operation</span></span>

<span data-ttu-id="623d1-104">Der Vorgang **GetPasswordExpirationDate** enthält das Ablaufdatum des e-Mail-Konto ein Kennwort für den aktuellen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="623d1-104">The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user.</span></span> 
  
<span data-ttu-id="623d1-105">Dieser Vorgang wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="623d1-105">This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a><span data-ttu-id="623d1-106">GetPasswordExpirationDate Vorgang SOAP-Header</span><span class="sxs-lookup"><span data-stu-id="623d1-106">GetPasswordExpirationDate operation SOAP headers</span></span>

<span data-ttu-id="623d1-107">Der Vorgang **GetPasswordExpirationDate** können die SOAP-Header, die in der folgenden Tabelle aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="623d1-107">The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="623d1-108">**Header**</span><span class="sxs-lookup"><span data-stu-id="623d1-108">**Header**</span></span>|<span data-ttu-id="623d1-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="623d1-109">**Element**</span></span>|<span data-ttu-id="623d1-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="623d1-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="623d1-111">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="623d1-111">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="623d1-112">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="623d1-112">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="623d1-113">Bezeichnet die Kultur gemäß Definition in RFC 3066, "Tags for the Identification des Languages", um Zugriff auf das Postfach verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="623d1-113">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="623d1-114">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="623d1-114">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="623d1-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="623d1-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="623d1-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="623d1-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="623d1-117">Das Schema für die Anforderung Vorgang identifiziert.</span><span class="sxs-lookup"><span data-stu-id="623d1-117">Identifies the schema for the operation request.</span></span> <span data-ttu-id="623d1-118">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="623d1-118">This is applicable to a request.</span></span> <span data-ttu-id="623d1-119">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="623d1-119">This is applicable to a request.</span></span>  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a><span data-ttu-id="623d1-120">GetPasswordExpirationDate Vorgang anforderungsbeispiel</span><span class="sxs-lookup"><span data-stu-id="623d1-120">GetPasswordExpirationDate operation request example</span></span>

### <a name="description"></a><span data-ttu-id="623d1-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="623d1-121">Description</span></span>

<span data-ttu-id="623d1-122">Im folgenden Beispiel wird eine **GetPasswordExpirationDate** Vorgang Anforderung veranschaulicht, wie das Ablaufdatum Kennwort für ein e-Mail-Konto abrufen.</span><span class="sxs-lookup"><span data-stu-id="623d1-122">The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account.</span></span> 
  
### <a name="code"></a><span data-ttu-id="623d1-123">Code</span><span class="sxs-lookup"><span data-stu-id="623d1-123">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="623d1-124">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="623d1-124">Request elements</span></span>

<span data-ttu-id="623d1-125">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="623d1-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="623d1-126">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="623d1-126">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md)
    
- [<span data-ttu-id="623d1-127">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="623d1-127">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a><span data-ttu-id="623d1-128">Erfolgreiche GetPasswordExpirationDate Vorgangsantwort</span><span class="sxs-lookup"><span data-stu-id="623d1-128">Successful GetPasswordExpirationDate operation response</span></span>

<span data-ttu-id="623d1-129">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="623d1-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="623d1-130">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="623d1-130">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
    
- [<span data-ttu-id="623d1-131">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="623d1-131">PasswordExpirationDate</span></span>](passwordexpirationdate.md)
    

