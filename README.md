# Logistics & Fleet Management System 2025

## 1. Жобаны басқару (Management)
* **Әдістеме:** Scrumban (Scrum + Kanban)
* **Құралдар:** GitHub Projects (Milestones & Labels)
* **Бақылау:** Нақты уақыт режиміндегі мониторинг

## 2. Технологиялық стек
* **Backend:** C# (.NET 8 Core)
* **Frontend:** React (Redux Toolkit)
* **Геолокация:** Azure Maps API
* **Деректер қоры:** Microsoft SQL Server
* **Оркестрация:** Kubernetes (AKS)

## 3. Жеткізу тізбегінің архитектурасы
```mermaid
graph LR
    Order[Тапсырыс беру] --> Dispatch[Диспетчерлік қызмет]
    Dispatch --> Driver[Жүргізуші мобильді қолданбасы]
    Driver --> GPS[GPS Tracking]
    GPS --> System[.NET Backend]
    System --> Map[Картадағы бақылау: React]
    
    subgraph "Cloud Infrastructure"
        SQL[(SQL Server)]
        K8s[Kubernetes Cluster]
    end
    
    System --- K8s
    K8s --- SQL
