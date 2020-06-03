---
title: GetPasswordExpirationDate-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b0297458-58fb-4e5d-bb47-0cd17155e106
description: Der GetPasswordExpirationDate-Vorgang stellt das Ablaufdatum des e-Mail-Kontokennworts für den aktuellen Benutzer bereit.
ms.openlocfilehash: 4184092cf98161e4c2f74446cef5439722ae71a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457893"
---
# <a name="getpasswordexpirationdate-operation"></a><span data-ttu-id="b751e-103">GetPasswordExpirationDate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b751e-103">GetPasswordExpirationDate operation</span></span>

<span data-ttu-id="b751e-104">Der **GetPasswordExpirationDate** -Vorgang stellt das Ablaufdatum des e-Mail-Kontokennworts für den aktuellen Benutzer bereit.</span><span class="sxs-lookup"><span data-stu-id="b751e-104">The **GetPasswordExpirationDate** operation provides the email account password expiration date for the current user.</span></span> 
  
<span data-ttu-id="b751e-105">Dieser Vorgang wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b751e-105">This operation was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="getpasswordexpirationdate-operation-soap-headers"></a><span data-ttu-id="b751e-106">SOAP-Header des GetPasswordExpirationDate-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="b751e-106">GetPasswordExpirationDate operation SOAP headers</span></span>

<span data-ttu-id="b751e-107">Der **GetPasswordExpirationDate** -Vorgang kann die SOAP-Header verwenden, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b751e-107">The **GetPasswordExpirationDate** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="b751e-108">**Header**</span><span class="sxs-lookup"><span data-stu-id="b751e-108">**Header**</span></span>|<span data-ttu-id="b751e-109">**Element**</span><span class="sxs-lookup"><span data-stu-id="b751e-109">**Element**</span></span>|<span data-ttu-id="b751e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b751e-110">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b751e-111">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="b751e-111">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="b751e-112">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="b751e-112">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="b751e-113">Identifiziert die Kultur gemäß der Definition in RFC 3066, "Tags für die Identifizierung von Sprachen", die für den Zugriff auf das Postfach verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b751e-113">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span> <span data-ttu-id="b751e-114">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b751e-114">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="b751e-115">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="b751e-115">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="b751e-116">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="b751e-116">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="b751e-117">Gibt das Schema für die Vorgangsanforderung an.</span><span class="sxs-lookup"><span data-stu-id="b751e-117">Identifies the schema for the operation request.</span></span> <span data-ttu-id="b751e-118">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b751e-118">This is applicable to a request.</span></span> <span data-ttu-id="b751e-119">Dies gilt für eine Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b751e-119">This is applicable to a request.</span></span>  <br/> |
   
## <a name="getpasswordexpirationdate-operation-request-example"></a><span data-ttu-id="b751e-120">GetPasswordExpirationDate-Vorgangsanforderung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="b751e-120">GetPasswordExpirationDate operation request example</span></span>

### <a name="description"></a><span data-ttu-id="b751e-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b751e-121">Description</span></span>

<span data-ttu-id="b751e-122">Im folgenden Beispiel einer **GetPasswordExpirationDate** -Vorgangsanforderung wird gezeigt, wie das Kennwortablaufdatum für ein e-Mail-Konto abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b751e-122">The following example of a **GetPasswordExpirationDate** operation request shows how to get the password expiration date for an email account.</span></span> 
  
### <a name="code"></a><span data-ttu-id="b751e-123">Code</span><span class="sxs-lookup"><span data-stu-id="b751e-123">Code</span></span>

```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
  </soap:Header>
  <soap:Body>
    <tns:GetPasswordExpirationDate>
      <tns:MailboxSmtpAddress>user1@DTZMZX-dom.extest.microsoft.com</tns:MailboxSmtpAddress>
    </tns:GetPasswordExpirationDate>
  </soap:Body>
</soap:Envelope>

```

### <a name="request-elements"></a><span data-ttu-id="b751e-124">Anfordern von Elementen</span><span class="sxs-lookup"><span data-stu-id="b751e-124">Request elements</span></span>

<span data-ttu-id="b751e-125">In der Anforderung werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="b751e-125">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="b751e-126">GetPasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="b751e-126">GetPasswordExpirationDate</span></span>](getpasswordexpirationdate.md)
    
- [<span data-ttu-id="b751e-127">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b751e-127">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md)
    
## <a name="successful-getpasswordexpirationdate-operation-response"></a><span data-ttu-id="b751e-128">Erfolgreiche Reaktion des GetPasswordExpirationDate-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="b751e-128">Successful GetPasswordExpirationDate operation response</span></span>

<span data-ttu-id="b751e-129">In der Antwort werden folgende Elemente verwendet:</span><span class="sxs-lookup"><span data-stu-id="b751e-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="b751e-130">GetPasswordExpirationDateResponse</span><span class="sxs-lookup"><span data-stu-id="b751e-130">GetPasswordExpirationDateResponse</span></span>](getpasswordexpirationdateresponse.md)
    
- [<span data-ttu-id="b751e-131">PasswordExpirationDate</span><span class="sxs-lookup"><span data-stu-id="b751e-131">PasswordExpirationDate</span></span>](passwordexpirationdate.md)
    

