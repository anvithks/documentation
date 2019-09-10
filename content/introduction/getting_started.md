---
title: Getting Started
description: "Quick access links to tutorials and concepts."
weight: 10
disableToc: true
---
### Sample File Share design flow chart

{{<mermaid align="left">}}
graph LR;
    A[NBP] -->|POST /file/share -> create| B(<span>API Server </span><br /> File Share Standard API)
    B --> |Identifies Parameters| C{Controller}
    C -->|Chooses Profile| D[Dock <br/> Specific Driver]
    C -->|File Share Metadata| E((DB))
{{</mermaid>}}

### Sample Sequence diagram for Multi-Cloud AK/SK Management  

{{<mermaid  align="left">}}
sequenceDiagram
    User ->> Keystone: 1. Send Request
    Keystone ->> User: 2. Receive Token
    User ->> MultiCloud API Handler: 3. Send Request and Signature
    MultiCloud API Handler ->> Keystone: 4. Validate Signature
    MultiCloud API Handler ->> User: 5. Receive Response
{{</mermaid>}}