# 🛒 Market Survey API

This is a RESTful API built with **Spring Boot 3**, **Java 24**, and **PostgreSQL**, deployable using **Railway**.

---

## 📌 Project Description

This project is a consumer satisfaction survey focused on the impact of basic food basket prices.<br>
Users respond with a simple **"Yes" or "No"** to indicate whether they have felt a difference in their monthly budget.<br>
It uses a new, clean data structure and modern backend stack to collect, store, and analyze responses.

---
## 🧭 Class Diagram (Mermaid)

``` mermaid
classDiagram
    class MarketResearch {
        +String project
        +String objective
        +String[] target_audience
        +String[] trends
        +String[] opportunities
        +String[] challenges
        +String conclusion
    }

    class Technologies {
        +String backend
        +String language
        +String deploy
        +String database
        +String[] protocols
    }

    class Competitor {
        +String name
        +String description
        +String[] advantages
        +String[] disadvantages
    }

    MarketResearch "1" --> "1" Technologies : uses
    MarketResearch "1" --> "*" Competitor : analyzes
    Competitor "*" --> "1" MarketResearch : influences
    Technologies "1" --> "1" MarketResearch : supports
    Competitor "*" --> "1" Technologies : compares_with
  

        
```

## ⚙️ Technologies Used

- Java 24
- Spring Boot 3.4.4
- PostgreSQL
- Railway (Cloud Deployment)
- Maven
- Mermaid for documentation 

---


