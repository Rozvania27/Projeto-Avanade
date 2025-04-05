# 🛒 Market Survey API

This is a RESTful API built with **Spring Boot 3**, **Java 24**, and **PostgreSQL**, deployable using **Railway**.

---

## 📌 Project Description

This project is a consumer satisfaction survey focused on the **impact of basic food basket prices**. Users respond with a **simple "Yes" or "No"** to indicate whether they have felt a difference in their monthly budget.

It uses a new, clean data structure and modern backend stack to collect, store, and analyze responses.

---
## 🧭 Class Diagram (Mermaid)

``` mermaid
classDiagram
    class SurveyResponse {
        +Long id
        +String consumerName
        +Boolean feltDifference
        +LocalDateTime responseDate
    }

    class SurveyResponseRepository {
        <<interface>>
        +List~SurveyResponse~ findAll()
        +SurveyResponse save(SurveyResponse response)
    }

    class SurveyResponseService {
        -SurveyResponseRepository repository
        +List~SurveyResponse~ listAll()
        +SurveyResponse save(SurveyResponse response)
        +long countYes()
        +long countNo()
    }

    class SurveyResponseController {
        -SurveyResponseService service
        +List~SurveyResponse~ getAll()
        +SurveyResponse submit(SurveyResponse response)
        +Map~String, Long~ getStats()
    }

    SurveyResponseService --> SurveyResponseRepository
    SurveyResponseController --> SurveyResponseService
```

## ⚙️ Technologies Used

- Java 24  
- Spring Boot 3  
- PostgreSQL  
- Railway (Cloud Deployment)  
- Maven  
- Lombok  

---

## 🚀 How to Run Locally

```bash
git clone https://github.com/your-user/market-survey-api.git
cd market-survey-api
