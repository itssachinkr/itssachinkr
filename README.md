- 👋 Hi, I’m Sachin
- 👀 I’m interested in Web Development, Competitive Programming
- 🌱 I’m currently learning React
<!--
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

<!---
itssachinkr/itssachinkr is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

```mermaid
flowchart TD
    A[Start] --> B[Initialize searchFields]
    A --> C[Initialize startDate and endDate]
    A --> D[Create base query]
    
    D --> E{Check for term}
    E -->|Yes| F[Extract terms into termList]
    F --> G[Create regex queries for each term]
    G --> H[Add to query $or]
    
    E -->|No| I{Check for stateFilter}
    I -->|Yes| J[Update query orderStatus]
    I -->|No| K{Check for orderId}
    
    K -->|Yes| L[Add orderId regex to query $or]
    K -->|No| M{Check for trackingId}
    
    M -->|Yes| N[Add trackingId regex to query $or]
    M -->|No| O{Check for city}
    
    O -->|Yes| P[Add city regex to query $or]
    O -->|No| Q{Check for deliveryPartnerName}
    
    Q -->|Yes| R[Add deliveryPartnerName regex to query $or]
    Q -->|No| S{Check for companyName}
    
    S -->|Yes| T[Add companyName regex to query $or]
    S -->|No| U{Check for deliveryPartnerNumber}
    
    U -->|Yes| V[Add deliveryPartnerNumber regex to query $or]
    U -->|No| W[Get order count]

    W --> X[Get orders with trips and sub-trips]
    X --> Y[Return response with status and data]
