# Fluent X Design
## Windows 11 Fluent/Mica Design Implementation for X (formerly Twitter)

**Document Version:** 1.0.0
**Release Status:** Final Release — Authoritative Version
**Effective Date:** 11 November 2026
**Copyright Holder:** Heyan Vieira Minuto
**License:** Business Source License 1.1 (BSL-1.1)
**Jurisdiction:** Republic of Italy — Civil Code, Articles 2575 et seq.

---

## TABLE OF CONTENTS
1. [PRODUCT OVERVIEW](#1-product-overview)
2. [SYSTEM REQUIREMENTS](#2-system-requirements)
3. [INSTALLATION PROCEDURE](#3-installation-procedure)
4. [MANIFEST V3 BROWSERS — PERMISSION CONFIGURATION](#4-manifest-v3-browsers--permission-configuration)
5. [DEFAULT SPECIFICATIONS](#5-default-specifications)
6. [LICENSE DOCUMENT — FULL TEXT](https://github.com/heyanvminuto/FluentX-Theme/blob/main/README.md#6-license-document--full-text)
7. [ACKNOWLEDGMENTS AND THIRD-PARTY NOTICES](#7-acknowledgments-and-third-party-notices)

---

## 1. PRODUCT OVERVIEW

Fluent X Design is a comprehensive user interface enhancement system for the X/Twitter web platform, implementing the Windows 11 Fluent/Mica design language. This work comprises an adaptive visual styling framework, dynamic background rendering system, custom colour management configuration, typography standardization, and supplementary user experience optimizations.

### 1.1 Functional Features
| Feature | Specification |
|---|---|
| Background Rendering | Fluent/Mica visual style — enabled by default |
| Primary Theme Colour | `#2d7d9a` — RGB(45, 125, 154) |
| Pop-up Element Background | Solid opaque white — `#ffffff` |
| Background Blur Effect | Disabled by default |
| Primary Typeface | Segoe UI — Windows native interface font |
| Premium Content Visibility | Hidden by default |
| Grok Interface Visibility | Hidden by default |
| Configuration Interface | Fully configurable via Stylus extension settings panel |

---

## 2. SYSTEM REQUIREMENTS

### 2.1 Supported Environments
- **Web Browsers:** Google Chrome (v88+), Mozilla Firefox (v90+), Microsoft Edge (v88+), Opera (v74+), Brave Browser
- **Required Software:** Stylus — User Style Manager Extension
  - Chrome/Edge/Brave/Opera Extension Identifier: `clngdbkpkpeebahjckkjfobafhncgmne`
  - Firefox Extension Identifier: `styl-us@openstyles.github.io`
- **Network Protocol:** Hypertext Transfer Protocol Secure (HTTPS)

---

## 3. INSTALLATION PROCEDURE

### 3.1 Pre-Installation
1. Acquire and install the Stylus browser extension from the appropriate official extension repository
2. Restart the browser application to ensure full extension initialization

### 3.2 Deployment
1. Navigate to the target domain: `https://x.com` or `https://twitter.com`
2. Activate the Stylus extension interface via the browser toolbar icon
3. Select the option: **"Write style for x.com"**
4. Remove any pre-existing content within the code editor area
5. Input the complete contents of the file `fluentx-design.user.css` into the editor
6. Select the **Save** command to persist the configuration
7. Verify successful application by inspecting the rendered interface

### 3.3 Post-Installation Configuration
Access the configuration panel by selecting the gear icon (⚙️) adjacent to the Fluent X Design entry within the Stylus interface. All customizable parameters are presented with real-time preview functionality.

---

## 4. MANIFEST V3 BROWSERS — PERMISSION CONFIGURATION

### 4.1 Applicability
This section applies exclusively to browsers implementing the **Web Extension Manifest V3** specification (including, but not limited to, Google Chrome, Microsoft Edge, Opera, and Brave Browser). Manifest V3 restricts certain network request operations by default, which may impact the proper functioning of custom styles that modify Content Security Policy (CSP) headers.

### 4.2 Requirement
Fluent X Design may require the **"Patch CSP"** functionality to be enabled within Stylus. This capability requires the `webRequestBlocking` permission, which is subject to additional authorization procedures under Manifest V3 constraints.

>  **Notice:** The following methods require elevated browser configuration privileges. Proceed only with appropriate authorization and an understanding of browser security implications.

---

### METHOD 1 — Extension Installation Policy Configuration

This method is recommended for managed environments and enterprise deployments.

**Step 1 — Export Existing Configuration**
1. Open the Stylus management interface
2. Navigate to **Settings → Backup → Export Backup**
3. Store the generated backup file in a secure location

**Step 2 — Configure Enterprise Policy**
1. Access your browser's enterprise policy configuration directory:
   - **Windows Registry:** `HKEY_LOCAL_MACHINE\Software\Policies\Google\Chrome\ExtensionInstallForcelist`
   - **macOS Profile:** `com.google.Chrome` → `ExtensionInstallForcelist`
   - **Linux:** `/etc/opt/chrome/policies/managed/`
2. Create or modify the policy list to include the Stylus extension identifier:
clngdbkpkpeebahjckkjfobafhncgmne;https://clients2.google.com/service/update2/crx

3. Enforce the policy configuration

**Step 3 — Restart Browser Application**
1. Terminate all running instances of the browser application
2. Re-launch the browser — verify the policy has been applied by navigating to:
- `chrome://policy` (Chrome/Edge/Brave)
- Confirm status: **ExtensionInstallForcelist** — Active

**Step 4 — Import Configuration and Complete Setup**
1. Open Stylus → **Settings → Backup → Import Backup**
2. Select the previously exported backup file
3. Navigate to Stylus Settings → locate **"Patch CSP"** → toggle to **Enabled**
4. Optionally, pin the Stylus icon to the browser toolbar for accessibility

---

### METHOD 2 — Command-Line Initialization Parameters

This method is suitable for individual workstations and non-managed environments.

**Step 1 — Modify Browser Launch Configuration**
1. Locate the browser application shortcut or executable launcher
2. Open the shortcut properties (right-click → Properties)
3. In the **Target** field, append the following parameter to the end of the existing path: --allowlisted-extension-id=clngdbkpkpeebahjckkjfobafhncgmne

**Example (Windows):** "C:\Program Files\Google\Chrome\Application\chrome.exe" --allowlisted-extension-id=clngdbkpkpeebahjckkjfobafhncgmne"
**Example (macOS — Terminal):**
open -a "Google Chrome" --args --allowlisted-extension-id=clngdbkpkpeebahjckkjfobafhncgmne
**Example (Linux — Terminal):**
google-chrome --allowlisted-extension-id=clngdbkpkpeebahjckkjfobafhncgmne


**Step 2 — Restart Browser Application**
1. Close all browser windows and terminate all background processes
2. Re-launch the browser using the modified shortcut/command

**Step 3 — Enable Patch CSP Functionality**
1. Open Stylus → **Settings**
2. Locate the option labelled **"Patch CSP"**
3. Toggle the setting to **Enabled**
4. Refresh the X/Twitter interface — the warning notification should no longer appear

---

### 4.3 Verification Procedure
To confirm successful configuration:
1. Navigate to the X/Twitter platform
2. Open Stylus → Settings
3. Confirm **"Patch CSP"** displays as **Enabled**
4. No permission-related notification shall be presented upon initial style application

---

## 5. DEFAULT SPECIFICATIONS

| Configuration Parameter | Preset Value |
|---|---|
| Background Source | Fluent / Mica |
| Background Overlay Opacity | `#000000b3` — 70% opacity |
| Background Blur | Disabled |
| Pop-up Background Colour | `#ffffff` — Solid White, 100% opacity |
| Primary Theme Colour | `#2d7d9a` — RGB(45, 125, 154) |
| Interface Icon | Standard X Logo |
| Typeface Family | Segoe UI |
| Premium Interface Elements | Hidden |
| Grok Interface Elements | Hidden |
| Explore Navigation Item | Visible |
| Communities Navigation Item | Visible |
| Lists Navigation Item | Visible |
| Calls Navigation Item | Hidden |
| Creator Studio Navigation Item | Hidden |

All parameters may be modified within the Stylus configuration panel following installation.

---

## 6. LICENSE DOCUMENT — FULL TEXT

Document Identifier:  LICENSE-FXD-2026-11-11-v1.0
Work Designation:     Fluent X Design
License Classification: Business Source License 1.1
Effective Date:       11 November 2026, 00:00 UTC
Jurisdiction:         Republic of Italy — Civil Code, Articles 2575 et seq.
Governing Law:        Italian Law; International Copyright Conventions
                      (Berne Convention, Paris Act 1971);
                      WIPO Copyright Treaty (1996);
                      EU Directive 2001/29/EC;
                      EU Directive 2019/790/EU


For all matters pertaining to this Work, including but not limited to:
licensing inquiries, commercial usage authorization, derivative distribution
permission, permissions beyond the Additional Use Grant, correspondence
regarding license compliance, and all other official communications:

  PRIMARY CORRESPONDENCE CHANNELS:
**1. TELECOMMUNICATIONS — VOICE, SMS, RCS AND WHATSAPP**

- Number: +39 379 225 0408
- Services: Voice calls, Short Message Service (SMS), Rich Communication Services (RCS), WhatsApp text and multimedia messaging
- WhatsApp: [https://wa.me/qr/CZ4ZK7CMFZRQB1?s=v](https://wa.me/qr/CZ4ZK7CMFZRQB1?s=v)
- Availability: Standard Central European Time (CET/CEST) business hours

---

**2. TELEGRAM INSTANT MESSAGING**

- Username: @heyanvminuto
- URL: [https://t.me/heyanvminuto](https://t.me/heyanvminuto)
- Protocol: Telegram Messenger Platform

---

**3. ELECTRONIC MAIL — PRIMARY**

- Address: [heyanvnm@outlook.com](mailto:heyanvnm@outlook.com)
- Protocol: SMTP / MIME
- Encryption: TLS recommended for all transmissions

---

**4. ELECTRONIC MAIL — SECONDARY**

- Address: [vieiraminutoheyan@gmail.com](mailto:vieiraminutoheyan@gmail.com)
- Protocol: SMTP / MIME
- Encryption: TLS recommended for all transmissions

---

**5. X (FORMERLY TWITTER) — DIRECT MESSAGING**

- Handle: @heyanvminuto
- Platform: X Corp. Direct Messaging System

  CORRESPONDENCE GUIDELINES:
    • All written requests for commercial use or derivative distribution
      permission must include: full legal name of requester, organizational
      affiliation (if applicable), intended use case, scope of deployment,
      estimated user volume, and duration of intended usage.
    • Authorization granted via one channel is valid across all channels
      provided the written record is preserved.
    • Response timeframes: Inquiries will be acknowledged within 14 calendar
      days; substantive responses provided within 30 calendar days where
      reasonably possible.


    BUSINESS SOURCE LICENSE VERSION 1.1
    Official License Text — Reference Copy
    Source: https://mariadb.com/bsl11/
    Copyright © 2023 MariaDB plc


DEFINITIONS

  "License"          Means this Business Source License 1.1 document,
                     including all Appendices, Parameters, and Additional
                     Use Grant set forth herein.

  "Licensed Work"    Means the work identified as Fluent X Design, including
                     all original code files, style definitions, configuration
                     interfaces, documentation, visual assets, and design
                     specifications made available under this License, together
                     with all partial copies, excerpts, and derivative
                     adaptations thereof.

  "Effective Date"   Means the date first set forth above as the effective
                     commencement of this License: 2026-11-11.

  "Change Date"      Means the specific future date upon which certain
                     restrictions under this License shall expire and the
                     Work shall become available under the Change License
                     identified herein: 2194-01-01.

  "Change License"   Means the license terms that shall apply to the
                     Licensed Work on and after the Change Date:
                     MIT License — https://opensource.org/licenses/MIT

  "Licensor"         Means Heyan Vieira Minuto, the holder of the
                     copyright and other proprietary rights in the
                     Licensed Work.

  "You" or "Your"    Means the individual person or legal entity
                     exercising permissions granted by this License.

  "Use" or "Using"   Means to access, download, install, copy, store,
                     execute, display, run, modify, adapt, translate,
                     redistribute, or otherwise exploit the Work in any
                     manner whatsoever.

  "Derivative Work"  Means any modification, adaptation, enhancement, or
                     derivative of the Licensed Work, whether in whole or
                     in part, including any work that incorporates all or
                     a portion of the Licensed Work, regardless of the
                     extent of modification made.

  "Commercial Use"   Means any use that generates revenue, facilitates
                     business operations, provides service to third parties
                     in exchange for consideration, or is undertaken for
                     purposes of commercial advantage or monetary
                     compensation of any kind whatsoever.

LICENSE PARAMETERS

  A. Licensed Work:        Fluent X Design
  B. Effective Date:       2026-11-11
  C. Change Date:          2194-01-01
  D. Change License:       MIT License
  E. Licensor Contact:     Heyan Vieira Minuto — contact details above

ADDITIONAL USE GRANT

  Subject to the terms, conditions, and limitations set forth in this
  License, the Licensor hereby grants to You a limited, non-exclusive,
  non-transferable, revocable permission to exercise the following
  rights:

  1. PERSONAL NON-COMMERCIAL USE
     You may view, download, install, and execute copies of the
     Licensed Work solely for Your own personal, private, and
     non-commercial enjoyment. No fee, subscription, or consideration
     of any kind may be charged or accepted in connection with
     such usage.

  2. PERSONAL MODIFICATION RIGHTS
     You may create modifications and adaptations of the Licensed
     Work solely for Your own personal, non-commercial use and
     benefit. Such modifications may not be distributed, shared,
     published, displayed publicly, or used for any purpose beyond
     Your individual private usage.

  3. UNMODIFIED REDISTRIBUTION
     You may reproduce and distribute verbatim, complete, and
     unaltered copies of the Licensed Work to third parties,
     provided that:
       a. This entire License document is reproduced in full,
          without omission or alteration;
       b. No compensation, donation request, or revenue generation
          mechanism is associated with the distribution;
       c. The source of the Work and attribution information
          remain clearly visible and intact;
       d. Recipients are notified of and agree to the terms
          of this License.

  4. RESERVATION OF ALL OTHER RIGHTS
     All rights not explicitly and expressly granted in this
     Additional Use Grant are strictly reserved to the Licensor.
     No implication, estoppel, or silent permission shall be
     construed from the mere publication or availability of
     the Work. Specifically, and without limiting the generality
     of the foregoing:
       a. You MAY NOT distribute modified or derivative works
          publicly or to third parties without prior written
          authorization from the Licensor;
       b. You MAY NOT use the Work or any derivative in or for
          any commercial context, business activity, or
          service offering without prior written commercial
          license from the Licensor;
       c. You MAY NOT sub-license, sell, rent, lease, or
          transfer the Work or Your rights hereunder to
          any third party;
       d. You MAY NOT remove, alter, or obscure any copyright
          notice, attribution, watermark, or license identifier
          contained within the Work.

LICENSE TERMS AND CONDITIONS

1. GRANT OF RIGHTS AND OWNERSHIP

  Subject to the timely and full observance of all terms and conditions
  contained herein, the Licensor grants to You the limited permissions
  explicitly described in the Additional Use Grant. All intellectual
  property rights, including copyright, moral rights, database rights,
  and all other proprietary interests in and to the Licensed Work,
  remain and shall remain the exclusive property of the Licensor and
  respective third-party contributors where applicable. Nothing in this
  License constitutes a transfer of title or ownership rights.

2. CHANGE OF LICENSE TERMS — FUTURE CONVERSION

  Effective upon the earlier of:
    (a) The Change Date specified herein: 2194-01-01; OR
    (b) The fourth anniversary of the first public release of this
        specific version of the Licensed Work by the Licensor;

  then, and only then, the restrictions contained in this License
  shall terminate, and the Licensed Work shall thereafter be made
  available under the terms of the Change License identified above.
  Upon such conversion, the full text of the Change License shall
  supersede this document with respect to future usage, but shall
  not retroactively validate any infringement occurring prior to
  the Change Date. No representation or warranty is made that
  conversion will occur at a specific time or that the Work will
  remain available in its current form until that date.

3. COMPLIANCE, ENFORCEMENT, AND COMMERCIAL LICENSING

  Any use of the Licensed Work outside the scope of the Additional
  Use Grant, or in violation of any term herein, constitutes a
  material breach of this License and terminates all permissions
  granted hereunder. In the event of such breach, You must:
    (a) Immediately cease all use and destroy all copies in
        Your possession or control; AND
    (b) Where applicable, obtain a valid commercial license
        directly from the Licensor through contact channels
        provided above; AND
    (c) Remain liable for all usage prior to cessation and
        for any unauthorized distribution that has occurred.

  Commercial licenses, permissions for derivative distribution,
  and waivers of usage restrictions may be granted by the
  Licensor in writing, in its sole discretion, and under such
  terms and compensation arrangements as may be mutually
  agreed in writing.

4. DISTRIBUTION AND COPY REQUIREMENTS

  Every copy of the Licensed Work, in whole or in part, including
  verbatim copies and excerpts, must reproduce this License document
  in its entirety, without modification, deletion, or alteration.
  This requirement applies equally to distribution in source form,
  embedded form, aggregated collections, and documentation. If You
  receive the Work from a third party, the terms of this License
  apply to Your possession and use regardless of whether the
  third party complied with distribution requirements.

5. DERIVATIVE WORKS AND CONTRIBUTIONS

  You may create derivative adaptations for Your own personal
  non-commercial use as permitted in Section 2 of the Additional
  Use Grant. You are not required to share or publish such
  adaptations. Any voluntary contribution, feedback, suggestion,
  or improvement communicated to the Licensor shall be deemed
  non-confidential and non-proprietary, and the Licensor shall
  have the perpetual, worldwide, royalty-free right to use,
  incorporate, and exploit such contributions in the Work without
  restriction or obligation.

6. TRADEMARKS AND BRANDING

  This License does not grant permission to use the trade names,
  trademarks, service marks, product names, or designations of
  the Licensor, even if they appear in the Work, except as
  reasonably necessary to describe the origin and authorship
  of the Work in unmodified redistributions.

7. NO WARRANTY AND LIMITATION OF LIABILITY

  THE LICENSED WORK IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY
  KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
  WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE,
  AND NONINFRINGEMENT. IN NO EVENT SHALL THE LICENSOR BE LIABLE
  FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION
  OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN
  CONNECTION WITH THE WORK OR THE USE OR OTHER DEALINGS IN THE
  WORK. ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE
  WORK IS WITH YOU. SHOULD THE WORK PROVE DEFECTIVE, YOU ASSUME
  THE COST OF ALL NECESSARY SERVICING, REPAIR, OR CORRECTION.

8. TERMINATION AND SURVIVAL

  This License shall automatically terminate if You violate any
  material term contained herein. Upon termination, You must
  cease all use and destroy all copies of the Work in Your
  possession. Sections 3 through 8 inclusive shall survive
  termination of this License indefinitely, as shall all
  provisions protecting the Licensor's intellectual property
  rights and limitations of liability.

9. INTERPRETATION AND SEVERABILITY

  This License shall be interpreted under the laws of the
  Republic of Italy. If any provision herein is found to be
  unenforceable or invalid, such provision shall be limited to
  the minimum extent necessary to be valid, and the remaining
  provisions shall remain in full legal force and effect. The
  headings used herein are for organizational convenience
  only and shall not be used to construe the intent of
  any provision.


                     **THIRD-PARTY COMPONENT NOTICES**


This Work incorporates components from external projects, each of which is
owned by their respective authors and made available under their original
licensing terms. These third-party components remain the property of their
respective copyright holders and are not subject to the Business Source
License 1.1 restrictions set forth above. Your use of these components
is governed exclusively by their respective license terms reproduced below.

------------------------------------------------------------------------------
COMPONENT 1 :**Xcellent**


  Original Work:   Xcellent
  Author:          Himither
  Repository:      [https://github.com/Himither/Xcellent](https://github.com/Himither/Xcellent)
  License:         MIT License
  Date Acquired:   2026-11-11

  MIT License

  Copyright (c) 2024 Himither

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.

------------------------------------------------------------------------------
COMPONENT 2: Customizable X
------------------------------------------------------------------------------

  Original Work:   Customizable X
  Author:          birb-naise
  Source Location: Included in this aggregation
  License:         MIT License
  Date Acquired:   2026-11-11

  MIT License

  Copyright (c) 2026 birb-naise

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.

------------------------------------------------------------------------------
SEVERABILITY AND INTERPRETATION
------------------------------------------------------------------------------

  In the event that any term, condition, or restriction contained in the
  Business Source License 1.1 portion of this document is found to conflict
  with the license terms applicable to these third-party components, the
  terms of the respective MIT License shall prevail solely with respect to
  the specific third-party component to which they apply. No provision of
  the BSL-1.1 shall be construed to restrict usage of the MIT-licensed
  components beyond what their original authors have expressly permitted.

  By using, copying, modifying, or reading this Work, You acknowledge that You
  have read, understood, and agree to be bound by the terms and conditions set
  forth in this document. If You do not agree to these terms, You must cease
  all use and remove all copies of this Work from Your possession immediately.
  
  This document, including all appendices, contact information, and license
  text, constitutes the complete and legally binding agreement between the
  parties concerning the Work herein and supersedes all prior communications,
  understandings, or agreements, whether oral or written.
  
  IN WITNESS WHEREOF, the Licensor has caused this License document to be
  prepared and published as of the Effective Date first written above.

  
                             **END OF LICENSE & DISCLAIMER**


---

## 7. ACKNOWLEDGMENTS AND THIRD-PARTY NOTICES

This work incorporates components from externally maintained projects, each governed by their respective license agreements. No proprietary rights are claimed over third-party components.

| Project Identifier | Principal Author | License Reference | Repository Location |
|---|---|---|---|
| Xcellent | Himither | MIT License | https://github.com/Himither/Xcellent |
| Customizable X | birb-naise | MIT License | Included in this distribution |

For the full text of third-party license agreements, please refer to the respective project repositories or contact the original authors.

---

**Document End — Fluent X Design — README — v1.0 — 2026-11-11**
